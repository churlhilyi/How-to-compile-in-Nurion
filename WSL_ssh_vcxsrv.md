## WSL_ssh_vcxsrv.md

### for __ssh__ :
1. Use __apt-get__ command to upate ssh:

            sudo apt-get update
            sudo apt-get upgrade
            sudo apt-get purge openssh-server
            sudo apt-get install openssh-server

2. Modify __ssh_config__ file:

            ForwardAgent yes
            ForwardX11 yes
            ForwardX11Trusted yes
            PasswordAuthentication yes
            XAuthLocation /bin/xauth
            
3. Set __alias__ in ~/.bashrc:

            alias nurion='ssh -X x2204a04@nurion.ksc.re.kr -p 22'

### for ___windows terminal___
1. set default profile to Ubuntu
2. add "cd" to /.basrc

### for ___vcxsrv___ :
1. Download & run the Installation file:

            go https://sourceforge.net/projects/vcxsrv/
            install it
            run it and check "Disable access control"
            add "-ac" to Additional parameters for VcXsrv

2. Add the following lines to ~/.bashrc file : 

            export DISPLAY="`grep nameserver /etc/resolv.conf | sed 's/nameserver //'`:0"
            export LIBGL_ALWAYS_INDIRECT=1

Done!
