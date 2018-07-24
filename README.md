# Phonegap + Cordova + IP WebCamera
This code demonstrates IP Web Camera Viewing using Phonegap and Cordova

### Setup Requirements

* Environment Variables
  * ANDROID_HOME=C:\Users\UIC\AppData\Local\Android\Sdk
  * JAVA_HOME=C:\Program Files\Java\jdk1.8.0_144
* NodeJS and Git

### Terminal

```bash
$ node --version
v8.9.3
$ git --version
git version 2.18.0.windows.1
$ npm install cordova phonegap@latest
$ phonegap create pgipcam --template framework7
$ cd pgipcam
$ cordova platforn add android
$ cordova plugin add cordova-plugin-inappbrowser
$ cordova plugin add cordova-plugin-whitelist
$ cordova build android --verbose
$ cordova run android --target=RQ30004JQ69
```

### Source Codes

```javascript
var ip = '192.168.1.6';
var url = 'http://'+ip+'/videostream.cgi?user=admin&pwd=';
var target = '_blank';
var settings = 'location=no';
cordova.InAppBrowser.open(url, target, settings);    
```