## vim82

1. Download the source file by using __git clone__ command:

            git clone https://github.com/vim/vim.git

2. Install it by typing __make__ command:

            ./configure --prefix=/home01/x2204a04/software/vim LDFLAGS="-L/apps/common/ncurses/6.1/lib"
            make -j 8
            make install
            (if some error is occured, use gfortran compiler)
            
3. Add 'export' to the .bashrc file 

Done!
