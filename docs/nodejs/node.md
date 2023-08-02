## 安装Node

打开[NodeJS官网](https://nodejs.org), 安装LTS稳定版本

!> 这里安装的版本号,具体要以公司正在使用的版本为标准来进行安装

!> 如需安装指定版本的Nodejs,输入以下网址并更改版本号安装即可[传送门](https://nodejs.org/dist/v16.18.1/)

```text
https://nodejs.org/dist/v16.18.1/
```

检查是否安装成功,在dos中执行 `node -v` 命令,出现版本号代表安装成功

```shell
node -v 
```

## 安装Npm的镜像源管理工具

```shell
npm install -g nrm
```

## 查看当前可使用的镜像

```shell
nrm ls
```

## 使用其中的一个镜像 

```shell
nrm use taobao
```

## 检查是否镜像是否使用成功

```shell
npm config get registry
```

!> 至此, 完整的NodeJs环境搭建就完成了, NodeJs中文文档官网[传送门](https://www.nodeapp.cn/)

