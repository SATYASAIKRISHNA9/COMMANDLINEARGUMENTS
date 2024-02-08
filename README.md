# COMMANDLINEARGUMENTS
GREP, AWK, SED, gvim and other commands








## gvim commands tricky


To make default font in gvim create .gvimrc file in home directory and copy below content.


````````````````````````````````````````````
set hlsearch
set ignorecase
 
set ruler
set incsearch
set nu
set shiftwidth=2
set tabstop=2
filetype indent on
set autoindent
set cindent
 
 
syntax on
 
set guifont=Monospace\ 18
`````````````````````````````````````````````

Tricky gvim commands to use


````````````````````````````````````
To substitute multiple spaces by single space.
:%s?\s\+? ?g
To match first 2 columns and placing 2nd column first and 1st column second.
:%s?\(.*\)\s\(.*\)?\2 \2?
````````````````````````````````````






