## vim82

1. Download the source file by using __git clone__ command:

            git clone https://github.com/vim/vim.git

2. Install it by typing __make__ command:

            export LD_LIBRARY_PATH="$LD_LIBRARY_PATH:/apps/common/ncurses/6.1/lib"
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
            vim ~/.vimrc
            :PlugInstall 

6. for fzf settings:

            cd ~/.vim/plugged/fzf
            ./install (key-binding: on)

7. for bat:

            module purge
            curl https://sh.rustup.rs -sSf | sh
            cargo install --locked bat

8. add following env to .bashrc:

            #--------------------fzf----------------------------------
            [ -f ~/.fzf.bash ] && source ~/.fzf.bash
            export PATH="/home/.vim/plugged/fzf/bin/:$PATH"
            # Preview file content using bat (https://github.com/sharkdp/bat)
            export FZF_CTRL_T_OPTS="
              --preview 'bat -n --color=always {}'
              --bind 'ctrl-/:change-preview-window(50%|down|hidden|)'"

            # CTRL-/ to toggle small preview window to see the full command
            # CTRL-Y to copy the command into clipboard using pbcopy
            export FZF_CTRL_R_OPTS="
              --preview 'echo {}' --preview-window up:3:hidden:wrap
              --bind 'ctrl-/:toggle-preview'
              --bind 'ctrl-y:execute-silent(echo -n {2..} | pbcopy)+abort'
              --color header:italic
              --header 'Press CTRL-Y to copy command into clipboard'"

            # Print tree structure in the preview window
            export FZF_ALT_C_OPTS="--preview 'tree -C {}'"
            . "$HOME/.cargo/env"


Done!
