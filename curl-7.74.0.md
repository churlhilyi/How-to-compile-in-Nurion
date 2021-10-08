## curl-7.74.0

1. Use __wget__ command:

            wget https://curl.haxx.se/download/curl-7.74.0.tar.xz

2. Use __tar -xvf__ command:

            tar -xvf curl-7.74.0.tar.xz

3. __Install__ it locally:

            ./configure --prefix=/pwd

            make all prefix=/pwd

            make install prefix=/pwd

3. Add __PATH__ to your .bashrc:

            export PATH=$PATH:/pwd/bin

4. Use __source__ command:

            source ~/.bashrc
            

-------------------------------
## or note: 

안녕하세요,
사용자 지원팀입니다.

curl 과 같은 라이브러리의 경우, /apps/common 디렉터리에 설치가 되어 있으며
아래 예시와 같이 환경설정 가능합니다.

[참고]
-누리온 사용법 (https://www.ksc.re.kr/gsjw/jcs/hd) > [별첨6] 공통라이브러리 목록

$ ls /apps/common/curl/7.59.0/


bin include lib share

[예시]

                        $ export LD_LIBRARY_PATH=/apps/common/curl/7.59.0/lib:$LD_LIBRARY_PATH
                        
                        $ export LDFLAGS="-L/apps/common/curl/7.59.0/lib -lcurl"
                        
                        $ export CPPFLAGS="-I/apps/common/curl/7.59.0/include"

예시를 참고하시어 curl 경로를 설정하여 설치 진행해보시기 바라며
설치 시 오류가 발생하는 경우, 현재 문의와 같이 오류내용, 설치과정 등을 적어 문의 부탁드립니다.

감사합니다.

----------------------------------

Done!
