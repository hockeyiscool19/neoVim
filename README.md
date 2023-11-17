# NeoVim Setup

Welcome to my NeoVim setup. In here, I will just outline the different ways I set up my editor, the different key bindings I use, and plugins I installed. 

### Why Neovim?

Unlike other projects, where you show competency with a coding language, this repository shows a deeper understanding of the machine on which code runs. Ultimately, learning the fundamentals of the machine helps in solving internal issues when they arise, making you a more efficient programmer. Implementing this project, I show competency in Linux and Ubuntu.

### Neovim Installation and Guides

I credit ThePrimegen for inspiring this guide: ```https://www.youtube.com/watch?v=w7i4amO_zaE&t=580s```. Ultimately, however, I had more success with NeuralNine's YouTube guide: ```https://www.youtube.com/watch?v=JWReY93Vl6g```. NeuralNine had a very complete guide, that involved chosing the correct version of Linux, Ubuntu, Neovim, and Node.js. 

### Favorite Plugins

I list all the plugins below, but I would like to go over my favorite features of this setup. See nvim/init.vim for full implementation.
1. NerdTree: This plugin allows you to see your file tree by C-f.
2. Coc: Conquer of Completion allows you to do code completion, which is necessary for any developer.
3. vim Multiple Cursors: allows you do do operations on multiple lines at the same time. 

```
Plug 'http://github.com/tpope/vim-surround' 
Plug 'https://github.com/preservim/nerdtree' " NerdTree
Plug 'https://github.com/tpope/vim-commentary' " For Commenting gcc & gc
Plug 'https://github.com/vim-airline/vim-airline' " Status bar
Plug 'https://github.com/lifepillar/pgsql.vim' " PSQL Pluging needs :SQLSetType pgsql.vim
Plug 'https://github.com/ap/vim-css-color' " CSS Color Preview
Plug 'https://github.com/rafi/awesome-vim-colorschemes' " Retro Scheme
Plug 'https://github.com/ryanoasis/vim-devicons' " Developer Icons
Plug 'https://github.com/tc50cal/vim-terminal' " Vim Terminal
Plug 'https://github.com/preservim/tagbar' " Tagbar for code navigation
Plug 'https://github.com/terryma/vim-multiple-cursors' " CTRL + N for multiple cursors
Plug 'https://github.com/neoclide/coc.nvim'  " Auto Completion
Plug 'https://github.com/tpope/vim-commentary' " For Commenting gcc & gc
```

### Favorite Keybindings

1. Copy, Paste: out of the box, vim does not have copy and paste. Not using copy and paste is akin to disliking sliced bread.
2. ```C-f``` Tree: this pulls up the file tree, allowing for easy navicability.
3. ```<leader>pv```: this exits files easier than the standard command, ```:Ex```. 
My key bindings listed below. See nvim/init.vim for full implementation.

```
let mapleader = " "
" :Ex is now pv
nnoremap <leader>pv :Ex<CR>
nnoremap <leader>gh :cd /home/joeisenman/nvim/github_repos<CR>
nnoremap <C-f> :NERDTreeFocus<CR>
nnoremap <C-n> :NERDTree<CR>
nnoremap <C-t> :NERDTreeToggle<CR>
nnoremap <C-l> :call CocActionAsync('jumpDefinition')<CR>
vnoremap <C-c> "+y
nnoremap <C-v> "+p
inoremap <C-v> <Esc>"+p
inoremap <Tab> <C-y>
nmap <F8> :TagbarToggle<CR>
```

### Useful Commands

#### Linux and CLI Commands
1. ```cd```: absolutely essential Linux command for changing directory.
2. ```mkdir [directory_name]```: makes directory.
3. ```mv [file] [location]```: this command allows you to move files and folders into other directories or allows you to convert a file type -- i.e., from ```.py``` to ```.js```
4. ```touch [file]```: allows you to create file from CLI.
5. ```cat [file]```: allows you to see what is inside of a file without going into that file.
6. ```ls```: lists everything inside of a current directory.
7. Language Specific Commands: this is more general, but knowing the commands for your specific coding language is important. For Python you would want to know: ```python```, ```pip install```, ```pip list```, ```source venv/bin/activate```, etc. You may also want to learn Docker and cloud commands -- useful for interfacing with AWS, GCP, or Azure. For general use, knowing about ```docker login```, ```docker build -t imageName .```, ```docker run -it -p port:port imageName```. 
 #### Vim Commands
 8. ```:q``` or ```:q!```: quits vim, which is surprisingly hard for beginners.
 9. ```:w```: saves the work you do.
 10. ```:Ex```: exits properly
 11. ```i```: insert modes for editting. 
 12. ```<esc>```: escapes into normal mode.
 13. ```dd```: deletes line.
 14. ```$```: skips to end of a line in normal mode. 
 15. ```:[number]```: skips to a certain row. 
 16. ```C-w, <arrow>```: when splitting screen, this allows you to switch which file you work on.

