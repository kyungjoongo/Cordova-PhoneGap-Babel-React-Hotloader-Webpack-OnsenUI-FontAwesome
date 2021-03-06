# Kitchensink/Boilerplate for Cordova-PhoneGap-Babel-React-Hotloader-Webpack-OnsenUI-FontAwesome
Template for ready-to-use hybrid mobile apps with native look.

## Preview
![Material](https://raw.github.com/vonubisch/Cordova-PhoneGap-Babel-React-Hotloader-Webpack-OnsenUI-FontAwesome/master/res/demo/preview-android.jpg)

## Tools
Not all are correctly implemented/configured yet.
- Apache Cordova - *to compile to iOS and Android Apps*
- Adobe PhoneGap - *some juicy Cordova tools*
- React - *DOM ninja*
- React Hotloading - *No more F5*
- Babel - *for sexy JS*
- Firestore - *store files and data*
- Webpack - *Pack it up*
- ESlint - *only pretty code*
- OnsenUI - *CSS framework native iOS/Android*
- FontAwesome - *good old icons*

## This repo is not ready, yet
Things to do:
- Add missing modules to package.json
- Make sure latest versions are used with NPM - any tool to check latest version and update?
- Find out how I can reduce size, due to later building by PhoneGap, so exclude (which) node_modules?
- Clean up webpack config ??
- Add more babel config ??
- Demo more UI stuff with OnsenUI-react

## Start application
Run via the CLI:
```
npm install
npm run start
```
Find out which modules are missing... Then a couple more:
```
npm install missing-module
```
Then a couple more tries at:
```
npm run start
```
Then open the browser at something like:
```
http://localhost:8080
```

## Build the app for production
Make sure Cordova has its platforms
```
cordova platform add android
cordova platform add ios
cordova platform add browser
```
To build the app without the hotreloader:
```
npm run build [ -- ios || android]
npm run prepare -- ios
npm run prepare -- android
```
This will switch your config.xml file to production mode, build the app bundle to `www` using Webpack and run `cordova build` for you.

Then you can run Cordova / PhoneGap like `phonegap serve` or `cordova run ios`

Now you can use the PhoneGap developer app or browser to view your app.
