# NDK Command Line App

## Add Android SDK tools to your PATH
```
export PATH=$PATH:/path/to/Android/Sdk/platform-tools/
```

## Add Android NDK to your PATH
```
export PATH=$PATH:/path/to/android-ndk/
```

## Setup NDK_PROJECT_PATH
```
export NDK_PROJECT_PATH=.
```

## Clean Build
```
ndk-build NDK_APPLICATION_MK=./Application.mk clean
```

## Build App
```
ndk-build NDK_APPLICATION_MK=./Application.mk
```

## Transfer compiled app to Android device
```
adb connect ANDROID_IP_HERE
adb push ./libs/armeabi-v7a/main.out /data/local/tmp/

adb shell
/data/local/tmp/main.out
```

## NDK Reference

ABI | Supported Instruction Sets
----|------------------------------------------------------
armeabi-v7a | armeabi, Thumb-2, VFPv3-D16
arm64-v8a   | AArch64
x86         | x86, MMX, SSE/2/3, SSSE3
x86_64      | x86-64, MMX, SSE/2/3, SSSE3, SSE4.1, SSE4.2, POPCNT
all         | build for all ABI's

Note: The NDK supported ARMv5 (armeabi), and 32-bit and 64-bit MIPS, but support for these ABIs was removed in NDK r17.

https://developer.android.com/ndk/guides/ndk-build

https://developer.android.com/ndk/guides/android_mk

https://developer.android.com/ndk/guides/application_mk

https://developer.android.com/ndk/guides/cpp-support

https://developer.android.com/ndk/guides/abis
