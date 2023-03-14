## fzf_vim

1. __Install vim-plug__:

2. __Install fzf__ by using vim-plug :

            call plug#begin('~/.vim/plugged')
            Plug 'junegunn/fzf', { 'do': { -> fzf#install() } }
            Plug 'junegunn/fzf.vim'
            call plug#end()

3. __Use key bindings__ to use ctrl + r command at bash:

            cd ~/.vim/plugged/fzf
            ./install
    
Done!
