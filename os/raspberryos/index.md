安装VIM

```
sudo apt-get install vim
sudo cp /etc/apt/sources.list /etc/apt/sources.list_`date +%Y%m%d%H%M`.bak
sudo cp /etc/apt/sources.list.d/raspi.list /etc/apt/sources.list.d/raspi.list.`date +%Y%m%d%H%M`.bak
sudo nano /etc/apt/sources.list
sudo nano /etc/apt/sources.list.d/raspi.list 

gpg --keyserver keyserver.ubuntu.com --recv-keys 9165938D90FDDD2E
gpg --export --armor 9165938D90FDDD2E | sudo apt-key add -
sudo apt-get update
sudo apt-get upgrade
```