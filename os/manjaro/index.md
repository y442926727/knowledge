1、下载 汉化包
`sudo pacman -S firefox-i18n-zh-cn`

2、查看add-ons下的language选项有没有已安装的包

3、在浏览器的地址栏输入`about:config` 搜索`intl.locale.requested` 将其值修改为`zh_CN`



## 首先更换国内源

[pacman](https://archlinux.org/pacman/)[软件包管理器](https://en.wikipedia.org/wiki/Package_management_system)是 Arch Linux 的一大亮点。它将一个简单的二进制包格式和易用的[构建系统](https://wiki.archlinux.org/index.php/Arch_Build_System_(简体中文))结合了起来。*pacman*的目标是简化对软件包的管理，无论软件包是来自[官方软件仓库](https://wiki.archlinux.org/index.php/Official_repositories_(简体中文))还是来自用户自己的创建。

*pacman* 通过和主服务器同步软件包列表来进行系统更新。这种服务器/客户端模式可在使用一条命令就下载或安装软件包的同时，也安装其必需的依赖包。

*pacman* 用 [C 语言](https://wiki.archlinux.org/index.php/C_(简体中文))编写，使用[bsdtar(1)](https://jlk.fjfi.cvut.cz/arch/manpages/man/bsdtar.1)[tar](https://en.wikipedia.org/wiki/tar_(computing))作为打包格式。

Manjaro下的实用命令搜集https://blog.csdn.net/sdujava2011/article/details/91872791

```shell
#手动选择国内源
sudo pacman-mirrors -i -c China -m rank   
#同步仓库
 #只下载已改列表：
sudo pacman -Sy
 #有时你可能想要强制下载软件包列表。 为此，请输入：
sudo pacman -Syy
#更新软件
 #更新已安装软件
sudo pacman -Su
 #更新软件前检查包列表是否最新:
sudo pacman -Syu
 #更新前强制下载包列表：
sudo pacman -Syyu
#查找软件
sudo pacman -Ss leafpad
#安装软件
sudo pacman -S leafpad
#卸载软件
sudo pacman -R leafpad
#卸载同时移除未被其他软件使用的依赖项
#sudo pacman -Rs leafpad
#同时再移除软件的配置文件
#sudo pacman -Rns leafpad
#在以后再删这些文件也是可以的
sudo pacman -Rns $(pacman -Qtdq)

```