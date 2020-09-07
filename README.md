# ReactNativeForkWindowsBuildBug

This is an empty react-native 0.63.2 project, the only change is to reference a fork of react-native per the documentation here https://github.com/facebook/react-native/wiki/Building-from-source

This will fail to build on windows with the following error because the react-native build scrips are generating invalid paths.

```
make: Leaving directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
make: Entering directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
[armeabi-v7a] SharedLibrary  : libjsinspector.so
make: Leaving directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
C:/dev/tools/AndroidSDK/ndk/21.0.6113669/build//../toolchains/llvm/prebuilt/windows-x86_64/bin/../lib/gcc/arm-linux-androideabi/4.9.x/../../../../arm-linux-androideabi/bin\ld: error: cannot open C:\dev\ReactNativeForkWindowsBuildBug\node_modules\react-native\ReactAndroid\build\tmp\buildReactNdkLib/local/armeabi-v7a/objs/jsinspector/C_/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/__/ReactCommon/jsinspector/InspectorInterfaces.o: No such file
 or directory
clang++: error: linker command failed with exit code 1 (use -v to see invocation)
make: *** [C:/dev/tools/AndroidSDK/ndk/21.0.6113669/build//../build/core/build-binary.mk:725: C:\dev\ReactNativeForkWindowsBuildBug\node_modules\react-native\ReactAndroid\build\tmp\buildReactNdkLib/local/armeabi-v7a/libjsinspector.so] Error 1
make: *** Waiting for unfinished jobs....
make: Entering directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
[armeabi-v7a] SharedLibrary  : libfb.so
make: Leaving directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
make: Entering directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
[armeabi-v7a] StaticLibrary  : libdouble-conversion.a
make: Leaving directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
make: Entering directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
[armeabi-v7a] StaticLibrary  : libjsi.a
make: Leaving directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
make: Entering directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
[armeabi-v7a] SharedLibrary  : libglog.so
make: Leaving directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
make: Entering directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
[x86_64] Compile++      : jsijniprofiler <= HermesSamplingProfiler.cpp
make: Leaving directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
make: Entering directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
[x86_64] Compile++      : reactnativeblob <= OnLoad.cpp
make: Leaving directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
make: Entering directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
[x86_64] Compile++      : hermes-executor-release <= HermesExecutorFactory.cpp
make: Leaving directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
make: Entering directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
[x86_64] Compile++      : reactnativeblob <= BlobCollector.cpp
make: Leaving directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
make: Entering directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
[x86_64] Compile++      : reactnative <= NativeToJsBridge.cpp
make: Leaving directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
make: Entering directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
[x86_64] Compile++      : jscruntime <= JSCRuntime.cpp
make: Leaving directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
make: Entering directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
[x86_64] Compile++      : reactnative <= CxxNativeModule.cpp
make: Leaving directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
make: Entering directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
[x86_64] Compile++      : hermes-executor-release <= OnLoad.cpp
make: Leaving directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
make: Entering directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
[x86_64] Compile++      : jscexecutor <= OnLoad.cpp
make: Leaving directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
make: Entering directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
[x86_64] Compile++      : jsireact <= JSIExecutor.cpp
make: Leaving directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
make: Entering directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'
[x86_64] Compile++      : reactnative <= SampleCxxModule.cpp
make: Leaving directory 'C:/dev/ReactNativeForkWindowsBuildBug/node_modules/react-native/ReactAndroid/src/main/jni/react/jni'

```
