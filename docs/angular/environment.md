## 安装Node

!> 如果本地没有安装nodeJs 请先移步安装Nodejs[传送门](/docs/nodejs/node.md)

## 安装Angular-cli

dos中执行 `npm install -g @angular/cli` 命令来安装Angular-cli

```shell
npm install -g @angular/cli
```

> MAC终端如果提示没有权限, 则在命令前面加上 **sudo** 然后输入密码回车即可

检查是否安装成功, 在dos中执行 `ng version`命令,出现版本号则代表安装成功

!> 这里安装的版本号 具体要以公司正在使用的版本为标准来进行安装

## 创建项目

在dos中执行 `ng new demo` 命令来创建一个Angular项目 

```shell
ng new demo
```

当dos中出现 `packages installed successfully` 字样 则代表项目已经创建成功

## 运行项目

在dos中, 先进入项目目录 然后执行 `npm run strat` 命令来启动项目

```shell
cd demo
npm run strat
```

项目启动成功之后 在浏览器中打开 [http://localhost:4200](http://localhost:4200) 

!> 至此, 完整的环境搭建就完成了, Angular更多语法请移步[Angular官网](https://angular.cn/), 预祝大家工作愉快 :blush:
