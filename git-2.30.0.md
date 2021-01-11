## git-2.30.0

First, make sure you have already installed 'curl' at Nurion. 

Then,

1. Use  'wget' command to download the source file : 

        wget https://www.kernel.org/pub/software/scm/git/git-2.30.0.tar.gz

2. Use  'tar -xvzf' command :

        tar -xvzf git-2.30.0.tar.gz

3. Install it locally :

        make prefix=/pwd
        make install prefix=/pwd

4. Add PATH to your .bashrc:

        export PATH=$PATH:/pwd/bin

5. Use source command:

        source ~/.bashrc
        
Done!
