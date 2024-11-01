*// ignore_for_file: avoid_print, file_names, non_constant_identifier_names, avoid_unnecessary_containers, no_leading_underscores_for_local_identifiers  
  
import 'dart:convert';  
import 'package:adole/Recom/Recom.dart';  
import 'package:adole/WeatherMap/weathermap.dart';  
import 'package:adole/utils/app_dimensions.dart';  
import 'package:cached_network_image/cached_network_image.dart';  
import 'package:flutter/material.dart';  
import 'dart:async';  
import 'dart:io';  
import 'package:path_provider/path_provider.dart';  
import 'package:flutter_sound/flutter_sound.dart';  
import 'package:intl/intl.dart';  
import 'package:permission_handler/permission_handler.dart';  
import 'package:shared_preferences/shared_preferences.dart';  
import 'package:uuid/uuid.dart';  
import 'package:web_socket_channel/web_socket_channel.dart';  
import '../ApiCall/ImageUpdateApi.dart';  
import '../ApiCall/VoiceJournalingApi.dart';  
  
  
class VoiceJournaling extends StatefulWidget {  
  const VoiceJournaling({Key? key}) : super(key: key);  
  @override  
  State<VoiceJournaling> createState() => _VoiceJournalingState();  
}  
  
class _VoiceJournalingState extends State<VoiceJournaling> {  
  final FlutterSoundRecorder _recorder = FlutterSoundRecorder();  
  final FlutterSoundPlayer _player = FlutterSoundPlayer();  
  
  final List<RecordedFile> _recordedFiles = [];  
  
  List<dynamic> recordingFiles = [];  
  String Path = "";  
  bool recognizing = false;  
  bool recognizeFinished = false;  
  bool _isRecording = false;  
  late DateTime _recordingDate;  
  late String _uuid = '';  
  bool _isPlaying = false;  
  bool _isRecordingComplete = false;  
  Duration _recordingDuration = const Duration(seconds: 0);  
  bool timerStarted = false;  
  WebSocketChannel? _socketChannel;  
  Sink? _socketSink;  
  int Is_playing = 0;  
  int _elapsedTime = 0;  
  late Timer _timer;  
  int highestElapsedTime = 0;  
  
  
  @override  
  void initState() {  
    super.initState();  
    checkMicrophonePermission();  
    _generateUUID();  
    _loadList();  
    _initializeRecorder();  
    _initializePlayer();  
    _connectWebSocket();  
    _listenForMessages();  
  }  
  
  void _connectWebSocket() {  
    final channel = WebSocketChannel.connect(  
      Uri.parse('wss://ssl.safewatch.care/audio'),  
    );  
    _socketChannel = channel;  
    _socketSink = channel.sink;  
  }  
  
  void _closeWebSocket() {  
    _socketChannel?.sink.close();  
    _socketChannel = null;  
    _socketSink = null;  
  }  
  
  void _listenForMessages() {  
    _socketChannel?.stream.listen(  
          (message) {  
        print("_listenForMessage method invoked");  
  
        if (message is String) {  
          // Handle the received text message as needed  
          print("Received Text message from server: $message");  
        } else if (message is List<int>) {  
          // Convert the message to a String using utf8 decoding  
          print("Decoding the message from the server");  
          String messageString = utf8.decode(message);  
  
          try {  
            final dynamic parsedMessage = jsonDecode(messageString);  
            if (parsedMessage is Map<String, dynamic>) {  
              // Assuming the received data is a JSON object with key "json"  
              if (parsedMessage.containsKey("json")) {  
                String nljson = parsedMessage["json"];  
                // Handle the nljson data as needed  
                print("Received data from server:");  
                print(const JsonEncoder.withIndent('  ')  
                    .convert(jsonDecode(nljson)));  
              } else {  
                // If the received data does not contain the "json" key  
                print(  
                    "Received data from server does not contain 'json' key: $parsedMessage");  
              }  
              if (parsedMessage.containsKey("transcription")) {  
                String transcription = parsedMessage["transcription"];  
                print("Received transcription: $transcription");  
              }  
            } else {  
              // Handle other types of messages if needed  
              print(  
                  "Received unsupported message type from server: $parsedMessage");  
            }  
          } catch (e) {  
            // Exception occurred while parsing the JSON data  
            print("Error parsing JSON data from server: $e");  
            print("Raw message: $messageString");  
  
            // If parsing as JSON fails, treat the message as a text message  
            print("Received text message from server: $messageString");  
          }  
        }  
      },  
      onError: (error) {  
        // Error occurred while receiving WebSocket messages  
        print("Error receiving WebSocket messages: $error");  
      },  
      onDone: () {  
        // WebSocket connection is closed  
        print("WebSocket connection closed.");  
      },  
    );  
  }  
  
  Future<List<int>> _getAudioBytes() async {  
    // Replace with the appropriate index for the recorded file you want to send  
    int index = _recordedFiles.length - 1;  
    try {  
      RecordedFile audioFile = _recordedFiles[index];  
      final File file = File(audioFile.path);  
      return await file.readAsBytes();  
    } catch (e) {  
      return [];  
    }  
  }  
  
  List<int> _convertToWav(List<int> audioBytes) {  
    // For demonstration purposes, we will just return the audioBytes as is.  
    return audioBytes;  
  }  
  
  Future<void> checkMicrophonePermission() async {  
    var status = await Permission.microphone.status;  
    if (status.isDenied) {  
      _showMicrophonePermissionPopup();  
    }  
  }  
  
  Future<void> _initializeRecorder() async {  
    await _recorder.openAudioSession();  
  }  
  
  Future<void> _generateUUID() async {  
    Uuid uuid = const Uuid();  
    String newUuid = uuid.v4();  
    SharedPreferences prefs = await SharedPreferences.getInstance();  
    String? storedUuid = prefs.getString('uuid');  
    if (storedUuid == null) {  
      await prefs.setString('uuid', newUuid);  
      setState(() {  
        _uuid = newUuid;  
      });  
    } else {  
      setState(() {  
        _uuid = storedUuid;  
      });  
    }  
  }  
  
  Future<void> _loadList() async {  
    // ignore: unnecessary_null_comparison  
    if (_uuid == null) {  
      print("UUID is not generated yet.");  
      return;    }  
    VoiceJournalingApi.loadList(_uuid).then((success) {  
      if (success != null) {  
        print("List loaded if condition");  
        setState(() {  
          recordingFiles = success;  
        });  
      } else {  
        print('not success:$success');  
      }  
    });  
  }  
  
  Future<void> _initializePlayer() async {  
    await _player.openAudioSession();  
  }  
  
  Future<void> _startRecording() async {  
    if (_player.isPlaying == true) {  
      await _player.stopPlayer();  
      setState(() {  
        _isPlaying = false;  
      });  
    }  
    Directory tempDir = await getTemporaryDirectory();  
    String fileName = DateTime.now().millisecondsSinceEpoch.toString();  
    String path = '${tempDir.path}/recorded_audio_$fileName.wav';  
    _recordingDate = DateTime.now();  
    _recorder.startRecorder(  
      toFile: path,  
      codec: Codec.pcm16WAV,  
    );  
    setState(() {  
      _isRecording = true;  
      Path = path;  
        _isRecording = true;  
        _elapsedTime = 0;  
        _startTimer();  
    });  
  
  }  
  
  Future<void> _stopRecording() async {  
    // Stop recording  
    print("Stop recording is Invoked");  
    await _player.stopPlayer();  
    setState(() {  
      _isPlaying = false;  
    });  
    await _recorder.stopRecorder();  
    DateTime recordingEndTime = DateTime.now();  
    _recordingDuration = recordingEndTime.difference(_recordingDate);  
    List<int> audioBytes = await _getAudioBytes();  
    List<int> wavAudio = _convertToWav(audioBytes);  
    RecordedFile recordedFile = RecordedFile(  
      path: Path.isEmpty ? '' : Path,  
      recordingDate: _recordingDate,  
      recordingDuration: _recordingDuration,  
    );  
    // Add the recorded file to the list  
    setState(() {  
      _isRecording = false;  
      _recordedFiles.add(recordedFile);  
      _isRecordingComplete = true;  
    });  
  
    // Save the list of recorded files in shared preferences  
    SharedPreferences prefs = await SharedPreferences.getInstance();  
    List<String> recordedFileStrings = _recordedFiles.map((file) => json.encode(file.toJson())).toList();  
    await prefs.setStringList('recordedFiles', recordedFileStrings);  
  
    // Send the configuration message and audio data to the server through WebSocket  
    try {  
      // Connect to the WebSocket server if not already connected  
      if (_socketChannel == null) {  
        _connectWebSocket();  
        _listenForMessages();  
      }  
      // Send the configuration message  
      String configMessage = '{ "config" : { "sample_rate" : 16000 } }'; // Replace 16000 with the correct sample rate  
      _socketSink?.add(utf8.encode(configMessage));  
      // Send the WAV audio data to the server  
      print("Audio data length: ${wavAudio.length}");  
      _socketSink?.add(wavAudio);  
      // Print statement indicating the message has been sent to the server  
      print("Message sent to server:");  
    } catch (e) {  
      print("Error sending data to server: $e");  
    }  
    _storeRecordedFile(_recordedFiles[0], _uuid);  
  
    setState(() {  
      _isRecording = false;  
      _stopTimer();  
    });  
  }  
  
  Future<void> _play(String filePath) async {  
    print("url path:$filePath");  
    await _player.openAudioSession();  
    await _player.startPlayer(  
      fromURI: filePath,  
      whenFinished: () {  
        setState(() {  
          _isPlaying = false;  
        });  
      },  
    );  
    setState(() {  
      _isPlaying = true;  
    });  
  }  
  
  Future<void> _playurl(String filePath) async {  
    setState(() {  
      _isPlaying = true;  
    });  
    await _player.startPlayer(fromURI: filePath);  
  }  
  
  Future<void> _pause(String filePath) async {  
    print("url path: $filePath");  
    setState(() {  
      _isPlaying = false;  
    });  
    await _player.pausePlayer();  
  }  
  
  void _showMicrophonePermissionPopup() {  
    showDialog(  
      context: context,  
      builder: (BuildContext context) {  
        return AlertDialog(  
          title: const Text("Microphone Permission"),  
          content: const Text(  
              "Please grant microphone permission to use this feature."),  
          actions: [  
            TextButton(  
              child: const Text("Open Settings"),  
              onPressed: () {  
                // Open app settings  
                openAppSettings();  
                Navigator.of(context).pop();  
              },  
            ),  
            TextButton(  
              child: const Text("Cancel"),  
              onPressed: () {  
                Navigator.push(  
                    context,  
                    MaterialPageRoute(  
                        builder: (context) => const weathermap()));  
              },  
            ),  
          ],  
        );  
      },  
    );  
  }  
  
  void _setCounterToOne() {  
    setState(() {  
      Is_playing = 1; // Set counter to 1 and trigger UI update  
    });  
  }  
  
  void _setCounterToZero() {  
    setState(() {  
      Is_playing = 0; // Set counter to 0 and trigger UI update  
    });  
  }  
  
  
  void reverseTimer() {  
    _timer = Timer.periodic(Duration(seconds: 1), (timer) {  
      if (_elapsedTime > 0) {  
        setState(() {  
          _elapsedTime--;  
        });  
      } else {  
        timer.cancel(); // Stop the timer when _elapsedTime reaches 0  
      }  
    });  
  }  
  
    void _startTimer() {  
      _timer = Timer.periodic(Duration(seconds: 1), (timer) {  
        setState(() {  
          _elapsedTime++;  
        });  
      });  
    }  
  
  
    void _stopTimer() {  
      _timer.cancel();  
    }  
  
  
  @override  
  void dispose() {  
    super.dispose();  
    _closeWebSocket();  
    _timer.cancel();  
    super.dispose();  
  }  
  
  @override  
  Widget build(BuildContext context) {  
    return Scaffold(  
        extendBodyBehindAppBar: true,  
        resizeToAvoidBottomInset: false,  
        appBar: PreferredSize(  
          preferredSize: Size.fromHeight(AppDimensions.height10(context) * 10.0),  
          child: Container(  
            color: Colors.black.withOpacity(1.0),  
            height: AppDimensions.height10(context) * 10,  
            child: AppBar(  
              elevation: 0,  
              centerTitle: true,  
              backgroundColor: Colors.transparent,  
              automaticallyImplyLeading: true,  
              leading: Container(  
                margin: EdgeInsets.only(left: 16, top: 8),  
                child: SizedBox(  
                  width: AppDimensions.height10(context) * 7.0,  
                  height: AppDimensions.height10(context) * 7.0,  
                  child: CachedNetworkImage(  
                    imageUrl: ImageUpdateApi.getImageUrl('menu'),  
                    fit: BoxFit.contain,  
                    errorWidget: (context, url, error) => Icon(Icons.error),  
                  ),  
                ),  
              ),  
              title: Row(  
                mainAxisAlignment: MainAxisAlignment.center,  
                children: [  
                  Container(  
                    width: AppDimensions.height10(context) * 20.9,  
                    height: AppDimensions.height10(context) * 5.3,  
                    color: Colors.transparent,  
                    child: Center(  
                      child: CachedNetworkImage(  
                        imageUrl: ImageUpdateApi.getImageUrl('workmark'),  
                        width: AppDimensions.height10(context) * 17.9,  
                        height: AppDimensions.height10(context) * 6.3,  
                        fit: BoxFit.contain,  
                        errorWidget: (context, url, error) => const Icon(Icons.error),  
                      ),  
                    ),  
                  ),  
                  SizedBox(width: AppDimensions.height10(context) * 5.0),  
                  Container(  
                    width: AppDimensions.height10(context) * 5.0,  
                    height: AppDimensions.height10(context) * 5.0,  
                    margin: EdgeInsets.only(top: 8), // Adjust top margin as needed  
                    color: Colors.transparent,  
                    child: CachedNetworkImage(  
                      imageUrl: ImageUpdateApi.getAvatarUrl(),  
                      fit: BoxFit.contain,  
                      errorWidget: (context, url, error) => const Icon(Icons.error),  
                    ),  
                  ),  
                ],  
              ),  
            ),  
          ),  
        ),  
  
        body: Stack(  
          //Background of Screen  
          children: <Widget>[  
              
            // Background for screen  
            Container(  
              width: MediaQuery.of(context).size.width,  
              height: MediaQuery.of(context).size.height,  
              decoration: BoxDecoration(  
                gradient: LinearGradient(  
                  begin: Alignment.topLeft,  
                  end: Alignment.bottomRight,  
                  colors: [Colors.blue, Colors.purple],  
                  stops: [0.0, 0.7], // Adjust stops to control color blending  
                  transform: GradientRotation(270), // Set the angle to 45 degrees  
                ),  
              ),  
            ),  
  
            Column(  
              mainAxisAlignment: MainAxisAlignment.start,  
              crossAxisAlignment: CrossAxisAlignment.center,  
              children: <Widget>[  
  
                //For Spacing  
                recordingFiles.isNotEmpty  
                    ? SizedBox(height: AppDimensions.height10(context) * 2)  
                    : SizedBox(height: AppDimensions.height10(context) * 12),  
  
                //Main list recording box  
                recordingFiles.isNotEmpty  
                    ? SizedBox(  
                    width: AppDimensions.height10(context) * 38,  
                    height: AppDimensions.height10(context) * 6.4 * 8,  
                    child: ClipRRect(  
                    child: Container(  
                    color: Color(0x00000000).withOpacity(0.3),  
                    child: SingleChildScrollView(  
                      child: Column(  
                        children: List.generate(  
                          recordingFiles.length,  
                              (index) => Column(  
                            mainAxisAlignment: MainAxisAlignment.start,  
                            crossAxisAlignment: CrossAxisAlignment.center,  
                            children: [  
                              SizedBox(  
                                width: AppDimensions.height10(context) * 34.8,  
                                height: AppDimensions.height10(context) * 6.4,  
                                // color: Colors.blue,  
                                child: Row(  
                                  mainAxisAlignment: MainAxisAlignment.spaceBetween,  
                                  crossAxisAlignment: CrossAxisAlignment.start,  
                                  children: [  
                                    GestureDetector(  
                                      onTap: () {  
                                        _recorder.stopRecorder();  
                                        setState(() {  
                                          _isRecording = false;  
                                        });  
                                        print("hello world button click:${recordingFiles[index]["url"]}");  
                                        _playurl(recordingFiles[index]["url"]);  
                                      },  
                                      //List play/pause icons  
                                      child: Container(  
                                        width: AppDimensions.height10(context) * 4.9,  
                                        height: AppDimensions.height10(context) * 4.9,  
                                        decoration: const BoxDecoration(  
                                            color: Colors.white,  
                                            shape: BoxShape.circle),  
                                        child: Center(  
                                          child: CachedNetworkImage(  
                                            imageUrl: ImageUpdateApi.getImageUrl('playBtn'),  
                                            width: AppDimensions.height10(context) * 2.8,  
                                            height: AppDimensions.height10(context) * 2.5,  
                                            fit: BoxFit.fill,  
                                            errorWidget: (context, url, error) => const Icon(Icons.error),  
                                          ),  
                                        ),  
                                      ),  
                                    ),  
                                    SizedBox(  
                                      width: AppDimensions.height10(context) * 16.1,  
                                      child: Column(  
                                        mainAxisAlignment: MainAxisAlignment.center,  
                                        crossAxisAlignment: CrossAxisAlignment.start,  
                                        children: [  
                                          Container(  
                                            child: Text(  
                                                recordingFiles[index]["title"],  
                                                style: TextStyle(  
                                                    fontSize: AppDimensions.height10(context) * 1.4,  
                                                    fontWeight: FontWeight.w500,  
                                                    color: Colors.white)),  
                                          ),  
                                          Container(  
                                            child: Text(DateFormat('MMM yyyy,dd').  
                                            format(DateTime.fromMillisecondsSinceEpoch(  
                                                int.parse(recordingFiles[index]["timestamp"])  
                                            )),  
                                              style: TextStyle(fontSize: AppDimensions.height10(context) * 1.2,  
                                                  fontWeight: FontWeight.w400,  
                                                  color: Colors.white),  
                                            ),  
                                          ),  
                                        ],  
                                      ),  
                                    ),  
                                    Container(  
                                      padding: EdgeInsets.only(top: AppDimensions.height10(context) * 1.5),  
                                      width: AppDimensions.height10(context) * 7.0,  
                                      child: Text(  
                                        '${00}.${Duration(minutes: int.parse(recordingFiles[index]["duration"])).inMinutes.remainder(60).toString().padLeft(2, '0')}.${Duration(seconds: int.parse(recordingFiles[index]["duration"])).inSeconds.remainder(60).toString().padLeft(2, '0')}',  
                                        style: TextStyle(  
                                            fontSize:  
                                            AppDimensions.height10(context) * 0.9,  
                                            fontWeight: FontWeight.w700,  
                                            color: const Color(0xFFFFC727)),  
                                      ),  
                                    ),  
                                  ],  
                                ),  
                              ),  
                            ],  
                          ),  
                        ),  
                      ),  
                    ),  
                  ),  
                  ),  
                )  
  
                    : SizedBox(  
                    width: AppDimensions.height10(context) * 38,  
                    height: AppDimensions.height10(context) * 6.4 * 8,  
                    child: ClipRRect(  
                      borderRadius: BorderRadius.circular(10),  
                      child: Container(  
                    color: Color(0x00000000).withOpacity(0.3),  
                  ),  
                ),  
                ),  
  
                  //Transcription Lines  
                  SizedBox(height: AppDimensions.height10(context) * 10),  
                    
                // Playlist navigation  
                if(Is_playing == 0)  
                  SizedBox(height: AppDimensions.height10(context) * 0.5),  
  
                if(Is_playing == 0)  
                Center(  
                  child: SizedBox(  
                    width: AppDimensions.height10(context) * 38.0,  
                    height: AppDimensions.height10(context) * 6.0,  
                    child: Row(  
                      mainAxisAlignment: MainAxisAlignment.spaceBetween,  
                      crossAxisAlignment: CrossAxisAlignment.center,  
                      children: [  
                        //Playlist Back Button  
                        GestureDetector(  
                          onTap: () {  
  
                          },  
                          child: SizedBox(  
                            width: AppDimensions.height10(context) * 6.0,  
                            height: AppDimensions.height10(context) * 6.0,  
                            child: FutureBuilder<bool>(  
                              builder: (context, snapshot) {  
                                double whiteCircleSize = 1.2;  
                                double circleSize = AppDimensions.height10(context) * 8.0 * whiteCircleSize;  
                                return Stack(  
                                  children: [  
                                    // Enlarge the white circle by adjusting the container size  
                                    Container(  
                                      width: circleSize,  
                                      height: circleSize,  
                                      decoration: BoxDecoration(  
                                        shape: BoxShape.circle,  
                                        color: Colors.white,  
                                        boxShadow: [  
                                          BoxShadow(  
                                            color: Colors.black26.withOpacity(0.4),  
                                            spreadRadius: 5,  
                                            blurRadius: 7,  
                                            offset: Offset(0, 3),  
                                          ),  
                                        ],  
                                      ),  
                                      child: Center(  
                                        child: GestureDetector(  
                                          onTap: () {  
                                            // Add your onTap logic here for the backBtn image  
                                          },  
                                          child: CachedNetworkImage(  
                                            imageUrl: ImageUpdateApi.getImageUrl('backBtn'),  
                                            fit: BoxFit.contain,  
                                            width: AppDimensions.height10(context) * 4,  
                                            height: AppDimensions.height10(context) * 4,  
                                            errorWidget: (context, url, error) =>  
                                            const Icon(Icons.error),  
                                          ),  
                                        ),  
                                      ),  
                                    ),  
                                  ],  
                                );  
                              },  
                            ),  
                          ),  
                        ),  
  
                        //Playlist Play-Stop Button  
                        GestureDetector(  
                          onTap: () {  
                            if (_isPlaying == false) {  
                              _recorder.stopRecorder();  
                              setState(() {  
                                _isRecording = false;  
                              });  
                              _play(Path);  
                            } else {  
                              _pause(Path);  
                              _stopTimer();  
                            }  
                            reverseTimer();  
                            _setCounterToOne();  
                          },  
  
                          child: _isPlaying == false  
                              ? Center(  
                            child: Container(  
                              width: AppDimensions.height10(context) * 6, // Adjust size and padding  
                              height: AppDimensions.height10(context) * 6, // Adjust size and padding  
                              decoration: BoxDecoration(  
                                shape: BoxShape.circle,  
                                color: Colors.white,  
                                boxShadow: [  
                                  BoxShadow(  
                                    color: Colors.black26.withOpacity(0.4),  
                                    spreadRadius: 5,  
                                    blurRadius: 7,  
                                    offset: Offset(0, 3),  
                                  ),  
                                ],  
                              ),  
                              child: Center(  
                                child: CachedNetworkImage(  
                                  imageUrl: ImageUpdateApi.getImageUrl('playBtn'), // Use correct image name from your config  
                                  width: AppDimensions.height10(context) * 4.5,  
                                  height: AppDimensions.height10(context) * 4.5,  
                                  fit: BoxFit.fill,  
                                  placeholder: (context, url) => const CircularProgressIndicator(),  
                                  errorWidget: (context, url, error) => const Icon(Icons.error),  
                                ),  
                              ),  
                            ),  
                          )  
                              : Center(  
                            child: Container(  
                              width: AppDimensions.height10(context) * 6, // Adjust size and padding  
                              height: AppDimensions.height10(context) * 6, // Adjust size and padding  
                              decoration: BoxDecoration(  
                                shape: BoxShape.circle,  
                                color: Colors.white,  
                                boxShadow: [  
                                  BoxShadow(  
                                    color: Colors.black26.withOpacity(0.4),  
                                    spreadRadius: 5,  
                                    blurRadius: 7,  
                                    offset: Offset(0, 3),  
                                  ),  
                                ],  
                              ),  
                              child: Center(  
                                child: CachedNetworkImage(  
                                  imageUrl: ImageUpdateApi.getImageUrl('pauseBtn'), // Use correct image name from your config  
                                  width: AppDimensions.height10(context) * 4.5,  
                                  height: AppDimensions.height10(context) * 4.5,  
                                  fit: BoxFit.contain,  
                                  placeholder: (context, url) => const CircularProgressIndicator(),  
                                  errorWidget: (context, url, error) => const Icon(Icons.error),  
                                ),  
                              ),  
                            ),  
                          ),  
                        ),  
  
                        //Playlist Mic Button  
                        GestureDetector(  
                          onTap: () {  
                            if (_isRecording) {  
                              _stopRecording();  
                            } else {  
                              _startRecording();  
                            }  
                          },  
  
                          child: Center(  
                            child: _isRecording  
                                ? Container(  
                                  width: AppDimensions.height10(context) * 6 , // Adjust size and padding  
                                  height: AppDimensions.height10(context) * 6, // Adjust size and padding  
                                  decoration: BoxDecoration(  
                                  shape: BoxShape.circle,  
                                  color: Colors.white,  
                                  boxShadow: [  
                                    BoxShadow(  
                                      color: Colors.black26.withOpacity(0.4),  
                                      spreadRadius: 5,  
                                      blurRadius: 7,  
                                      offset: Offset(0, 3),  
                                  ),  
                                ],  
                              ),  
                                child: Center(  
                                  child: CachedNetworkImage(  
                                    imageUrl: ImageUpdateApi.getImageUrl('pauseBtn'),  
                                    width: AppDimensions.height10(context) * 5.1,  
                                    height: AppDimensions.height10(context) * 4.8,  
                                    fit: BoxFit.fitHeight,  
                                    errorWidget: (context, url, error) => const Icon(Icons.error),  
                                ),  
                              ),  
                            )  
                                : Container(  
                                  width: AppDimensions.height10(context) * 6 , // Adjust size and padding  
                                  height: AppDimensions.height10(context) * 6, // Adjust size and padding  
                                  decoration: BoxDecoration(  
                                  shape: BoxShape.circle,  
                                  color: Colors.white,  
                                  boxShadow: [  
                                    BoxShadow(  
                                      color: Colors.black26.withOpacity(0.4),  
                                      spreadRadius: 5,  
                                      blurRadius: 7,  
                                      offset: Offset(0, 3),  
                                    ),  
                                  ],  
                              ),  
                                  child: Center(  
                                    child: CachedNetworkImage(  
                                      imageUrl: ImageUpdateApi.getImageUrl('recordBtn'),  
                                      width: AppDimensions.height10(context) * 5.1,  
                                      height: AppDimensions.height10(context) * 4.8,  
                                      fit: BoxFit.fitHeight,  
                                      errorWidget: (context, url, error) => const Icon(Icons.error),  
                                    ),  
                                  ),  
                            ),  
                          ),  
                        ),  
  
                        //Playlist Next Button  
                        GestureDetector(  
                          onTap: () {  
  
                          },  
                          child: SizedBox(  
                            width: AppDimensions.height10(context) * 6.0,  
                            height: AppDimensions.height10(context) * 6.0,  
                            child: FutureBuilder<bool>(  
                              builder: (context, snapshot) {  
                                double whiteCircleSize = 1.2;  
                                double circleSize = AppDimensions.height10(context) * 8.0 * whiteCircleSize;  
                                return Stack(  
                                  children: [  
                                    // Enlarge the white circle by adjusting the container size  
                                    Container(  
                                      width: circleSize,  
                                      height: circleSize,  
                                      decoration: BoxDecoration(  
                                        shape: BoxShape.circle,  
                                        color: Colors.white,  
                                        boxShadow: [  
                                          BoxShadow(  
                                            color: Colors.black26.withOpacity(0.4),  
                                            spreadRadius: 5,  
                                            blurRadius: 7,  
                                            offset: Offset(0, 3),  
                                          ),  
                                        ],  
                                      ),  
                                      child: Center(  
                                        child: GestureDetector(  
                                          onTap: () {  
                                            // Add your onTap logic here for the backBtn image  
                                          },  
                                          child: CachedNetworkImage(  
                                            imageUrl: ImageUpdateApi.getImageUrl('nextBtn'),  
                                            fit: BoxFit.fill,  
                                            width: AppDimensions.height10(context) * 4,  
                                            height: AppDimensions.height10(context) * 4,  
                                            errorWidget: (context, url, error) =>  
                                            const Icon(Icons.error),  
                                          ),  
                                        ),  
                                      ),  
                                    ),  
                                  ],  
                                );  
                              },  
                            ),  
                          ),  
                        ),  
                      ],  
                    ),  
                  ),  
                ),  
  
  
                //Square Box for playing and pause  
                if(Is_playing == 1)  
                  SizedBox(height: AppDimensions.height10(context) * 1),  
  
                if(Is_playing == 1)  
                  Center(  
                    child: Row(  
                      mainAxisAlignment: MainAxisAlignment.spaceBetween,  
                      crossAxisAlignment: CrossAxisAlignment.center,  
                      children: [  
                        Container(  
                          margin: EdgeInsets.only(left : AppDimensions.height10(context) * 3.0),  
                          width: AppDimensions.height10(context) * 5.0,  
                          height: AppDimensions.height10(context) * 5.0,  
                          color: Colors.transparent,  
                          child: Column(  
                            mainAxisAlignment: MainAxisAlignment.center,  
                            children: [  
                              Text(  
                                '$_elapsedTime',  
                                style: TextStyle(  
                                  fontSize: AppDimensions.height10(context) * 4,  
                                  fontWeight: FontWeight.w700,  
                                  color: const Color(0xFFFFFFFF),  
                                ),  
                              ),  
                            ],  
                          ),  
                        ),  
  
                        Center(  
                          child: Container(  
                            width: AppDimensions.height10(context) * 7.0,  
                            height: AppDimensions.height10(context) * 7.0,  
                            decoration: BoxDecoration(  
                              color: Colors.black,  
                              boxShadow: [  
                                BoxShadow(  
                                  color: Colors.black26.withOpacity(0.4),  
                                  spreadRadius: 5,  
                                  blurRadius: 7,  
                                  offset: Offset(0, 3),  
                                ),  
                              ],  
                            ),  
                            child: GestureDetector(  
                              onTap: () {  
                                if (_isPlaying == false) {  
                                  _recorder.stopRecorder();  
                                  setState(() {  
                                    _isRecording = false;  
                                  });  
                                  _play(Path);  
                                } else {  
                                  _pause(Path);  
                                }  
                              },  
                              child: _isPlaying == false  
                                  ? Center(  
                                child: Container(  
                                  width: AppDimensions.height10(context) * 6, // Adjust size and padding  
                                  height: AppDimensions.height10(context) * 6, // Adjust size and padding  
                                  child: Center(  
                                    child: CachedNetworkImage(  
                                      imageUrl: ImageUpdateApi.getImageUrl('playBtn'), // Use correct image name from your config  
                                      width: AppDimensions.height10(context) * 4.5,  
                                      height: AppDimensions.height10(context) * 4.5,  
                                      fit: BoxFit.fill,  
                                      placeholder: (context, url) => const CircularProgressIndicator(),  
                                      errorWidget: (context, url, error) => const Icon(Icons.error),  
                                    ),  
                                  ),  
                                ),  
                              )  
                                  : Center(  
                                child: Container(  
                                  width: AppDimensions.height10(context) * 6, // Adjust size and padding  
                                  height: AppDimensions.height10(context) * 6, // Adjust size and padding  
                                  child: Center(  
                                    child: CachedNetworkImage(  
                                      imageUrl: ImageUpdateApi.getImageUrl('pauseBtn'), // Use correct image name from your config  
                                      width: AppDimensions.height10(context) * 4.5,  
                                      height: AppDimensions.height10(context) * 4.5,  
                                      fit: BoxFit.contain,  
                                      placeholder: (context, url) => const CircularProgressIndicator(),  
                                      errorWidget: (context, url, error) => const Icon(Icons.error),  
                                    ),  
                                  ),  
                                ),  
                              ),  
                            ),  
                          ),  
                        ),  
  
                        Container(  
                          margin: EdgeInsets.only(  
                            right : AppDimensions.height10(context) * 3.0  
                          ),  
                          width: AppDimensions.height10(context) * 5.0,  
                          height: AppDimensions.height10(context) * 5.0,  
                          color: Colors.transparent,  
                          child: Column(  
                            mainAxisAlignment: MainAxisAlignment.center,  
                            children: [  
                              Text(  
                                '${_recordingDuration.inSeconds.remainder(60).toString().padLeft(2, '0')}',  
                                style: TextStyle(  
                                  fontSize: AppDimensions.height10(context) * 4,  
                                  fontWeight: FontWeight.w700,  
                                  color: const Color(0xFFFFFFFF),  
                                ),  
                              ),  
                            ],  
                          ),  
                        ),  
                      ],  
                    ),  
                  ),  
  
  
                SizedBox(height: AppDimensions.height10(context) * 1),  
                if(Is_playing == 0)  
                Container(  
                  child : Text(  
                    '$_elapsedTime seconds',  
                style: TextStyle(  
                  fontSize: AppDimensions.height10(context) * 2,  
                  fontWeight: FontWeight.w700,  
                  color: const Color(0xFFFFFFFF),  
                  ),  
                  ),  
                ),  
  
                // if(Is_playing == 0)  
                // Container(                //   child: LinearProgressIndicator(                //     color: Colors.amber,                //     backgroundColor: Colors.black,                //     valueColor: AlwaysStoppedAnimation(Colors.blue),                //     value: 0.5,                //   ),                // ),  
                // Screen navigation                SizedBox(height: AppDimensions.height10(context) * 1.0),  
                Container(  
                  color: Colors.white.withOpacity(0.5),  
                  height: AppDimensions.height10(context) * 6,  
                  child: Row(  
                    mainAxisAlignment: MainAxisAlignment.spaceEvenly,  
                    crossAxisAlignment: CrossAxisAlignment.center,  
                    children: [  
                      //Back btn  
                      GestureDetector(  
                        onTap: () {  
                          Navigator.push(  
                            context,  
                            MaterialPageRoute(  
                              builder: (context) => const weathermap(),  
                            ),  
                          );  
                        },  
                        child: Center(  
                          child: Center(  
                            child: CachedNetworkImage(  
                              imageUrl: ImageUpdateApi.getImageUrl('backBtn'),  
                              width: AppDimensions.height10(context) * 5.50,  
                              height: AppDimensions.height10(context) * 3.50,  
                              fit: BoxFit.contain,  
                              errorWidget: (context, url, error) =>  
                              const Icon(Icons.error),  
                            ),  
                          ),  
                        ),  
                      ),  
  
                      if(Is_playing == 0)  
                      GestureDetector(  
                        onTap: () {  
                          Navigator.push(  
                            context,  
                            MaterialPageRoute(  
                              builder: (context) => const Recom(),  
                            ),  
                          );  
                        },  
  
                        child: Container(  
                          child: SizedBox(  
                            width: AppDimensions.height10(context) * 6.0,  
                            height: AppDimensions.height10(context) * 6.0,  
                            child: FutureBuilder<bool>(  
                              builder: (context, snapshot) {  
                                double whiteCircleSize = 1.2;  
                                double circleSize = AppDimensions.height10(context) * 8.0 * whiteCircleSize;  
                                return Stack(  
                                  children: [  
                                    // Enlarge the white circle by adjusting the container size  
                                    Container(  
                                      width: circleSize,  
                                      height: circleSize,  
                                      decoration: BoxDecoration(  
                                        shape: BoxShape.circle,  
                                        color: Colors.white,  
                                        boxShadow: [  
                                          BoxShadow(  
                                            color: Colors.black26.withOpacity(0.4),  
                                            spreadRadius: 5,  
                                            blurRadius: 7,  
                                            offset: Offset(0, 3),  
                                          ),  
                                        ],  
                                      ),  
                                    ),  
                                    Positioned.fill(  
                                      // Center the image on top of the white circle  
                                      child: Center(  
                                        child: CachedNetworkImage(  
                                          imageUrl: ImageUpdateApi.getImageUrl('logo'),  
                                          fit: BoxFit.contain,  
                                          width: AppDimensions.height10(context) * 4,  
                                          height: AppDimensions.height10(context) * 4,  
                                          errorWidget: (context, url, error) =>  
                                          const Icon(Icons.error),  
                                        ),  
                                      ),  
                                    ),  
                                  ],  
                                );  
                              },  
                            ),  
                          ),  
                        ),  
                      ),  
  
                      if(Is_playing == 1)  
                      GestureDetector(  
                        onTap: () {  
                          _setCounterToZero();  
                        },  
  
                          child: Container(  
                            width: AppDimensions.height10(context) * 5.0,  
                            height: AppDimensions.height10(context) * 5.0,  
                            decoration: BoxDecoration(  
                              color: Colors.black,  
                              boxShadow: [  
                                BoxShadow(  
                                  color: Colors.black26.withOpacity(0.4),  
                                  spreadRadius: 5,  
                                  blurRadius: 7,  
                                  offset: Offset(0, 3),  
                                ),  
                              ],  
                            ),  
                            child: GestureDetector(  
                              onTap: () {  
                                _setCounterToZero();  
                              },  
                              child: Padding(  
                                padding: const EdgeInsets.all(5),  
                                child: CachedNetworkImage(  
                                  imageUrl: ImageUpdateApi.getImageUrl('logo'),  
                                  fit: BoxFit.contain,  
                                  width: AppDimensions.height10(context) * 3.5,  
                                  height: AppDimensions.height10(context) * 3.5,  
                                  errorWidget: (context, url, error) =>  
                                  const Icon(Icons.error),  
                                ),  
                              ),  
                            ),  
                          )  
                      ),  
  
                      //Next Btn  
                      GestureDetector(  
                        onTap: () {  
                          Navigator.push(  
                            context,  
                            MaterialPageRoute(  
                              builder: (context) => const Recom(),  
                            ),  
                          );  
                        },  
                        child: Center(  
                          child: CachedNetworkImage(  
                            imageUrl: ImageUpdateApi.getImageUrl('nextBtn'),  
                            // Use correct image name from your config  
                            width: AppDimensions.height10(context) * 5.50,  
                            height: AppDimensions.height10(context) * 3.50,  
                            fit: BoxFit.contain,  
                            // placeholder: (context, url) =>  
                            // const CircularProgressIndicator(),                            errorWidget: (context, url, error) =>  
                            const Icon(Icons.error),  
                          ),  
                        ),  
                      ),  
                    ],  
                  ),  
                ),  
              ],  
            ),  
          ],  
        ));  
  }  
  
  // Method to store the recorded file  
  void _storeRecordedFile(RecordedFile recordedFile, String? _uuid) async {  
    if (!_isRecordingComplete) {  
      print("Recording not complete");  
      return;    }  
  
    try {  
      print("Preparing Audio to be uploaded");  
      // Prepare the audio file for uploading  
      File audioFile = File(recordedFile.path);  
  
      // Read the audio data as bytes  
      List<int> audioBytes = await audioFile.readAsBytes();  
  
      String auth = ' YWRvbGU6MTIzIGFkb2xl';  
  
      String uid = _uuid ?? ''; // Handle possible null _uuid  
      // Generating the hash by uploading audio      String? hash = await VoiceJournalingApi.uploadAudioAndGetHash(auth, audioFile);  
  
      if (hash != null) {  
        print("API Request Data:");  
        print("Transcription: EMPTY TRANSCRIPTION");  
        print("UID: $uid");  
        print("Recording Date: ${DateTime.now()}");  
        print("Hash: $hash");  
  
        // Make API request to store the recorded audio file  
        bool isSuccess = await VoiceJournalingApi.addEntry(  
          'EMPTY TRANSCRIPTION', // Default value if transcription is empty  
          uid,  
          DateTime.now(),  
          hash,  
          audioBytes,  
        );  
        if (isSuccess) {  
          print("UI updating: audio file uploaded");  
          // Clear the recorded audio file data and reset UI state  
          setState(() {  
            _isRecordingComplete = false;  
            _recordedFiles.clear();  
            _recordingDuration = const Duration(seconds: 0);  
          });  
        } else {  
          print("UI not updating: error in API call");  
          // Handle error if necessary  
        }  
      } else {  
        print("Error uploading audio or getting hash");  
        // Handle error if necessary  
      }  
    } catch (error) {  
      print("Error: $error");  
      // Handle error if necessary  
    }  
  }  
  
// void _disposeRecordedFile() {  
//   // Clear the recorded audio file data and reset UI state  
//   setState(() {  
//     _isRecordingComplete = false;  
//     _recordedFiles.clear();  
//     _recordingDuration = const Duration(seconds: 0);  
//   });  
// }  
  
}  
  
class RecordedFile {  
  final String path;  
  final DateTime recordingDate;  
  final Duration recordingDuration;  
  
  RecordedFile({  
    required this.path,  
    required this.recordingDate,  
    required this.recordingDuration,  
  });  
  
  factory RecordedFile.fromJson(Map<String, dynamic> json) {  
    return RecordedFile(  
      path: json['path'],  
      recordingDate: DateTime.parse(json['recordingDate']),  
      recordingDuration: Duration(milliseconds: json['recordingDuration']),  
    );  
  }  
  
  Map<String, dynamic> toJson() {  
    return {  
      'path': path,  
      'recordingDate': recordingDate.toIso8601String(),  
      'recordingDuration': recordingDuration.inMilliseconds,  
    };  
  }  
}