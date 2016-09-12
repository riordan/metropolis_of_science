Metropolis of Science
======================
Mobile app for [Metropolis of Science](http://metropolisofscience.org/) created and maintained by students in the [M.A. Science, Environment and Medicine Journalism Program at the Columbia University Graduate School of Journalism](https://journalism.columbia.edu/ma-science-environment-medicine). This mobile app was developed by @juanfrans and is built using [Apache Cordova](https://cordova.apache.org).

# Installation and Build
## Prerequisites
This application uses [Apache Cordova](https://cordova.apache.org) to build mobile applications for Apple iOS (iPhone) and Google Android.

1. [Install nodejs & npm](https://nodejs.org/en/)
2. Install Apache Cordova `$ npm install -g cordova` or `$ sudo npm install -g cordova`
3.
Additional details on installing cordova can be found in the [official cordova installation guide](https://cordova.apache.org/docs/en/latest/guide/cli/#installing-the-cordova-cli).

### iOS Prerequisites
To build for iOS you MUST run this build on a Mac (or theoretically using [Adobe's Phonegap Build](https://build.phonegap.com/) service, though I haven't tested this).

**Follow the [Cordova iOS Guide](https://cordova.apache.org/docs/en/latest/guide/platforms/ios/index.html).** The instructions here are **critical** for deploying to the Apple App Store.

#### the short version
1. Install XCode
2. Install XCode command line tools: `$ xcode-select --install`
3. Install npm packages [ios-sim](https://www.npmjs.org/package/ios-sim) & [ios-deploy](https://www.npmjs.org/package/ios-deploy)
```
$ npm install -g ios-sim
$ npm install -g ios-deploy
```

### Android Prerequisites
[¯\_(ツ)_/¯](https://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html)

#### Basically...
1. Install [Android Studio](https://developer.android.com/studio/index.html)
2. Launch Android Studio, which will download and install A Whole Lot of Google Onto Your Computer
3. Launch the android sdk manager (on a mac it's at `$ ~/Library/Android/tools/android`), and use it to install:
  * "SDK Platform" for android-23 (AKA: Android 6.0 (API 23) -> SDK Platform)
  * "Android SDK Platform-tools (latest)
  * "Android SDK Build-tools" (latest)

Now things _should_ build.

# Building the Project
## For Mucking around
The first time you start working with this project, you'll need to create versions for ios and android.

```
$ cordova platform add ios --save
$ cordova platform add android --save
```

Beyond that, when you update the project, you can just run:

```
$ cordova build
```

Or to update the project just for iOS (or just Android), run:

```
$ cordova build ios

OR

$ cordova build android
```


## For Testing The Project
To test for the Android project, open it (`platforms/android`) in Android Studio.

Likewise for testing the iOS app, open it (`platforms/ios`) in XCode and run it in the emulator there.

There's ways to do this from the command line but `¯\_(ツ)_/¯`.
