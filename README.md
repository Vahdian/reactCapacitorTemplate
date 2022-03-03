Tutorial document

Install Capacitor we need to execute the following command:

$ npm install @capacitor/core @capacitor/cli

*****************************************************************************************
$ npx cap init –>

import { CapacitorConfig } from '@capacitor/cli';

const config: CapacitorConfig = {
 appId: 'com.example.app', → Default name
 appName: 'newportfolio', → Default name
 webDir: 'build',
 bundledWebRuntime: false,
};

export default config;

webDir -> React App Path “./build”
appName -> Name App

*******************
$ npm install @capacitor/android
$ npx cap add android

$ npm install @capacitor/ios
$ npx cap add ios

$ npm run build

$ npx cap sync

*****************************************************************************************

The file AndroidManifest.xml can be found at this path:

android/app/src/main/AndroidManifest.xml

Include the following:
android:usesCleartextTraffic="true"

   <application
       android:usesCleartextTraffic="true"
       android:allowBackup="true"
       android:icon="@mipmap/ic_launcher"
       android:label="@string/app_name"
       android:roundIcon="@mipmap/ic_launcher_round"
       android:supportsRtl="true"
       android:theme="@style/AppTheme">

*****************************************************************************************

$ npx cap sync android
$ npx cap sync ios

$ npx cap open android
$ npx cap open ios


*****************************************************************************************


How to generate .APK or .AAB using Android Studio:

Open Android Studio
Build
Build Bundle(s) / APK(s)

To generate .APK click on Build APK(s)
To generate .AAB click on Build Bundle(s)

When the Build is over, click in locate to open the path where it was generated.

Or go to your React/Angular project found at this path:

APK: android/app/build/outputs/apk/debug/app-debug.apk

AAB: android/app/build/outputs/bundle/debug/app-debug.aab
