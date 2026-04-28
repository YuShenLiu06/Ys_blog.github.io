# 在cent os 7.6中安装mcdr和mcsm

## 安装并配置mcsm

在控制台执行这一串指令`sudo su -c "wget -qO- https://script.mcsmanager.com/setup_cn.sh | bash" `下载mcsm

## 1.下载并配置我的世界服务端（如果你已经有了服务端，则可以忽略）

## 2.下载轩辕镜像到服务器上

使用指令`bash <(wget -qO- https://xuanyuan.cloud/docker.sh)`安装轩辕镜像，并且安装docker

同时去[官网](https://docker.xuanyuan.me/)注册，有条件的可以充7块钱买流量包，也可以直接使用免费的镜像加速

## 3.安装docker镜像

mcdr的docker的image源 `mcdreforged/mcdreforged-corretto:latest`

在你的docker界面上搜索该镜像，然后使用对应的pull指令

> 如果无法连接，去服务器提供商出打开8080端口

## 4. 在mcsm上应用该镜像和初始化mcdr

1. 在mcsm点击新建应用（选不选mc都一样）可以选择压缩包上传服务端压缩包，
2. 在实例中点击应用实例设置
3. 启动命令输入 `mcdreforged init`
4. 容器化->打开端口25565 
5. 选择我们刚刚pull下来的docker image 
6. 点击运行实例
7. 将服务器主体文件转移进刚刚创建的文件夹server下
8.  `config.yml`配置 `star-command` 为你的启动指令

## 安装完毕，恭喜🎉