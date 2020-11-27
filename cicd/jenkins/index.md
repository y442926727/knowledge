# windows环境下安装

## 下载

地址：https://jenkins.io/

![image-20200426165755550](index.assets/image-20200426165755550.png)

![image-20200426165943147](index.assets/image-20200426165943147.png)

## 安装

![image-20200426170044575](index.assets/image-20200426170044575.png)

![image-20200426170102615](index.assets/image-20200426170102615.png)

![image-20200426170135689](index.assets/image-20200426170135689.png)

![image-20200426170150126](index.assets/image-20200426170150126.png)

![image-20200426170206098](index.assets/image-20200426170206098.png)

![image-20200426170219386](index.assets/image-20200426170219386.png)

![image-20200426170233343](index.assets/image-20200426170233343.png)

![image-20200426170247514](index.assets/image-20200426170247514.png)

![image-20200426170307020](index.assets/image-20200426170307020.png)

![image-20200426170328987](index.assets/image-20200426170328987.png)

![image-20200426170344504](index.assets/image-20200426170344504.png)

![image-20200426170358862](index.assets/image-20200426170358862.png)

![image-20200426170410276](index.assets/image-20200426170410276.png)

![image-20200426170503738](index.assets/image-20200426170503738.png)

# linux环境下安装

ToDo

# 使用

## 修改用密码

![image-20200426170640742](index.assets/image-20200426170640742.png)

![image-20200426170655027](index.assets/image-20200426170655027.png)

![image-20200426170708132](index.assets/image-20200426170708132.png)

## 安装插件

### 源代码插件（SVN）

![image-20200426170741797](index.assets/image-20200426170741797.png)

![image-20200426170828723](index.assets/image-20200426170828723.png)

![image-20200426170858064](index.assets/image-20200426170858064.png)

### jenkins插件下载镜像加速

修改C:\windows\system32\drivers\etc\hosts文件

```ini
127.0.0.1		updates.jenkins-ci.org
```

![img](index.assets/1590045499784.png)

修改Nginx代理设置

```
        location /download/plugins
        {
            proxy_next_upstream http_502 http_504 error timeout invalid_header;
            proxy_set_header Host mirrors.tuna.tsinghua.edu.cn;
            proxy_set_header X-Real-IP $remote_addr;
            proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
            rewrite /download/plugins(.*) /jenkins/plugins/$1 break;
            proxy_pass https://mirrors.tuna.tsinghua.edu.cn;
        }
```

![img](index.assets/15900459777267.png)

# 问题

## 代理

![image-20200426181052524](index.assets/image-20200426181052524.png)

![image-20200426181106597](index.assets/image-20200426181106597.png)

SVN配置

C:\Windows\SysWOW64\config\systemprofile\AppData\Roaming\Subversion

![image-20200426181147318](index.assets/image-20200426181147318.png)

C:\Users\Administrator\AppData\Roaming\Subversion

![image-20200426181211096](index.assets/image-20200426181211096.png)

![image-20200426181229032](index.assets/image-20200426181229032.png)