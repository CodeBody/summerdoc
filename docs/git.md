# Git详解

## 创建目录

```shell
mkdir git-test
```

## 初始化git

```shell
git init
```

## 添加.gitignore文件 并关联它

在当前目录下手动创建一个 .gitignore 文件

```shell
git config core.excludesfile .gitignore 
```

## 添加文件

在当前目录下手动创建一个MD文件 比如: git-test.md 然后执行下面命令添加到本地Git中去

```shell
git add .
```

## 提交本地修改

```shell
git commit -m '第一次修改'
```

## 创建远程仓库

首先你需要在[Gitee](https://gitee.com)或者[Github](https://github.com)上创建一个远程仓库

![Git仓库创建](http://rxpnrskwv.hn-bkt.clouddn.com/images/gitrepositorycreate.jpg)

## 本地关联到远程仓库

```shell
 git remote add origin <你的仓库地址>
```

## 提交到远程仓库

```shell
git push -u origin main
```


