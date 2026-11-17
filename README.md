# 下班捉鬼 — PICO VibeLab Android export

Standalone Android Gradle project exported from Unity 6000.6.7f1.
Package: `com.ghostprototype.picoghost`; version: `0.63` (code `63`).
Target ABI: `arm64-v8a`; minimum SDK: 29; target/compile SDK: 36.

The release IL2CPP library is compiled locally and included in
`unityLibrary/src/main/jniLibs/arm64-v8a/libil2cpp.so`.
Cloud builds do not invoke Unity or compile IL2CPP.
The CMake task builds only Unity's Android frame-pacing glue.

Use JDK 17, Android SDK 36 / build tools 36.0.0, NDK 27.2.12479018
and CMake 3.22.1. Run `./gradlew :launcher:assembleRelease`.
The only release APK is `launcher/build/outputs/apk/release/launcher-release.apk`.

Unity-generated local tool paths are retained for VibeLab's path adaptation.
For a local build, provide SDK location through local configuration.
Signing remains the Unity template's debug signing; no private signing key,
keystore, local SDK configuration, or build cache is included in this repository.
PICO manages the distributed APK signature.

Gameplay includes gaze selection, pinch-and-swipe capture, tutorial,
normal and ultimate challenges. The custom PICO launcher icon and its
layer/SDF metadata are included in the exported resources.
