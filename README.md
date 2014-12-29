openwrt
=======
我是在UBUNTU环境下编译的，怎么安装就省略了，直接开始吧。老鸟勿喷
首先是
sudo apt-get install gcc g++ binutils patch bzip2 flex bison make autoconf gettext texinfo unzip sharutils subversion libncurses5-dev ncurses-term zlib1g-dev openssl libssl-dev gawk qemu vim

可能make menuconfig的时候提示缺少AWK的时候，可以这样sudo apt-get install gawk

建立工作目录 工作目录随意命名
sudo mkdir openwrt
设置权限
Sudo chmod 777 -R openwrt
切换到工作目录
cd openwrt

然后是下载源码

TRUNK版的是
svn checkout svn://svn.openwrt.org/openwrt/trunk 
cd trunk 
./scripts/feeds update -a 
./scripts/feeds install -a 

DREAMBOX版的是
svn co svn://svn.openwrt.org.cn/dreambox/backfire openwrt-dreambox
cd openwrt-dreambox
./scripts/feeds update -a 
./scripts/feeds install -a

之后初始化配置
make defconfig

make 界面

make menuconfig

第一次不要选着什么config直接选择型号
Save 后

Make V=99
为了减小第一次的时间 还有确定有没有出错eeror

Openwrt 资源网站http://www.openwrt.org.cn/bbs/thread-7121-1-1.html
所需编译软件 http://downloads.openwrt.org.cn/sources/
Openwrt 编译教程贴 http://www.openwrt.org.cn/bbs/thread-60-1-1.html
