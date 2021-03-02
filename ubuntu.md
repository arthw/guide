## Win10安装ubuntu18.04双系统黑屏怎么解救？
进去了ubuntu的启动界面，结果一闪就成了黑屏。

题主是有用独立显卡吗？
尝试让光标停留在“Try”项目按e，在代码中找到quiet slash ，在这之后添加acpi_osi=linux nomodeset，保存文本进入即可（Ctrl+X）。 


## 最大化按钮消失，minimize maximize buttons missing tightenvnc Ubuntu 20.04
Download xfwm4_4.14.5-1_amd64.deb from https://launchpad.net/ubuntu/groovy/amd64/xfwm4/4.14.5-1
```
wget http://launchpadlibrarian.net/494460182/xfwm4_4.14.5-1_amd64.deb
sudo dpkg -i xfwm4_4.14.5-1_amd64.deb
reboot
```

## 关闭自动休眠功能

检查休眠功能的状态以及历史记录，如下：
```
$ systemctl status sleep.target
 ● sleep.target - Sleep
    Loaded: loaded (/lib/systemd/system/sleep.target; static; vendor preset: enabled)
    Active: inactive (dead)
      Docs: man:systemd.special(7)
 Feb 24 13:18:08 xps systemd[1]: Reached target Sleep.
 Feb 26 13:29:31 xps systemd[1]: Stopped target Sleep.
 Feb 26 13:29:57 xps systemd[1]: Reached target Sleep.
 Feb 26 13:30:19 xps systemd[1]: Stopped target Sleep.
```
	
执行关闭休眠功能的命令，如下：
```
$ sudo systemctl mask sleep.target suspend.target hibernate.target hybrid-sleep.target
 Created symlink /etc/systemd/system/sleep.target → /dev/null.
 Created symlink /etc/systemd/system/suspend.target → /dev/null.
 Created symlink /etc/systemd/system/hibernate.target → /dev/null.
 Created symlink /etc/systemd/system/hybrid-sleep.target → /dev/null.
```
再次观察系统休眠状态，如下：
```
$ systemctl status sleep.target
● sleep.target
   Loaded: masked (Reason: Unit sleep.target is masked.)
   Active: inactive (dead)
```
发现自动休眠功能已经被关闭，不会出现自动休眠导致远程控制无法访问的情况了。
