## ubuntu 16.04安装R-base过程

1. 下载源代码文件;
2. 解压缩: tar -zxf R-x.x.x.tar.gz
3. 预编译: ./configure --prefix=/home/user/program/R-3.x.x --enable-R-shlib
4. 出错: configure: error: No F77 compiler found
5. 安装gfortran: sudo apt-get install gfortran
6. 预编译再次出错: configure: error: --with-readline=yes (default) and headers/libs are not available
7. 安装依赖包: sudo apt-get install libreadline6-dev libxt-dev
8. 预编译出现很多warning，需要安装依赖包: sudo apt-get install texinfo texlive
