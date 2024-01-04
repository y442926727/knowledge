操作系统，有Window，MAC，Linux

要检查 Linux 系统是否[安装](https://www.bunian.cn/tag/az)了[桌面环境](https://www.bunian.cn/tag/zhuomianhuanjing)，可以尝试以下几种方法：

#### 检查运行的显示[管理器](https://www.bunian.cn/tag/guanliqi)（display manager）

显示管理器负责管理图形登录界面。通常，安装桌面环境时会自动安装一个显示管理器。

检查当前正在运行的显示管理器，可以查看系统是否安装了桌面环境。

在终端中输入以下命令：

```
systemctl list-units --type=service | grep -E '(gdm|sddm|lightdm|lxdm|kdm|xdm|slim)'
```

如果输出中显示了一个或多个显示管理器（例如，`gdm.service`、`lightdm.service` 等），则表明系统已安装桌面环境。

#### 检查安装的桌面环境包

检查系统中已安装的桌面环境包，可以帮助您确定是否安装了桌面。在基于 Debian 的系统（例如，Ubuntu、Linux Mint）上，使用以下命令：

```
dpkg -l | grep -E '(gnome|kde|xfce|lxde|lxqt|cinnamon|mate|budgie|deepin|enlightenment)'
```

在基于 RHEL 的系统（例如，Fedora、CentOS、RHEL）上，使用以下命令：

```
rpm -qa | grep -E '(gnome|kde|xfce|lxde|lxqt|cinnamon|mate|budgie|deepin|enlightenment)'
```

如果输出中显示了一个或多个桌面环境包，则表明系统已安装桌面环境。

#### 查看登录界面

如果您能够在启动 Linux 系统时看到图形登录界面，这意味着您的系统已安装了桌面环境。

图形登录界面可能包括用户名、密码输入框以及桌面环境选择器等元素。

**总结**

通过以上方法，您可以确定 Linux 系统是否安装了桌面环境。

需要注意的是，某些轻量级发行版可能使用非常简洁的桌面环境，因此在使用第二种方法时，您可能需要针对这些轻量级桌面环境进行搜索。

init 0：关机
init 3 ：图形化切换到命令行界面
init 5：命令行切换到图形化界面
init 6：重启

[Linux 系统的启动过程六阶段 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/561243350?utm_id=0)

https://developer.tuya.com/cn/docs/archived-documents/raspberry-pi?id=Kag5j3k931w6n
