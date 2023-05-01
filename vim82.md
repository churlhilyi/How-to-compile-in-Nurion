## vim82

1. Download the source file by using __git clone__ command:

            git clone https://github.com/vim/vim.git

2. Install it by typing __make__ command:

            ./configure --prefix=/home01/x2204a04/software/vim LDFLAGS="-L/apps/common/ncurses/6.1/lib"
            (./configure --prefix=/home01/x2655a03/software/vim/ CC=icc CFLAGS="-O3 -fPIC" LDFLAGS="-L/apps/common/ncurses/6.1/lib")
            make -j 8
            make install
            (If some error  occured, use gfortran compiler.)
            
3. Add 'export' to the .bashrc file 

4. Make a backup directory:
            
            mkdir ~/.vim/backup

5. For vim-plug type(git is necessary):

            curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
            https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim


Done!
