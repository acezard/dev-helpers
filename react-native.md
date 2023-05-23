# RN helpers

## Hack `run-android`

In `/home/anc/cozy/cozy-react-native/node_modules/@react-native-community/cli-platform-android/build/commands/runAndroid/index.js`

 ```
    // "app" is usually the default value for Android apps with only 1 app
    //const {
    //  appName,
    //  sourceDir
    //} = androidProject;
    //const {
    //  appFolder
    //} = args;
    //const variant = args.variant.toLowerCase();
    //const buildDirectory = `${sourceDir}/${appName}/build/outputs/apk/${variant}`;
    //const apkFile = getInstallApkName(appFolder || appName, // TODO: remove appFolder
    //adbPath, variant, device, buildDirectory);
    const pathToApk = `/home/anc/cozy/cozy-react-native/android/app/build/outputs/apk/dev/debug/app-dev-x86-debug.apk`;
    const adbArgs = ['-s', device, 'install', '-r', '-d', pathToApk];
```
