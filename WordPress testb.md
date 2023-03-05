---
title: WordPress搭建个人博客教程
date: 2023-02-28 18:20:20
author: hefanx
cover: https://cdn.staticaly.com/gh/hefanx/blog-tuchuang@master/img/WordPress%E6%90%AD%E5%BB%BA%E5%8D%9A%E5%AE%A2.jpg
tags:
  - WordPress
  - 搭建博客
---
1. 首先需要在服务器上安装宝塔面板，宝塔面板安装教程请参考下面这篇文章。

[宝塔面板国际版aapanel安装教程](https://blog.hefan64.tk/2023/02/28/%E5%AE%9D%E5%A1%94%E9%9D%A2%E6%9D%BF%E5%9B%BD%E9%99%85%E7%89%88aapanel%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B/)

2. 在cloudfare上解析一个域名，按win+R，输入cmd，然后再按Enter键，在命令提示符面板里ping一下刚才解析的域名，如果可以ping通说明域名已经解析好了。
3. 打开宝塔面板——点击网站——添加站点，填写站点配置信息如下：

- 域名：填写刚才解析的域名
- 数据库：选择MySQL，数据库账号密码选择默认就可以
- PHP版本：选择PHP-74
- 记得先把数据库的账号和密码复制保存到记事本上，后面需要用到。

4. 完成上述配置后点击提交，然后打开刚添加的域名——域名管理——再次点击刚添加的域名——打开后如果显示“恭喜，站点创建成功”，就可以给站点配置SSL证书了。
5. 点击网站——点击刚添加的域名——SSL——Let's Encrypt——选中刚添加的域名——点击申请，然后宝塔面板就会自动帮我们申请SSL证书——保存——开启强制HTTPS。
6. 点击网站——根目录——删除根目录下的全部文件——打开WordPress中文官网——获取WordPress——选择下载最新版的WordPress压缩包（建议选择下载tar.gz格式的压缩包）。
7. 点击网站——根目录——上传刚才下载的WordPress压缩包——右键解压WordPress压缩包——删除WordPress压缩包——打开WordPress文件夹——把全部文件剪切到根目录下——删除WordPress空文件夹。
8. 点击网站——点击刚添加的域名——域名管理——再次点击刚添加的域名——来到WordPress安装向导页面——点击现在就开始——填写数据库配置信息如下：

- 数据库名：填写网站的域名
- 用户名：复制粘贴刚才保存的数据库账号
- 密码：复制粘贴刚才保存的数据库密码

备注：记得先打开宝塔面板——数据库查看一下是否已经创建了数据库，如果没有则先点击root密码——修改root密码，再创建一个数据库，然后再执行上述操作。

9. 完成上述配置信息后点击提交——运营安装程序——填写网站的配置信息如下：

- 站点标题：my blog （可以自定义）
- 用户名：my blog （可以自定义）
- 密码：建议设置的复杂一点（可以自定义）
- 您的电子邮件地址：填写自己的邮箱

10. 完成上述配置信息后点击安装WordPress——跳转到WordPress登录页面，填写WordPress账号和密码就可以登录WordPress后台了——点击左上角的my blog就可以来到WordPress前台。
11. 安装自己需要的WordPress主题和插件，至此WordPress搭建个人博客就完成了。

![img](https://cdn.staticaly.com/gh/hefanx/blog-tuchuang@master/img/WordPress%E6%90%AD%E5%BB%BA%E5%8D%9A%E5%AE%A2.jpg)
