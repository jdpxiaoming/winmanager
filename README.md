# winmanager
win manager for vim mirror http://vim.sourceforge.net/scripts/script.php?script_id=95

这是方便我使用Vundle.vim所建立的winManager 2.3 的一个镜像，你可以随意使用，请放心使用 如有更新欢迎留言我会及时更新！

[winmanager插件]

winmanager插件可以把Explorer插件(vim 7.0以前的文件浏览插件，现在的netrw)和BufExplorer插件集成在一起，我们上篇文章中介绍过的taglist插件也提供了对winmanager插件的支持。

下载后，把该文件在~/.vim/目录中解压缩，这会把winmanager插件解压到~/.vim/plugin和~/.vim/doc目录中：

plugin/winmanager.vim – winmanager插件
plugin/winfileexplorer.vim  - 改良的Explorer插件
plugin/wintagexplorer.vim – winmanager提供的tag插件，用处不大
doc/winmanager.txt – 帮助文件 
仍然用”:helptags ~/.vim/doc“命令来生成帮助标签，然后就可以使用”:help winmanager“来查看帮助了。

使用winmanager插件可以控制各插件在vim窗口中的布局显示。我的vimrc中这样设置：

  """"""""""""""""""""""""""""""
  
  " winManager setting
  
  """"""""""""""""""""""""""""""
  
  let g:winManagerWindowLayout = "BufExplorer,FileExplorer|TagList
  
  let g:winManagerWidth = 30
  
  let g:defaultExplorer = 0
  
  nmap <C-W><C-F> :FirstExplorerWindow<cr>
  
  nmap <C-W><C-B> :BottomExplorerWindow<cr>
  
  nmap <silent> <leader>wm :WMToggle<cr>
  
g:winManagerWindowLayout变量的值定义winmanager的窗口布局，使用上面的设置，我们的窗口布局看起来是这样的：
