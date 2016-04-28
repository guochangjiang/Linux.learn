## ubuntu 16.04安装R-base过程

此方法适用于自己从头由R-base源代码进行R的安装，简单的话可以直接由sudo apt-get install r-base进行安装，但是版本可能比较落后。

> 参考: http://www.linuxidc.com/Linux/2015-04/115790.htm

1. 下载源代码文件;
2. 解压缩: tar -zxf R-x.x.x.tar.gz
3. 预编译: ./configure --prefix=/home/user/program/R-3.x.x --enable-R-shlib
4. 出错: configure: error: No F77 compiler found
5. 安装gfortran: sudo apt-get install gfortran
6. 预编译再次出错: configure: error: --with-readline=yes (default) and headers/libs are not available
7. 安装依赖包: sudo apt-get install libreadline6-dev libxt-dev
8. 预编译出现很多warning，需要安装依赖包: sudo apt-get install texinfo texlive
9. 下载并安装inconsolata: sudo cp -r ./inconsolata /usr/share/texlive/texmf-dist/tex
10. 刷新一下 sty: sudo mktexlsr
11. 再次进行预编译，应该就成功了。
12. 安装: sudo make && make install

