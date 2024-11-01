import 'package:flutter/material.dart';  
import 'package:flutter_cache_manager/flutter_cache_manager.dart';  
import 'package:flutter_svg/flutter_svg.dart';  
import 'package:http/http.dart' as http;  
import 'package:path_provider/path_provider.dart';  
import 'dart:io';  
import 'dart:typed_data';  
  
class ImageUpdateApi {  
  static final CacheManager _cacheManager = DefaultCacheManager();  
  
  static final Map<String, dynamic> imageConfig = {  
    "BaseUrl": "https://ipfs.safewatch.care/ipfs/Qmd2WLAjt3J9hTyxG1czVXpZGfRx7SJBohnKNrkGU4y92x/", 
    
    "imageSet": {  
      "InsightBG": "png/insightscreen.png",  
      "JournalBG": "png/journalscreen.png",  
      "MoodBG": "png/moodscreen.png",  
      "PlayingBG": "png/playingscreen.png",  
      "RecordingBG": "png/recordingscreen.png",  
      "backBtn": "png/backpage.png",  
      "emotionalBtn": "emotional.svg",  
      "image": "png/placeholder.png",  
      "lifeBtn": "liferec.svg",  
      "logo": "png/logo.png",  
      "logoText": "png/logowordmark.png",  
      "logoutBtn": "logout.svg",  
      "mentalBtn": "brain.svg",  
      "menu": "png/hamburger-menu.png",  
      "mood0Btn": "png/rainy.png",  
      "mood1Btn": "png/cloudy.png",  
      "mood2Btn": "png/cloudysunny.png",  
      "mood3Btn": "png/sunny.png",  
      "nextBtn": "png/nextpage.png",  
      "pauseBtn": "png/pause.png",  
      "physicalBtn": "phyex.svg",  
      "playBtn": "png/playbutton.png",  
      "player": "png/playerline.png",  
      "playing": "png/playing.png",  
      "rainbownBtn": "rainbow.svg",  
      "recordBtn": "png/microphone.png",  
      "recording": "png/playerline.png",  
      "setup": "png/setup-menu.png",  
      "spinner": "adole-spinner.svg",  
      "splash": "png/splash.png",  
      "stopBtn": "png/stop.png",  
      "workmark": "png/wordmark.png"  
    }  
  };  
  
  static String getAvatarUrl() {  
    final avatarUrl = "https://avatars.dicebear.com/api/micah/mroszales.jpg"; // Update with your avatar URL  
    return avatarUrl;  
  }  
  
  static String getImageUrl(String imageName) {  
    final baseUrl = imageConfig['BaseUrl'];  
    final imageSet = imageConfig['imageSet'];  
    final imagePath = imageSet[imageName];  
    return '$baseUrl$imagePath';  
  }  
  
  static Future<Uint8List?> _downloadImage(String imageUrl) async {  
    try {  
      final response = await http.get(Uri.parse(imageUrl));  
      if (response.statusCode == 200) {  
        return response.bodyBytes;  
      }  
    } catch (error) {  
      _handleError(error, '_downloadImage');  
    }  
    return null;  
  }  
  
  static Future<void> _saveImageToCache(String imageUrl,  
      Uint8List imageBytes) async {  
    try {  
      final cacheDirectory = await getTemporaryDirectory();  
      final sanitizedUrl = imageUrl.replaceAll(RegExp(r'[^\w\s\-_.]'), '');  
      final cacheFilePath = File('${cacheDirectory.path}/$sanitizedUrl');  
      await cacheFilePath.writeAsBytes(imageBytes);  
  
      print('Image saved in cache for image: $imageUrl');  
    } catch (error) {  
      _handleError(error, '_saveImageToCache');  
    }  
  }  
  
  static Future<Uint8List?> _getImageFromCache(String imageUrl) async {  
    try {  
      final cacheDirectory = await getTemporaryDirectory();  
      final sanitizedUrl = imageUrl.replaceAll(RegExp(r'[^\w\s\-_.]'), '');  
      final cacheFilePath = File('${cacheDirectory.path}/$sanitizedUrl');  
  
      if (await cacheFilePath.exists()) {  
        return await cacheFilePath.readAsBytes();  
      }  
    } catch (error) {  
      _handleError(error, '_getImageFromCache');  
    }  
    return null;  
  }  
  
  static Future<void> checkForAllImageUpdates() async {  
    try {  
      final imageSet = imageConfig['imageSet'];  
      for (String imageName in imageSet.keys) {  
        print('Checking ETag for image: $imageName');  
        await checkForImageUpdate(imageName);  
      }  
    } catch (error) {  
      _handleError(error, 'checkForAllImageUpdates');  
    }  
  }  
  
  static Future<bool> checkForImageUpdate(String imageName) async {  
    try {  
      final imageUrl = getImageUrl(imageName);  
      final response = await http.head(Uri.parse(imageUrl));  
      final currentETag = response.headers['etag'];  
  
      String? storedETag = await _getETagFromCache(imageUrl);  
      bool isImageUpdated = storedETag != currentETag;  
  
      if (isImageUpdated) {  
        if (imageUrl.endsWith('.svg')) {  
          final svgBytes = await _downloadImage(imageUrl);  
          if (svgBytes != null) {  
            await _saveImageToCache(imageUrl, svgBytes);  
          }  
        } else {  
          final imageBytes = await _downloadImage(imageUrl);  
          if (imageBytes != null) {  
            await _saveImageToCache(imageUrl, imageBytes);  
          }  
        }  
  
        await _saveETagToCache(imageUrl, currentETag, storedETag);  
        print('Image updated from server: $imageName');  
        print('New ETag fetched from server: $currentETag');  
        if (storedETag != null) {  
          print('Old ETag stored in cache: $storedETag');  
        }  
      } else {  
        print('Image fetched from cache: $imageName');  
      }  
  
      return isImageUpdated;  
    } catch (error) {  
      _handleError(error, 'checkForImageUpdate');  
      return false;    }  
  }  
  
  static Future<String?> _getETagFromCache(String imageUrl) async {  
    try {  
      final cacheDirectory = await getTemporaryDirectory();  
      final sanitizedUrl = imageUrl.replaceAll(RegExp(r'[^\w\s\-_.]'), '');  
      final cacheFilePath = File(  
          '${cacheDirectory.path}/etag_$sanitizedUrl.txt');  
  
      if (await cacheFilePath.exists()) {  
        return await cacheFilePath.readAsString();  
      }  
    } catch (error) {  
      _handleError(error, '_getETagFromCache');  
    }  
    return null;  
  }  
  
  static Future<void> _saveETagToCache(String imageUrl, String? eTag,  
      String? oldEtag) async {  
    try {  
      final cacheDirectory = await getTemporaryDirectory();  
      final sanitizedUrl = imageUrl.replaceAll(RegExp(r'[^\w\s\-_.]'), '');  
      final cacheFilePath = File(  
          '${cacheDirectory.path}/etag_$sanitizedUrl.txt');  
      await cacheFilePath.writeAsString(eTag ?? '');  
  
      if (eTag != null) {  
        print('New ETag saved in cache for image: $imageUrl');  
      }  
    } catch (error) {  
      _handleError(error, '_saveETagToCache');  
    }  
  }  
  
  static void _handleError(dynamic error, String methodName) {  
    print('Error in $methodName: $error');  
  }  
  
  static Widget renderImage(String imageName, {double width = 100.0, double height = 100.0}) {  
    return FutureBuilder<Uint8List?>(  
      future: _getImageFromCache(getImageUrl(imageName)),  
      builder: (context, snapshot) {  
        if (snapshot.connectionState == ConnectionState.waiting) {  
          return CircularProgressIndicator();  
        } else if (snapshot.hasError) {  
          return Text('Error: ${snapshot.error}');  
        } else if (snapshot.hasData) {  
          // Try to decode as SVG  
          try {  
            final svgString = String.fromCharCodes(snapshot.data!);  
            return SvgPicture.string(  
              svgString,  
              width: width,  
              height: height,  
            );  
          } catch (e) {  
            // Decoding as SVG failed, try PNG  
            return Image.memory(  
              snapshot.data!,  
              width: width,  
              height: height,  
            );  
          }  
        } else {  
          return Text('No image available.');  
        }  
      },  
    );  
  }  
}