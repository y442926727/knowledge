# asp.net
## 【构建】服务器环境安装

###  ASP.NET生成工具(MSBuild)

#### 下载

搜索引擎搜索VS2017,进入微软官方下载页面，在页面下方的“所有下载”中展开“工具”栏位，按下图下载生产工具。

![image-20200426172410803](index.assets/image-20200426172410803.png)

#### 安装

![image-20200426172559912](index.assets/image-20200426172559912.png)

![image-20200426172619504](index.assets/image-20200426172619504.png)

![image-20200426172631431](index.assets/image-20200426172631431.png)

![image-20200426172642698](index.assets/image-20200426172642698.png)

![image-20200426172656881](index.assets/image-20200426172656881.png)

后续根据你发布的类型选择你要安装的工具类型。

### Jenkins相关插件安装和配置

#### 安装插件

![image-20200426170741797](index.assets/image-20200426170741797.png)

![image-20200426170800084](index.assets/image-20200426170800084.png)

![image-20200426170828723](index.assets/image-20200426170828723.png)

![image-20200426170858064](index.assets/image-20200426170858064.png)



#### 配置

![image-20200426170934874](index.assets/image-20200426170934874.png)

![image-20200426170952650](index.assets/image-20200426170952650.png)



##  【测试】服务器环境安装

### IIS安装时必须安装管理服务或添加安装管理服务

![image-20200426173152327](index.assets/image-20200426173152327.png)

![image-20200426174943616](index.assets/image-20200426174943616.png)

### Web Deploy安装

#### 下载

地址：https://www.iis.net/downloads/microsoft/web-deploy

![image-20200426175346801](index.assets/image-20200426175346801.png)

![image-20200426175403196](index.assets/image-20200426175403196.png)

#### 安装

![image-20200426175449655](index.assets/image-20200426175449655.png)

#### 站点启用Web Deploy发布

在启用之前，请按照通常IIS部署站点方式部署网站，然后再这个网站右键如下图启用。

![image-20200426175613908](index.assets/image-20200426175613908.png)

![image-20200426175635639](index.assets/image-20200426175635639.png)

## 建立构建任务

### 准备构建配置

![image-20200426175811615](index.assets/image-20200426175811615.png)

![image-20200426175836639](index.assets/image-20200426175836639.png)

![image-20200426175852995](index.assets/image-20200426175852995.png)

### 新建构建任务

![image-20200426175937099](index.assets/image-20200426175937099.png)

![image-20200426175951075](index.assets/image-20200426175951075.png)

![image-20200426180005490](index.assets/image-20200426180005490.png)

![image-20200426180034732](index.assets/image-20200426180034732.png)

![image-20200426180051515](index.assets/image-20200426180051515.png)

![image-20200426180115331](index.assets/image-20200426180115331.png)

## 问题

### 报错问题

请把MSBuild加入信任

![image-20200426181258545](index.assets/image-20200426181258545.png)

![image-20200426181304815](index.assets/image-20200426181304815.png)

### AppSettings的值问题

![image-20200426181354104](index.assets/image-20200426181354104.png)

![image-20200426181427263](index.assets/image-20200426181427263.png)