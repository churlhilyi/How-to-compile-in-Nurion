## qe-6.7.0

1. Use __wget__ command:

            wget https://github.com/QEF/q-e/archive/qe-6.7.0.tar.gz

2. Use __tar -xvf__ command:

            tar -xvf qe-6.7.0.tar.gz

3. __Install__ it locally:

            ./configure --prefix=/pwd

            make -j4 all prefix=/pwd

3. Add __PATH__ to your cal_script:

            export PATH=$PATH:/pwd/bin


Done!
