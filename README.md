# react-native-common-errors
react-native-common-errors

# Enabling Multidex
### Learn how to enable multidex on your Android application.

As more native dependencies are added to your project, it may bump you over the 64k 
method limit on the Android build system. Once this limit has been reached, you will start to see the following 
error whilst attempting to build your Android application:

```bash 
Execution failed for task ':app:mergeDexDebug'.
```
```shell
defaultConfig {
    applicationId "com.example.poll"
    minSdkVersion 16
    targetSdkVersion 28
    versionCode flutterVersionCode.toInteger()
    versionName flutterVersionName
    testInstrumentationRunner "androidx.test.runner.AndroidJUnitRunner"
    //This line here...
+    multiDexEnabled true
}
```
