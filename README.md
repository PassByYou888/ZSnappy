# ZSnappy

这是google体系中的高速压缩算法:snappy for pascal.

# 起源

最近在弄远程桌面,手贱发到社区,因为桌面同步在编码环节使用了ffmpeg+mjpeg,被一大堆人吐槽.

于是,顺手做了一个图片差分算法.Snappy是这个差分的压缩支持部分.单独剥离以后避免同名,就以ZSnappy命名.

# windows兼容性说明

- 支持objfpc/delphi
- 目前预编译只有x86/x64两个版本,最近有点忙,空下来会给出android/ios/osx各个平台的预编版本
- 预编译的x86/x64需要vs2017依赖库支持

# linux兼容性说明

- 直接安装预编译好的snappy动态库,可以支持arm-v7/arm-arch-64/mips/龙芯,等等版本linux系统
- 我所使用的Linux系统为debian+ubuntu

```
// 安装预编译snappy库
sudo apt-get install libsnappy-dev

// 快速搜索libsnappy.so,只要whereis可以找到,那么ZSnappy就能直接使用
whereis libsnappy.so

// 如果whereis找不到,可能是系统目录错了,直接全盘搜
// 这里注意区分link和母体,直接把母体copy到app目录即可
find / -name libsnappy.so
```

# android兼容性说明

- 暂时无法直接编译出android平台的静态库+动态库
- github被封锁断网,很多依赖项无法get,空了会拉下来编一下

# macos/ios兼容性说明

- mac-mini改装windows,暂时没有可以构建macos/ios的系统工具

 
by.qq600585

2024-4
