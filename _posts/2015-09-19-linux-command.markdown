---
layout: post
title:  "Linux常用命令"
date:   2015-08-17 22:10:00
categories: 学习笔记
tags: [ linux,学习笔记,常用命令 ]
---

# Linux

###文件搜索

####搜索文件

{% highlight bash %}
#in ubuntu
mlocate
#in archlinux
locate
{% endhighlight %}
####更新索引
{% highlight bash %}
updatedb
{% endhighlight %}

###中文man
man-pages-zh_cn

###窗口管理
{% highlight bash %}
wmctrl -a
{% endhighlight %}
用户激活管理窗口等，可以实现快捷键激活某程序
###挂载
{% highlight bash %}
mount.ntfs-3g /dev/sda4 /media/others -n -o rw,utf8,uid=1000,gid=1000,dmask=022,fmask=133
{% endhighlight %}
###随机输出文本
{% highlight bash %}
sort -R
{% endhighlight %}
###播放软件
{% highlight bash %}
mplayer -playlist "playlistfile"
{% endhighlight %}
###创建公钥
{% highlight bash %}
cd ~/.ssh
ssh-keygen -t rsa -C "your_email@youremail.com" 
{% endhighlight %}
###配置多屏幕
{% highlight bash %}
xrandr
#关闭内置屏幕
xrandr --output LVDS1 --off
#启动屏幕 
xrandr --output LVDS1 --auto
{% endhighlight %}
###配置音量
{% highlight bash %}
amixer
amixer -D pulse set Master 40%
#alias to volume
{% endhighlight %}
###保存URL或HTML文件为图片
{% highlight bash %}
cutycapt --url=http://file:// --out=filename
{% endhighlight %}
###压缩图片质量
{% highlight bash %}
convert -quality 70 fromimg.jpg toimg.jpg
{% endhighlight %}

##禁用触摸板
临时禁止触摸板
{% highlight bash %}
sudo modprobe -r psmouse
{% endhighlight %}
开启触摸板
{% highlight bash %}
sudo modprobe -a psmouse
{% endhighlight %}
永远禁用触摸板：
{% highlight bash %}
sudo vi /etc/modprobe.d/blacklist.conf
blacklist psmouse
{% endhighlight %}

##awesome
###不能显示壁纸
> 安装feh

###个性化配置文件
{% highlight bash %}
cp /etc/xdg/awesome/rc.lua ~/.config/awesome/rc.lua
{% endhighlight %}

##软件记录
###轻量级文件管理器
thunar
###图形化SVN
rapidsvn
###邮件客户端
thunderbird
###文本编辑
wps et wpp
vim
vimcdoc-svn

###声音设置
{% highlight bash %}
#in alsa
alsamixer
#in puseaudio
pavucontrol
{% endhighlight %}
###百度云管理
{% highlight bash %}
bcloud-gui
bypy
{% endhighlight %}

###屏幕取色
gpick

###markdown编辑器
remarkable
###看图
sxiv
sxiv -t 缩略图模式
feh
###截图
scrot

###自动换壁纸软件
Variety需要修改配置文件用以在awesome或i3中使用
###随机命令
shuf
###看视频
{% highlight bash %}
mpv
#使用shift+q退出可以保存上次退出位置
{% endhighlight %}
###科学计算
{% highlight bash %}
Scilab 
{% endhighlight %}
###查询窗口信息
{% highlight bash %}
xprop WM_CLASS
{% endhighlight %}
###屏保管理
{% highlight bash %}
xset DPMS 
{% endhighlight %}

###无线管理
{% highlight bash %}
netctl-auto
wifi-menu
{% endhighlight %}
###音乐播放器
{% highlight bash %}
mpd
#前端
ario/ncmpc/ncmpcpp/osdlyrics
{% endhighlight %}

###电子书
calibre

###音频编辑
Audacity
ardour
qtractor 
lmms
snd
DJ工具
mixxx
mp3标签管理
easytag

###游戏 
openra 开源红色警戒
wesnoth 韦诺之战

###游戏平台
Humble Store? 
steam

##建模流程绘图
yEd
umbrello

###按键精灵
xdotool

###源测速
{% highlight bash %}
sudo reflector --verbose --country 'China' -l 20 -p http --sort rate --save /etc/pacman.d/mirrorlist

{% endhighlight %}

###清理无用软件包
pacman -Qtd | awk '{print $1}' | xargs -t yaourt -R

###GTK主题管理
lxappearance


find /medit/others -type f -name "*.txt" | xargs grep "天道"

###终端乱码
luit -encoding gbk telnet 123.125.116.212 6666 
