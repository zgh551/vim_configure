# Vim Configuration
This paper contain the configure file of vim and powerline configuration.

## 1. powerline

### 1.1. add follow contains to `.bashrc` file

```bash
POWERLINE_SCRIPT=/usr/share/powerline/bindings/bash/powerline.sh
if [ -f $POWERLINE_SCRIPT ]; then
    powerline-daemon -q
    POWERLINE_BASH_CONTINUATION=1
    POWERLINE_BASH_SELECT=1
    source $POWERLINE_SCRIPT
fi
```

其中,第一行代表powerline的软件的安装位置.

使用powerline配置terminal,文件路径"~/."

## 2. tmux tool

### 2.1. add `.tmux.conf` file to user path

关于`tmux`工具的配置,文件位于"~/."

### 2.2. set powerline to be tmux
```bash
set -g default-terminal "screen-256color"
source "/usr/share/powerline/bindings/tmux/powerline.conf"
```

## 3. vim
### 3.1. add `.vimrc` file to user path

配置vim编辑器,文件位于用户根目录"~/."

### 3.2. add `Vundle` plug
#### 3.2.1. Download Vundle
```shell
$ git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```
after this, open `vim` and enter `:PlugInstall`

### 3.3. Clang Format Tool
#### 3.3.1. add clang vundle plug
```shell
" clang-format for language format
Plugin 'rhysd/vim-clang-format'
```

#### 3.3.2. configure clang format for vim
```bash
let g:clang_format#command = 'clang-format'
nmap <F4> :ClangFormat<cr>
autocmd FileType c ClangFormatAutoEnable
let g:clang_format#detect_style_file = 1
```
[doc for clang format](https://github.com/rhysd/vim-clang-format)

### 3.4. add `.ycm_extra_conf.py` file

YCM配置文件,主要指定搜索文件路径,在根目录新建.vim文件夹,"~/.vim/."
