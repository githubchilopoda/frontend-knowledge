# startup

```
vi /etc/rc.local

#!/bin/sh -e
#
# rc.local
#
# This script is executed at the end of each multiuser runlevel.
# Make sure that the script will "exit 0" on success or any other
# value on error.
#
# In order to enable or disable this script just change the execution
# bits.
#
# By default this script does nothing.

/usr/bin/sslocal -c /etc/shadowsocks/config.json
exit 0
```

# keybinding

ubuntu:

```
长按super建，会出来所有快捷键的提示
```

# 将CapsLock修改为Ctrl键

ubuntu:

```
sudo vi /etc/default/keyboard
XKBOPTIONS='ctrl:swapcaps'

sudo dpkg-reconfigure keyboard-configuration //需重启系统，否则可能会遇到切换中文输入法将配置还原的问题（ibus）
```

http://askubuntu.com/questions/149971/how-do-you-remap-a-key-to-the-caps-lock-key-in-xubuntu

# apt-get

如果出现无法定位软件包，可以``sudo apt-get update``

如果``apt-get update``没有更新，那么查看``/etc/apt/sources.list``是否为空，如果为空可将``/usr/share/doc/apt/examples/sources.list``拷贝过去

# bandwidth

http://askubuntu.com/questions/20872/how-do-i-limit-internet-bandwidth

# proxy

首次使用chrome需设置系统proxy，对于ss，只要手动设置socks代理，不要设置http/https代理，否则会连不上