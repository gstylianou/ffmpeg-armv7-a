# ffmpeg-armv7-a
How to build ffmpeg for 32 bit armv7-a.

Instructions:
1. Download the latest android NDK from here: https://developer.android.com/ndk/downloads/index.html. The android NDK used here was version r15b.
2. Download ffmpeg source code from here: https://ffmpeg.org/download.html. The ffmpeg build in the project used ffmpeg version 3.3. Extract the code in the folder sources of the android NDK.
3. Use the provided build_android.sh. We used this succesfully under Mac OS X. We believe it should be okay under linux. You might need to do changes in the following lines: 
   NDK=$HOME/Desktop/android-ndk-r15b   This is the path android NDK was extracted to. Make the necessary changes if you extracted it in a different path.
   SYSROOT=$NDK/platforms/android-16/arch-arm/   This is the path for 32 bit platform.
   TOOLCHAIN=$NDK/toolchains/arm-linux-androideabi-4.9/prebuilt/darwin-x86_64  This is the path of the compilers for the 32 bit armv7-a. 
   
Note that the file build_android.sh is stored in the ffmpeg folder which is in the path ..sources/FFmpeg.   
For your convenience, we also provide the binary file ffmpeg.


