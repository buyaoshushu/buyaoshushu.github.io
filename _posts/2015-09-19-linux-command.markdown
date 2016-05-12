---
layout: post
title:  "Linux常用命令"
date:   2015-08-17 22:10:00
categories: 学习笔记
tags: [ linux,学习笔记,常用命令 ]
---
>本文说明：文章主要用于自己备忘，记录的是在日常工作娱乐中用到的一些命令及软件包，并不一定都是常用命令。基础命令完全没有收集。所以不适用于初学者。另外，处理命令还有一些软件记录。如果对命令或软件有疑问可以直接评论给我。我会第一时间回复的。

ssh端口转发
ssh -C -f -N -g -L 3999:127.0.0.1:3306 root@server.ip.domain

# Linux
###文件搜索
####搜索文件
```bash
#in ubuntu
mlocate
#in archlinux
locate
```
####更新索引
```bash
updatedb
```

####文件内搜索（学习中）
```bash
#新发现的方法
tracker
````

###中文man
```bash
pacman -Ss man-pages-zh_cn
```

###窗口管理
```bash
#用户激活管理窗口等，可以实现快捷键激活某程序
wmctrl -a
```

###挂载
```bash
mount.ntfs-3g /dev/sda4 /media/others -n -o rw,utf8,uid=1000,gid=1000,dmask=022,fmask=133
```
###随机输出文本
```bash
sort -R
```

###播放软件
```bash
mplayer -playlist "playlistfile"
```
###创建SSH公钥
```bash
cd ~/.ssh
ssh-keygen -t rsa -C "your_email@youremail.com" 
```

###配置多屏幕
```bash
xrandr
#关闭内置屏幕
xrandr --output LVDS1 --off
#启动屏幕 
xrandr --output LVDS1 --auto
```

###配置音量
```bash
amixer
amixer -D pulse set Master 40%
#alias to volume
```

###保存URL或HTML文件为图片
```bash
cutycapt --url=http://file:// --out=filename
```

###压缩图片质量，转换图片格式等等，图片处理神器
```bash
convert -quality 70 fromimg.jpg toimg.jpg
```

##禁用触摸板
```bash
#临时禁止
sudo modprobe -r psmouse
#开启触摸板
sudo modprobe -a psmouse
#永远禁用触摸板
sudo vi /etc/modprobe.d/blacklist.conf
blacklist psmouse
```

##awesome
###不能显示壁纸
```bash
pacman -S feh
```
###个性化配置文件
```bash
cp /etc/xdg/awesome/rc.lua ~/.config/awesome/rc.lua
```
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
```bash
#in alsa
alsamixer
#in puseaudio
pavucontrol
```

###百度云管理
```bash
bcloud-gui
bypy
```

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
variety需要修改配置文件用以在awesome或i3中使用

###随机命令
shuf

###看视频
```bash
mpv
#使用shift+q退出可以保存上次退出位置
```

###科学计算
```bash
Scilab 
```

###查询窗口信息
```bash
xprop WM_CLASS
```

###屏保管理
```bash
xset DPMS 
```

###无线管理
```bash
netctl-auto
wifi-menu
```

###音乐播放器
```bash
mpd
#前端
ario/ncmpc/ncmpcpp/osdlyrics
```

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
```bash
sudo reflector --verbose --country 'China' -l 20 -p http \
--sort rate --save /etc/pacman.d/mirrorlist
```

###清理无用软件包
```bash
pacman -Qtd | awk '{print $1}' | xargs -t yaourt -R
```

###GTK主题管理
lxappearance

###更新ＤＮＳ
```bash
sudo systemctl restart nscd.service
```



###终端乱码
```bash
luit -encoding gbk telnet 123.125.116.212 6666
```
###搜狗输入法皮肤安装
使用sogou-qimpanel打开皮肤文件

###鼠标控制
keynav-git
