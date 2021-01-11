Use 'wget' command:

wget https://curl.haxx.se/download/curl-7.74.0.tar.xz

Use 'tar -xvf' command:

tar -xvf curl-7.74.0.tar.xz

Install it locally:

./configure --prefix=/pwd

make all prefix=/pwd

make install prefix=/pwd

Add PATH to your .bashrc:

export PATH=$PATH:/pwd

Use source command:

source ~/.bashrc

Done!
