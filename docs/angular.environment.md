# 安装Node

打开[NodeJS官网](https://nodejs.org), 安装LTS稳定版本

检查是否安装成功, dos中输入 `node -v`  出现版本号代表安装成功

```shell
node -v 
```

!> 这里安装的版本号 具体要以公司正在使用的版本为基准 进行安装

# 配置Npm

> 配置Npm的网络代理

```shell
npm config set registry https://registry.npm.taobao.org/
```

检查是否配置成功, 在dos中输入 `npm config get registry` 出现设置的淘宝的地址代表配置成功

```shell
npm config get registry
```

# 安装Angular-cli

dos中输入 `npm install -g @angular/cli` 安装Angular-cli

```shell
npm install -g @angular/cli
```

> MAC终端如果提示没有权限, 则在命令前面加上 **sudo** 然后输入密码回车即可

检查是否安装成功, 在dos中输入 `ng version` 出现版本号则代表安装成功

!> 这里安装的版本号 具体要以公司正在使用的版本为基准 进行安装

# 创建项目

使用 `ng new demo` 命令来创建一个Angular项目 

```shell
ng new demo
```

当dos中出现 `packages installed successfully` 代表创建成功

# 运行项目

在dos中, 先进入项目目录 然后运行 `npm run strat` 来启动项目

```shell
cd demo
```

```shell
npm run strat
```

项目启动成功之后 在浏览器中打开 [http://localhost:4200](http://localhost:4200) 

至此, 完整的环境搭建就完成了, 预祝大家工作愉快 :blush:
