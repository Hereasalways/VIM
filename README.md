# vim配置

## 简介

该代码是一份vim的配置脚本, 遵循以下思路去配置：

1. 尽可能不改变vim原生快捷键和配置
2. 尽可能精简插件，只保留当前github最热最实用插件
3. 插件的快捷键尽可能不使用vim原有快捷键，防止覆盖vim原有功能

## 效果图
### 完整界面

![](1.png)

+ 左侧为目录树，按F2打开
+ 右侧为符号列表， 按F9打开
+ 顶上为打开buffer列表，默认打开，为airline功能，可修改配置关闭
+ 底下为状态栏，使用了airline插件的经典状态栏

### 文件搜索功能

![](2.png)

按ctrl+p 进入文件搜索功能,由当前最热门的fzf提供搜索支持

除了ctrl+p以外，还有如下搜索快捷键提供各种类型搜索：

    nnoremap <c-n>f :FZF<CR>
    nnoremap <c-n>g :GFiles?<CR>
    nnoremap <c-n>b :Buffers<CR>
    nnoremap <c-n>a :Ag<CR>
    nnoremap <c-n>r :Rg<CR>
    nnoremap <c-n>l :BLines<CR>
    nnoremap <c-n>t :BTags<CR>
    nnoremap <c-n>m :Marks<CR>
    nnoremap <c-n>h :History<CR>
    nnoremap <c-n>k :History:<CR>
    nnoremap <c-n>/ :History/<CR>
    nnoremap <c-n>c :Commands<CR>

### 代码搜索功能

![](3.png)


+ 普通模式按F8跳出搜索代码命令，输入待搜索单词进行搜索
+ 或visual模式下按F8搜索当前选择单词，
+ 使用ctrlsf插件提供搜索功能，搜索结果可编辑保存

## 安装 
+ git clone https://github.com/Hereasalways/VIM.git
+ mv VIM ~/.vim
+ cp ~/.vim/.vimrc ~/.vimrc
+ 打开vim, 执行:PlugInstall
+ 安装ctags, gtags, astyle, lua, the\_silver\_searcher, fcitx-remote-for-osx, python3, clangd/ccls

## vim 编译配置参考

```
./configure --with-features=huge \
            --enable-multibyte \
            --enable-rubyinterp=yes \
            --enable-perlinterp=yes \
            --enable-luainterp=yes \
            --with-lua-prefix=/usr/ \
            --enable-cscope \
            --prefix=/home/xuchaojie/vim8 \
            --enable-python3interp=yes \
            --with-python3-command=python3
```


