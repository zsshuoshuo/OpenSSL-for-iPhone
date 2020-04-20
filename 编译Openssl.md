# 编译Openssl
>  参考资料：https://www.jianshu.com/p/1d6ed8ec18ef
> https://github.com/x2on/OpenSSL-for-iPhone.git
## macOS版本(10.15.4 (19E287)
1. cd到目录，运行./build-libssl.sh --targets="ios-sim-cross-x86_64" 编译模拟器版本 注意可以用--version=1.0.2来指定版本
2. 拷贝出来lib文件夹
3. 运行./build-libssl.sh --targets="mac-catalyst-x86_64 ios64-cross-arm64 ios64-cross-arm64e" 编译真机和maccatalyst版本 拷贝include和lib文件夹
4. 注意用真机版本的include来生成xcframework
5. 注意：/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX10.15.4.sdk 由于这个目录是不存在的，所以在系统中手动拷贝了一份