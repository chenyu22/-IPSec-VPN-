配置
1、linux 18.06 
2、安装gtk+3环境
3、安装glade
4、安装必须的库  libpam0g-dev libssl-dev make gcc
5、解压、配置
./configure --enable-eap-identity --enable-eap-md5 --enable-eap-mschapv2 --enable-eap-tls --enable-eap-ttls --enable-eap-peap --enable-eap-tnc --enable-eap-dynamic --enable-eap-radius --enable-xauth-eap --enable-xauth-pam  --enable-dhcp  --enable-openssl  --enable-addrblock --enable-unity --enable-certexpire --enable-radattr --enable-swanctl --enable-openssl  --disable-gmp --enable-save-keys  --enable-vici  --enable-save-keys
6、编译、安装
make
make install
7、编译guimain
gcc -Wall -g -o guimain guimain.c `pkg-config --cflags --libs gtk+-3.0` -export-dynamic -L/usr/local/lib/ipsec  -lvici
8、安装完成，运行guimain即可