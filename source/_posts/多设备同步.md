---
title: I move my hexo to another computer!
date: 
comments: true
categories: Hexo
---

# Record Life.

​	This blog is to test how to write blogs on multi-device.

<!--more-->

## 更换电脑操作

一样的，跟之前的环境搭建一样，

- ## 安装git

```text
sudo apt-get install git
```

- ## 设置git全局邮箱和用户名

```text
git config --global user.name "yourgithubname"
git config --global user.email "yourgithubemail"
```

- ## 设置ssh key

```text
ssh-keygen -t rsa -C "youremail"
#生成后填到github和coding上（有coding平台的话）
#验证是否成功
ssh -T git@github.com
ssh -T git@git.coding.net #(有coding平台的话)
```

- ## 安装nodejs

```text
sudo apt-get install nodejs
sudo apt-get install npm
```

- ## 安装hexo  

```text
sudo npm install hexo-cli -g
```

但是已经不需要初始化了，

直接在任意文件夹下，

```text
git clone git@………………
```

然后进入克隆到的文件夹：

```text
cd xxx.github.io
npm install
npm install hexo-deployer-git --save
```

生成，部署：

```text
hexo g
hexo d
```



## Tips: 然后就可以开始写你的新博客了

```text
hexo new newpage
```

​	1. 不要忘了，每次写完最好都把源文件上传一下

```text
git add .
git commit –m "xxxx"
git push 
```

​	2. 如果是在已经编辑过的电脑上，已经有clone文件夹了，那么，每次只要和远端同步一下就行了

```text
git pull
```