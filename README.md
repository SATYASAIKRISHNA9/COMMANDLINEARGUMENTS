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
-->  :%s?\s\+? ?g
To match first 2 columns and placing 2nd column first and 1st column second.
-->  :%s?\(.*\)\s\(.*\)?\2 \2?
````````````````````````````````````











## AWK COMMANDS


```````````````````````````````````````````````````````````````
1st part -- Below command will fetch lines from line number 65 to line number 312 from file file_name.txt and prints only 2nd, 22nd and 24th column.
2nd part -- It will grep words and invert match of "0"
3rd part -- Gives the lines which are not beginning with space.

-->  awk 'NR==65, NR==312 {print $2,$22,$24}' file_name.txt| grep -w -v "0" | grep -v "^\s"
 
if we want to print only 3rd column.

-->  awk '{print $3}'

I wanna grep from one file which is csv then i need to use field separator and prints 2nd column.

-->  grep "pattern1" | awk -F ',' '{print $2}'




``````````````````````````````````````````````````````````````````


















## GREP COMMANDS


``````````````````````````````````````````````````````
if we want to grep different patterns at a time we can use below command.

-->  grep -E "pattern1|pattern2"

``````````````````````````````````````````````````````






















## SED COMMANDS


```````````````````````````````````````````````````````````
I want to fetch few lines between pattern1 and pattern2. We are redirecting it to file so console will not be messy and we can do our requirements from file.

-->  sed -n '/pattern1/,/pattern2/p' file_name > new_file.txt


```````````````````````````````````````````````````````````
