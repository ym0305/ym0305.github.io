---
title: hexo配置静态个人博客
date: 2019-09-27 23:12:16
tags: 教程
---

### Windows下面配置  hexo 

<!-- more -->

### 第一步--安装

1. 首先要安装 [git](https://git-scm.com/download/win) ，因为 hexo 很多操作都涉及命令行，所以还要配置 git 的环境变量
   - 配置 git 的环境变量
   - 打开系统属性里面的环境变量
   - 选择系统变量 path 
   - 添加 `/安装路径/git/cmd` 例如我的就是 `C:\Program Files\Git\cmd` 
2. 安装 [Node.js](https://nodejs.org/en/) ，并记得在安装步骤勾选 add Path 这个选项
3. 上两步完成后可以安装 hexo了，使用 `$npm install -g hexo-cli` 命令安装 hexo ，并等待安装完成

### 第二步--建站

1. 用 `cd` 命令进入到你想把 hexo 保存的路径 ，例如 `D:\` 下面

2.  然后执行以下命令 

   ```bash
   $hexo init <你想要的文件名>
   cd <文件名>
   npm install
   ```

   这些命令会在你的文件夹下面新建所需要的文件

3. 然后到目录下面找到 `_config.yml` 中配置博客的信息了

   快速搭建只需要修改下面这些信息就行了

   | 参数        | 描述       | 值（例子） |
   | ----------- | ---------- | ---------- |
   | title       | 网站标题   | JOJO的博客 |
   | subtitle    | 网站副标题 | JOJO       |
   | description | 网站描述   | 技术 JOJO  |
   | author      | 你的名字   | JOJO       |
   | url         | 网址       | 你的域名   |

### 第三步--在本地生成服务器

1. 在 hexo 目录下执行 ` $hexo generate` 命令生成静态文件，该命令也可以简写成 ` $hexo g` 
2. 然后执行 ` $hexo deploy` 部署网站，也可以简写成 ` $hexo d` 
3. 最后启动服务器，执行 ` hexo server` ，然后就可以访问了，访问的默认地址为 `localhost:4000`   

至此，在 Windows 本地情况下配置 hexo 个人博客就是这样做了！

**接下来就是部署到 ` github` 上面，利用 `githubPage` ，实现我们的个人博客在网上也能访问**

