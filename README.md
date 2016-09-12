# 终极vim配置
终极vim配置是一个被良好优化的vim配置,它包含NERD Tree,文件查找,代码补全,语法检查等多个开发必备的插件,一键安装,省去你到处找各种vim插件的麻烦.



## 如何安装?

```bash
git clone https://git.oschina.net/eccozhou/vimrc.git ~/.vim_runtime
sh ~/.vim_runtime/install_awesome_vimrc.sh
```


## 功能简介

### NERD Tree树形目录
命令模式输入",nn",右边栏会弹出一个以开始运行vim所在目录为根目录的一个树状文件目录列表:
![Screenshot 1](http://d3.freep.cn/3tb_160903110454be7e572973.png)


### 当前目录文件名查找
命令模式按住ctrl + f,打开查找窗口,输入部分文件名快速查找文件:
![Screenshot 2](http://d2.freep.cn/3tb_1609031121082u5n572973.png)


### 语法检查
当编辑的代码出现语法错误时,vim底部会弹出红色提醒框:
![Screenshot 3](http://d2.freep.cn/3tb_160903115729dnvi572973.png)


### 代码片段填充
比如在一个c文件里, 插入模式你输入`for<tab>`, 她将填充一个for循环代码片段:

```c
for (i = 0; i < count; i++) {

}
```

### 当前已打开文件列表
打开一个文件后, 在命令模式":e 文件"再打开一个文件, 这时命令模式输入",o", 你将看到当前已打开文件列表.


### Goyo写作模式
命令模式输入":Goyo"进入.


### 快速注释
命令模式输入"gcc"注释光标所在行.


## 如何包含自定义的配置
安装完成后你可以新建 **~/.vim_runtime/my_configs.vim** 文件,在里面添加你需要的配置项目,下面是我的 **my_configs.vim** :

```bash
cd ~/.vim_runtime/ | cat my_configs.vim
syntax enable
set background=dark
colorscheme solarized
```

你也可以安装你自己需要的插件, 比如使用pathogen我们可以安装 [vim-rails](https://github.com/tpope/vim-rails):

```bash
cd ~/.vim_runtime
git clone git://github.com/tpope/vim-rails.git sources_non_forked/vim-rails
```

## 如何卸载
按如下进行操作:
* 删除 `~/.vim_runtime`
* 删除你的`~/.vimrc`中有关`.vim_runtime`的配置


## Linux注意事项
请确保你的vi是vim的别名, 否则请使用vim编辑文件.


## 已安装的插件
详细了解各插件用法, 可查看各插件相应文档.

* [pathogen.vim](https://github.com/tpope/vim-pathogen): Manages the runtime path of the plugins
* [snipMate.vim](https://github.com/garbas/vim-snipmate): snipMate.vim aims to be a concise vim script that implements some of TextMate's snippets features in Vim
* [bufexplorer.zip](https://github.com/vim-scripts/bufexplorer.zip): Buffer Explorer / Browser. This plugin can be opened with `<leader+o>`
* [NERD Tree](https://github.com/scrooloose/nerdtree): A tree explorer plugin for vim
* [ack.vim](https://github.com/mileszs/ack.vim): Vim plugin for the Perl module / CLI script 'ack'
* [ag.vim](https://github.com/rking/ag.vim): A much faster Ack
* [ctrlp.vim](https://github.com/ctrlpvim/ctrlp.vim): Fuzzy file, buffer, mru and tag finder. In my config it's mapped to `<Ctrl+F>`, because `<Ctrl+P>` is used by YankRing
* [mru.vim](https://github.com/vim-scripts/mru.vim): Plugin to manage Most Recently Used (MRU) files. Includes my own fork which adds syntax highlighting to MRU. This plugin can be opened with `<leader+f>`
* [open_file_under_cursor.vim](https://github.com/amix/open_file_under_cursor.vim): Open file under cursor when pressing `gf`
* [vim-indent-object](https://github.com/michaeljsmith/vim-indent-object): Defines a new text object representing lines of code at the same indent level. Useful for python/vim scripts
* [vim-multiple-cursors](https://github.com/terryma/vim-multiple-cursors): Sublime Text style multiple selections for Vim, CTRL+N is remapped to CTRL+S (due to YankRing)
* [vim-expand-region](https://github.com/terryma/vim-expand-region): Allows you to visually select increasingly larger regions of text using the same key combination.
* [vim-fugitive](https://github.com/tpope/vim-fugitive): A Git wrapper so awesome, it should be illegal
* [goyo.vim](https://github.com/junegunn/goyo.vim) and [vim-zenroom2](https://github.com/amix/vim-zenroom2): 
Remove all clutter and focus only on the essential. Similar to iA Writer or Write Room [Read more here](http://amix.dk/blog/post/19744)
* [vim-commentary](https://github.com/tpope/vim-commentary): Comment stuff out.  Use `gcc` to comment out a line (takes a count), `gc` to comment out the target of a motion. `gcu` uncomments a set of adjacent commented lines.
* [syntastic](https://github.com/scrooloose/syntastic): Syntax checking hacks for vim
* [vim-yankstack](https://github.com/maxbrunsfeld/vim-yankstack): Maintains a history of previous yanks, changes and deletes
* [lightline.vim](https://github.com/itchyny/lightline.vim): A light and configurable statusline/tabline for Vim


## 包含的配色方案

* [peaksea](https://github.com/vim-scripts/peaksea)
* [vim-colors-solarized](https://github.com/altercation/vim-colors-solarized)
* [vim-irblack](https://github.com/wgibbs/vim-irblack)
* [mayansmoke](https://github.com/vim-scripts/mayansmoke)
* [vim-pyte](https://github.com/therubymug/vim-pyte)


Fork from https://github.com/amix/vimrc
