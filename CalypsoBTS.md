
# CalypsoBTS UBUNTU (20.04)

INSTALLATION BTS FOR HACKING LTE :  
As same as : 
* [shamrin](https://gist.github.com/shamrin/8b2d6c1493c70544c39e)   
* [security-bits.de](https://security-bits.de/research/cellular/lab_setup) 
### Installing all gcc
```
apt update
```
```
sudo apt-get install libboost-all-dev libusb-1.0-0-dev doxygen python3-docutils python3-mako python3-numpy python3-requests python3-ruamel.yaml python3-setuptools cmake build-essential
```
```
apt-get remove texinfo
```
```
apt-get install alsa-base alsa-oss alsa-utils oss-compat
```
```
modprobe snd-pcm-oss
```
```
modprobe snd-mixer-oss
```
apt-key adv --recv-keys --keyserver keyserver.ubuntu.com 3B4FE6ACC0B21F32 40976EAF437D05B5 
```
apt-get install gcc-9 g++-9 gcc-10 g++-10 git -y
```
Adding on last line (could be done with mousepad)
* for raspberry :  
echo "deb http://ports.ubuntu.com/ubuntu-ports xenial main restricted universe multiverse" >> /etc/apt/sources.list  
```
echo "deb http://ports.ubuntu.com/ubuntu-ports xenial main restricted universe multiverse" >> /etc/apt/sources.list  
```
* for normal computer :  
Architecture could be amd64, armel, arm64 ?"  
echo "deb [arch=amd64] http://fr.archive.ubuntu.com/ubuntu/ xenial main restricted universe multiverse" >> /etc/apt/sources.list  
```
echo "deb http://fr.archive.ubuntu.com/ubuntu/ xenial main restricted universe multiverse" >> /etc/apt/sources.list
```
```
tail -f /etc/apt/sources.list 
```
Tape ctrl+C  
```
apt update
```
```
apt-get install gcc-4.9 g++-4.9 gcc-7 g++-7 -y
```
```
sed -i '$ d' /etc/apt/sources.list
```
```
tail -f /etc/apt/sources.list 
```
Tape ctrl+C  
```
apt update
```
```
apt-get install -y build-essential libusb-1.0-0-dev libsqlite3-dev libsctp-dev libgmp-dev libx11-6 libx11-dev flex libncurses5 libdbd-sqlite3 libdbi-dev libncurses5-dev libncursesw5 libpcsclite-dev zlib1g-dev libmpc3 lemon aptitude libtinfo-dev libtool shtool autoconf git-core pkg-config make libmpfr-dev libmpc-dev libtalloc-dev libfftw3-dev libgnutls28-dev libtool-bin libxml2-dev sofia-sip-bin libsofia-sip-ua-dev sofia-sip-bin libncursesw5-dev bison libgmp3-dev alsa-oss
```
```
update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-4.9 49 --slave /usr/bin/g++ g++ /usr/bin/g++-4.9
```
```
update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-7 70 --slave /usr/bin/g++ g++ /usr/bin/g++-7
```
```
update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-9 90 --slave /usr/bin/g++ g++ /usr/bin/g++-9
```
```
update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-10 100 --slave /usr/bin/g++ g++ /usr/bin/g++-10
```

Adding on last line (could be done with mousepad):  
* for raspberry : 
```
echo "deb http://ports.ubuntu.com/ubuntu-ports bionic main restricted universe multiverse" >> /etc/apt/sources.list    
```
* for normal computer :  
deb [arch=amd64] http://fr.archive.ubuntu.com/ubuntu/ bionic main restricted universe multiverse" >> /etc/apt/sources.list  
```
echo "deb http://fr.archive.ubuntu.com/ubuntu/ bionic main restricted universe multiverse" >> /etc/apt/sources.list
```
```
tail -f /etc/apt/sources.list
```
Tape ctrl+C
```
apt update
```
```
apt-get install -y gcc-5 g++-5 libssl1.0-dev
```
```
update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-5 50 --slave /usr/bin/g++ g++ /usr/bin/g++-5
```
```
sed -i '$ d' /etc/apt/sources.list
```
```
tail -f /etc/apt/sources.list
```
Tape ctrl+C
```
apt  update
```
```
update-alternatives --set gcc /usr/bin/gcc-4.9
```
```
gcc --version
```
All deb files in : /var/cache/apt/archives/
### Installing gnuarm
```
cd src && mkdir nitb && cd nitb
```
```
wget http://ftp.gnu.org/gnu/texinfo/texinfo-4.13.tar.gz 
```
```
tar xvf texinfo-4.13.tar.gz
```
```
mv texinfo-4.13.tar.gz ../../Desktop/ltehack_backup/
```
```
cd texinfo-4.13
```
* for raspberry :
```
./configure --build=aarch64-unknown-linux-gnu
```
* for normal computer : 
```
./configure
```
```
make 
```
```
make  install && ldconfig
```
```
cd ..
```

Download GNU_ARM_FOR UBUNTU IN :  
[gnuarm](https://drive.google.com/file/d/1xV3RLZg3Lm4m3UPd1nDfO_xEjIH2F5lQ/view?usp=share_link)  
[wget and drive](https://medium.com/@acpanjan/download-google-drive-files-using-wget-3c2c025a8b99)
```
wget --load-cookies /tmp/cookies.txt "https://docs.google.com/uc?export=download&confirm=$(wget --quiet --save-cookies /tmp/cookies.txt --keep-session-cookies --no-check-certificate 'https://docs.google.com/uc?export=download&id=1xV3RLZg3Lm4m3UPd1nDfO_xEjIH2F5lQ' -O- | sed -rn 's/.*confirm=([0-9A-Za-z_]+).*/\1\n/p')&id=1xV3RLZg3Lm4m3UPd1nDfO_xEjIH2F5lQ" -O gnuarm2_for_ubuntu.zip  && rm -rf /tmp/cookies.txt
```
```
unzip gnuarm2_for_ubuntu.zip
```
```
mv gnuarm2_for_ubuntu.zip ../../Desktop/ltehack_backup/
```
```
cd gnuarm
```
```
chmod +x gnu-arm-build.2.sh
```
```
bash gnu-arm-build.2.sh
``` 
CLICK ENTER  
Some times, compilation could take 5H,wait and drink some beer:  

make[1]: Leaving directory '/root/Desktop/karli/gnuarm/build/gcc-4.5.2'  
Build complete!  
Add /root/Desktop/karli/gnuarm/install/bin to your PATH  
to make arm-elf-gcc and friends
```
cd ../../..
```
Exporting path and addin this on bashrc
/home/ltehack/src/nitb/gnuarm/install/bin
```
export PATH=$PATH:src/nitb/gnuarm/install/bin
```
Error 1 if no gnuarm export :  
/usr/include/newlib/sys/_stdint.h:48:20: error: conflicting types for 'uint32_t'
   48 | typedef __uint32_t uint32_t ;

Error 2 if no gnuarm export :  
fatal error: sys/_types.h: No such file or directory  

```
apt-get install zip
```
```
update-alternatives --set gcc /usr/bin/gcc-9
```
Verifying gcc version :
```
gcc --version
```
```
cd src/ltehack_backup
```
### Installing libosmocore
```
git clone https://github.com/osmocom/libosmocore
```
```
cd libosmocore
```
```
git checkout cf70aa0c40c574c32b832454f725cc37459c5d8d
```
```
cd .. && zip -r libosmocore_karly.zip libosmocore/ && mv libosmocore_karly.zip ../../Desktop/ltehack_backup/
```
```
cd libosmocore && autoreconf -i 
```
```
./configure
```
```
make 
```
```
make install 
```
```
ldconfig -i 
```
```
cd ..
```
### Changing to python 2
```
apt-get install python2
```
```
sudo ln -s /usr/bin/python2 /usr/bin/python
```
### Installing osmocombb
```
git clone https://github.com/osmocom/osmocom-bb
```
```
cd osmocom-bb/
```
```
git checkout 4f677e6ba8434dab376495cd996d140548fa6e93
```

Adding on file using mousepad src/target/firmware/Makefile  
*|					#uncomment CFLAGS += -DCONFIG_TX_ENABLE	|*

```
cd src
```
```
sed -i -e  's/#CFLAGS += -DCONFIG_TX_ENABLE/CFLAGS += -DCONFIG_TX_ENABLE/g' target/firmware/Makefile
```
```
tail -f target/firmware/Makefile
```
Tape ctrl+C
```
cd ../..
```
```
zip -r osmocom-bb_karly4f677.zip osmocom-bb/
```
```
mv osmocom-bb_karly4f677.zip ../../Desktop/ltehack_backup/
```
```
cd osmocom-bb/src 
```
```
make  
```
```
cd ../..
```
### Installing libosmo-dsp
```
git clone https://github.com/osmocom/libosmo-dsp
```
```
cd libosmo-dsp
```
```
git checkout 551b9752bcd5d3d21bb2df0736b1801bda3d0d10
```
```
cd ..
```
```
zip -r libosmo-dsp_karly.zip libosmo-dsp
```
```
mv libosmo-dsp_karly.zip ../../Desktop/ltehack_backup/
```
```
cd libosmo-dsp/
```
```
autoreconf -i
```
```
./configure 
```
```
make 
```
```
make install 
```
```
ldconfig -i
```
```
cd ..
```
### Changing to gcc-5 
```
update-alternatives --set gcc /usr/bin/gcc-5
```
Verifying version : 
```
gcc --version
```
### Installing TRX
```
git clone https://github.com/osmocom/osmocom-bb trx
```
```
cd trx
```
git checkout 620fe497efa492feff4550e336cc3f8167715936
```
git checkout jolly/testing
```
```
cd src
```
wget https://github.com/bbaranoff/telco_install_sh/raw/main/trx.highram.bin
```
sed -i -e  's/#CFLAGS += -DCONFIG_TX_ENABLE/CFLAGS += -DCONFIG_TX_ENABLE/g' target/firmware/Makefile
```
```
tail -f target/firmware/Makefile
```
```
cd ../..
```
```
zip -r trx_for_ubuntu.zip trx/
```
```
mv trx_for_ubuntu.zip ../../Desktop/ltehack_backup/
```
```
cd trx/src
```
```
make  HOST_layer23_CONFARGS=--enable-transceiver 
```
```
find -name trx.highram.bin
```
This file trx.highram.bin should be appears
```
cd ../..
```
IF DEBIAN :  
apt-get install gcc gcc-arm-none-eabi  
git clone https://github.com/osmocom/osmocom-bb trx2  
cd trx2  
git checkout jolly/testing  
or git checkout 620fe497efa492feff4550e336cc3f8167715936  
cd src  
wget https://github.com/bbaranoff/telco_install_sh/raw/main/trx.highram.bin  
sed -i -e  's/#CFLAGS += -DCONFIG_TX_ENABLE/CFLAGS += -DCONFIG_TX_ENABLE/g' target/firmware/Makefile  
tail -f target/firmware/Makefile  
cd ../..  
zip -r trx2_for_ubuntu.zip trx2/  
cd trx2/src  
make HOST_layer23_CONFARGS=--enable-transceiver -e CROSS_TOOL_PREFIX=arm-none-eabi-  

find -name trx.highram.bin  
cd ../..  

### Changing to python 3
```
apt-get install python3
```
```
rm -rf /usr/bin/python
```
```
sudo ln -s /usr/bin/python2 /usr/bin/python
```

### Installing asterisk dependancies
```
apt-get install libortp-dev
```
```
apt-get install dahdi-source  
```
```
apt-get install libtool shtool automake dahdi-source libssl-dev sqlite3 libsqlite3-dev libsctp-dev libfftw3-dev libfftw3-3 autoconf libsctp-dev libgnutls28-dev libcurl4-gnutls-dev git-core pkg-config make doxygen libtalloc-dev libpcsclite-dev libusb-1.0-0-dev
```
### Changing to gcc-9
```
update-alternatives --set gcc /usr/bin/gcc-9
```
Verifying version : 
```
gcc --version
```
