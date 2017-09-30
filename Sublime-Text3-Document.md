##sublime Text 3
```
安装准备——安装 Package Control
Package Control是一个开源的用于插件管理的插件，在为Sublime安装其他插件之前，需要安装它。
它有两种安装方式Simple和Manual。此处我们选择simple方式来安装。
从菜单 View - Show Console 或者 ctrl + ~ 快捷键，调出 console。将以下 Python 代码粘贴进去并 enter 执行，不出意外即完成安装\

Sublime Text __3：__
import urllib.request,os,hashlib; h = '2915d1851351e5ee549c20394736b442' + '8bc59f460fa1548d1514676163dafc88'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)

```
###ubuntu 
```
1.打开终端，首先安装 subl3 的软件库，使用命令

sudo add-apt-repository ppa:webupd8team/sublime-text-3

中间会询问是否添加仓库，点击enter即可。

2.刷新软件库，使用命令

sudo apt-get update

3.安装subl3,使用命令

sudo apt-get install sublime-text-installer

通过以上三步，subl就安装完成了，安装完成会自动启动，把软件图标锁定到侧边启动栏，以后就直接可以点击图标启动了。

然后就是最基本的配置了。

```
###Sublime package
***
#####sublime text 3 的中文汉化
```
汉化subl很简单。
直接点击 Preferences 选项卡的 package control 选项，选择下拉的 install package 选项
在输入框中输入  localization ，然后点击检索出来的 Chineselocalizetion 插件，等待安装完成
再看一下界面，已经成中文的了。如果需要切换，点击 帮助 选项卡的 language 选项可以选择你想要的语言。
```
#####安装 emmet 插件
```
写 html 怎么能不用 emmet 插件呢，简直是神器啊。可以 google 一下 看一下教程，试用一下，你会发现你已经离不开它了。
安装 emmet 插件很简单，跟安装汉化差不多，点开选项卡 首选项，在点开 package control ，再点击 install package ，在弹出的搜索框输入 emmet，等待安装完成就可以了。
需要注意的是，跟别的编辑器的 emmet 插件使用 table 来自动填写不同，sublame text 3 需要使用 ctrl + e 来完成自动填写。你可以试一下，输入 ！，之后按 ctrl + e，一个HTML文件的主体就出现了。
如果你想在 emmet 使用 tabel 来完成自动填写，那就需要修改 emmet 插件设置了
```
#####清空sublime text 3 配置（还原设置）
```
subl的缺点就是有时候出现莫名其妙的bug，卸载重装又很麻烦。
这时可以通过清空subl的配置文件，来达到还原设置，让 subl 像刚装上一样，清新可人（这是什么形容词啊？）
清空配置命令如下：
sudo rm -rf /home/$USER/.config/sublime-text-3/
使用后就像恢复出厂设置了一样（不要乱试，后果严重，在你确定需要的时候再使用，否则你要哭出来）
```
####Markdown
#####MarkdownEditing
```
MarkdownEditing提供markdown编辑的基本辅助提示，也有自己的一套配色方案。安装此插件可以方便markdown的书写。打开Command Paletter，按照上述方法安装即可。
安装Markdown Preview或OmniMarkupPreviewer
这两个插件是用来预览markdown文档的。此处推荐OmniMarkupPreviewer，这个打开一次就可以实时预览自己编辑的内容。安装完OmniMarkupPreviewer后，默认是不支持mathjax公式的，需要支持，请修改配置文件，在user中增加以下配置即可。
{ "mathjax_enabled": true }
***********************************
接下来推荐几个增强型的插件
Monokai Extended & Markdown Extended
提供一套Monokai的markdown主题，比原来的美观。
MarkdownTOC
这个插件可以一键生成目录。安装完后的简单配置工作。打开Preferences -> Package Settings -> MarkdownTOC -> Setting - User进行配置。
{ "default_autolink": true, #目录以链接形式呈现 "default_bracket": "round", #目录以链接形式呈现 "default_depth": 0 #无限目录深度}

将光标置于文档首部，点击 Tools -> MarkdownTOC -> Insert TOC，会自动在文首生成目录.
Table Editor
用于编辑表格的工具。

```
#####OmniMarkupPreviewer
```
ctrl+alt+o
http://macplay.leanote.com/post/%E8%BF%91%E4%B9%8E%E5%AE%8C%E7%BE%8E%E7%9A%84-Markdown-%E5%86%99%E4%BD%9C%E4%BD%93%E9%AA%8C-Sublime-Text-3-OmniMarkupPreviewer
```

