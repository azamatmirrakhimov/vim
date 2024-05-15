# Что бы не искать что делать 
## 1. Надоперейти в директорию vim/src

~~~
apt install make clang libtool-bin -y
~~~

~~~
make
~~~
~~~~
make install
~~~~
## Потом для чуть чуть обновим  vim если версия все еще не изменилось просто выйдейти зайдите все должно измениться 

~~~
vim ~/.vimrc
~~~
## Создали файл vimrc и там надо будет написать конфиг для удобство 
~~~
" Initialize Vim-Plug plugin manager
call plug#begin('~/.vim/plugged')

" Add vim-go plugin
Plug 'fatih/vim-go'

" End the plugin section
call plug#end()

" Enable file type detection and plugins
filetype plugin indent on

" Basic Vim settings
set number             " Show line numbers
set noswapfile         " Disable swap file
set noshowmode         " Do not show mode in command line
set tabstop=2          " Number of spaces tabs count for
set shiftwidth=2       " Number of spaces for indentation
set softtabstop=2      " Number of spaces for <Tab> in insert mode
set expandtab          " Use spaces instead of tabs
set backspace=indent,eol,start " Make backspace behave more naturally

" Map <leader> to comma
let mapleader=","      " Corrected from maplead to mapleader

" Go file specific settings
if has("autocmd")
  autocmd FileType go setlocal tabstop=2 shiftwidth=2 softtabstop=2 noexpandtab nolist autowrite
endif
~~~~
