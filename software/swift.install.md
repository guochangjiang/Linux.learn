## 苹果公司Swift开源语言开发包的安装

+ 参考: https://swift.org/download

+ 平台: Ubuntu 16.04

### 安装过程

1. 下载对于平台的安装文件: 

> https://swift.org/builds/swift-2.2.1-release/ubuntu1510/swift-2.2.1-RELEASE/swift-2.2.1-RELEASE-ubuntu15.10.tar.gz

> https://swift.org/builds/swift-2.2.1-release/ubuntu1510/swift-2.2.1-RELEASE/swift-2.2.1-RELEASE-ubuntu15.10.tar.gz.sig

2. 安装依赖包: sudo apt-get install clang libicu-dev
3. 第一次安装需要运行
```{bash}
gpg --keyserver hkp://pool.sks-keyservers.net \
      --recv-keys \
      '7463 A81A 4B2E EA1B 551F  FBCF D441 C977 412B 37AD' \
      '1BE1 E29A 084C B305 F397  D62A 9F59 7F4D 21A5 6D5F'
# 或者
wget -q -O - https://swift.org/keys/all-keys.asc | gpg --import -
```
4. 验证: gpg --keyserver hkp://pool.sks-keyservers.net --refresh-keys Swift
5. 再验证: gpg --verify swift-<VERSION>-<PLATFORM>.tar.gz.sig
6. 解压缩安装包: tar xzf swift-<VERSION>-<PLATFORM>.tar.gz
7. 将解压缩得到的文件夹复制到安装位置，例如/home/xxx/programs/swift
8. 编辑.bashrc将/home/xxx/programs/swift/usr/bin加入环境变量
9. 运行swift，显示如下信息便成功了。

> Welcome to Swift version 2.x.x (swift-2.x.x-RELEASE). Type :help for assistance.
