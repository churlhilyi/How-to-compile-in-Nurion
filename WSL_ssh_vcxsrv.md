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
            GSSAPIAuthentication no
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

3. Use __apt-get__ command to install X related apps:

            sudo apt-get install x11-apps xfonts-base xfonts-100dpi xfonts-75dpi xfonts-cyrillic
            
4. 시작 프로그램 폴더(시작 → 실행 → "shell:startup")에 Xming 단축 아이콘을 위치시켜 Windows 부팅시 자동으로 실행되도록 한다.

5. Be sure there are no net gaurd to vcxsrv. For McAfee, a. 수신 및 송신: 모든 기기에 대해 열기, b. 넷가드: 꺼짐 
Done!
