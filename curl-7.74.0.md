## curl-7.74.0

1. Use __wget__ command:

            wget https://curl.haxx.se/download/curl-7.74.0.tar.xz

2. Use __tar -xvf__ command:

            tar -xvf curl-7.74.0.tar.xz

3. Install it locally:

            ./configure --prefix=/pwd

            make all prefix=/pwd

            make install prefix=/pwd

3. Add __PATH__ to your .bashrc:

            export PATH=$PATH:/pwd/bin

4. Use __source__ command:

            source ~/.bashrc
            

Done!
