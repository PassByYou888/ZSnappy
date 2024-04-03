# ZSnappy 

Recently, I was working on remote desktops, and my hands were sent to the community. Because desktop synchronization uses ffmpeg+mjpeg in the coding phase, a lot of people roast about it 
So, I did a simple image differencing algorithm. ZSnappy is the compression support part of this differencing 

# Windows compatibility description 

- Supports objfpc/delphi 
- Currently, only x86/x64 versions are available for pre-compiling. I've been a bit busy lately, but I will provide pre-compiled versions for various platforms such as android/ios/osx when I have free time 
- Precompiled x86/x64 requires vs2017 dependent library support 

# Linux compatibility description 

- Install the pre-compiled snappy dynamic library directly, which supports arm-v7/arm-arch-64/mips/loongson, and other versions of Linux systems 
- The Linux system I use is debian+ubuntu 

``` 
// Install the pre-compiled snappy library 
sudo apt-get install libsnappy-dev 

// Quickly search for libsnappy.so. If it can be found by whereis, ZSnappy can be used directly 
whereis libsnappy.so 

// If whereis cannot find it, it may be because the system directory is incorrect. Search the entire disk directly 
// Here, pay attention to the distinction between link and parent. Simply copy the parent to the app directory 
find / -name libsnappy.so 
``` 

# Android compatibility description 

- Currently unable to directly compile static libraries and dynamic libraries for the Android platform 
- Github is blocked and many dependencies cannot be obtained. I will make a list if it is empty 

# macos/ios compatibility description 

- mac-mini modified for windows, there is currently no system tool available for building macos/ios 
  
by.qq600585 
2024-4