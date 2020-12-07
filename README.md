# vim_configure
contain the configure file of vim

- .bashrc

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

- .tmux.conf

关于`tmux`工具的配置,文件位于"~/."

```bash
set -g default-terminal "screen-256color"
source "/usr/share/powerline/bindings/tmux/powerline.conf"
```

- .vimrc

配置vim编辑器,文件位于用户根目录"~/."



- .ycm_extra_conf.py

YCM配置文件,主要指定搜索文件路径,在根目录新建.vim文件夹,"~/.vim/."