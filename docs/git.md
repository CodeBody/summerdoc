# Git详解

## 初始化

```shell
git init
```

## 关联本地的.gitignore文件

```shell
git config core.excludesfile .gitignore 
```

## 添加缓存文件

```shell
git add .
```

## 提交本地修改

```shell
git commit -m '第一次修改'
```

## 本地关联到远程仓库

```shell
git remote add origin <你的仓库地址>
```

## 提交到远程仓库

```shell
git push -u origin main
```

## 查看当前分支

```shell
git branch
```

## 查看当前git状态

```shell
git status
```

## 创建分支并切换

```shell
git checkout -b <分支名称>
```

## 合并分支

要先切回主线

```shell
git checkout main
git merge <分支名称>
```

