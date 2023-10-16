# bgfx-android-examples
This is a simple base Android application harness to allow the running of the BGFX examples. The project can also be used as a basis to port any existing BGFX code to Android. The actual Android project is based upon the NDK example app for the native-activity as described here,

https://developer.android.com/ndk/samples/sample_na

## Build instructions

This project will assume you're on a Linux based host. Firstly clone the repository using the following command,

### Prequisites

Make sure you have SDK and NDK environment variables set correctly. It'll looks omething like this,

`export ANDROID_SDK_ROOT=~/Android/Sdk`

`export ANDROID_NDK_ROOT=~/Android/Sdk/ndk/25.1.8937393`

Clone the repo using,

`git clone --recurse-submodules https://github.com/gsfare/bgfx-android-examples.git`

### Build BGFX dependencies.

`cd bgfx-android-example/bgfx`
`make android-arm64`

### Build the Android app.

`cd bgfx-android-example/native-activity`
`./gradlew assembleDebug`

Install as usual!
