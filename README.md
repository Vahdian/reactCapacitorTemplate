Tutorial document

Install Capacitor we need to execute the following command:

$ npm install @capacitor/core @capacitor/cli

***************
$ npx cap init –>

import { CapacitorConfig } from '@capacitor/cli';

const config: CapacitorConfig = {
 appId: 'com.example.app', → Default name
 appName: 'newportfolio', → Default name
 webDir: 'build',
 bundledWebRuntime: false,
};

export default config;

webDir -> Path to build React App
appName -> Name App

*******************

$ npx cap add android

$ npx cap add ios

$ npx cap sync

$ npm run build



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

$ npx cap sync android
$ npx cap sync ios

$ npx cap open android
$ npx cap open ios

