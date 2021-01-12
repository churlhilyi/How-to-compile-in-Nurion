## git-2.30.0

First, make sure you have already installed ___curl___ at Nurion. 

Then,

1. Use  __wget__ command to download the source file: 

        $ wget https://www.kernel.org/pub/software/scm/git/git-2.30.0.tar.gz

2. Use  __tar -xvzf__ command:

        $ tar -xvzf git-2.30.0.tar.gz

3. __Install__ it locally:

        $ make prefix=/pwd
        $ make install prefix=/pwd

4. Add __PATH__ to your .bashrc:

        $ export PATH=$PATH:/pwd/bin

5. Use __source__ command:

        $ source ~/.bashrc
        

Done!

-------------------------

For the ssh connection,
1. Add __config__ to ~/.ssh

        $ cat >> config
        Host github.com
                Hostname ssh.github.com
                Port 443
