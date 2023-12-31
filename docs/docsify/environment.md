# docsify环境搭建,部署与优化

!> 在此之前,先确保本机已经安装了NodeJs

在dos中执行 `node -v` 命令,出现版本号则代表已经安装成功。否则请先移步到[NodeJs安装](/docs/nodejs/node.md)

```shell
node -v
```

## 安装docsify-cli

在dos中执行 `npm i docsify-cli -g` 命令来安装docsify-cli

```shell
npm i docsify-cli -g
```

检查是否安装成功, 在dos中执行 `docsify -v` 命令,出现版本号则代表已经安装成功

```shell
docsify -v
```

## 创建项目

在dos中执行 `docsify init docsify-test` 命令来创建项目 这里**docsify-test**为项目名称, 由用户自己定义

```shell
docsify init docsify-test
```

项目创建成功之后, 进入到当前的目录, 显示当前的目录结构

```shell
cd docsify-test
ls -all
```

里面的文件如下

```text
index.html -- 这个是我们的入口文件, 也是全局的配置文件, 在里面可以配置页面的侧边栏, 导航栏, 全局主题等等
README.md  -- 这个是我们的首页, 会做为主页内容渲染
.nojekyll  -- 这个是用于阻止 GitHub Pages 忽略掉下划线开头的文件(这个文件默认隐藏)
```

## 启动项目

在当前目录下, 执行 `docsify serve` 命令,来启动当前项目

```shell
docsify serve
```

启动成功之后, 会生成一个**http://localhost:端口号**的网址, 直接拷贝网址在浏览器上打开即可

!> 至此, 完整的环境搭建就完成了。 具体docsify的配置和用法请参考[docsify官网](https://docsify.js.org)








