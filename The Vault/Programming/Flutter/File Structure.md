Tags : #flutter #Programming 
## Main Project Structure 
- `.idea` : Project related settings (Code editor settings), this one is project specific. 
- `Android folder` : The android folder inside flutter project contains the android platform specific settings, resources and code. If you need to write any platform specific code, we will be making changes in here.
- `Build folder` : The build folder contains the output generated when you build or run the flutter project. You will find the release related files/folders like apk's and app bundles in here. It is a type of run time generated folder. 
- `IOS folder` : Similar to android folder, the IOS folder contains IOS specific settings, resources and code. You will make the platform specific code or changes in here.
- `Lib folder` :  The lib folder is main folder where you will write all the Flutter app related codes. Initially it will contain just one single file main. Dart which has the entry point for a flutter app. 
- `Test folder` : The test folder is set to contain any testing related codes that you can write. If you decide to write test cases, you will be adding code in here.
- `.gitignore folder` : It's a type of VCS (Version Control System), so that's that! You can adjust the .gitgnore file to include/exclude any files/folders as you need.
- `.metadata` : File contains flutter project related metadata that flutter tool uses. You should not make manual changes to this file. 
- `.packages` : A flutter project code is composed of numerous libraries and packages. Some packages are pre-installed with Flutter while others are downloaded during development. The .packages holds the paths to each of the libraries/packages un your local computer. We do not need to make any manual changes to this file.
- `Pubspec.yaml file` : The Pubspec.yaml contains Flutter app specific metadata and configurations. You can configure dependencies such as external packages, image assets, font files, app versions etc. With the help of this file. You can often make changes to the pubspec.yaml file to add external dependencies. 
- `Pubspec.lock file` : Dependent on pubspec.yaml file, as this file is lists the specific versions of each dependency that packages use in your app and ensures the version stays consistent across different developers machine. No need to make any changes here. 