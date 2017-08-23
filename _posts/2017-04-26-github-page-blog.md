---
layout: post
title:  使用github-page、jekyll搭建独立博客（二）
date:   2017-4-26 15:36:28 +0800
categories: 技术分享
tag:
    - blog
    - jekyll
    - Github Pages
---

* content
{:toc}


    使用jekyll能快速的搭建出美观、好用的博客，而github-page更是直接支持编译jekyll博客。

    github-page可以免费托管静态页面，并提供二级访问地址，如果有需要也可以绑定自己的域名。

通过上一篇文章的操作，已经在本地搭建了一个jekyll的环境，并且和Github Pages中的环境一致，这次我们只需要将本地代码提交到Github中即可将博客发布到互联网上。

注册Github账户、使用Git等问题，就不再累述，自行Google、Baidu。

在Github上创建一个新的 repository，repository的名字命名为 username.github.io,其中username是你Github的用户名。
如果这个repository的命名没有和你的用户名对应上，Github Pages便不会工作。
![创建]({{ '/styles/images/create_repository.jpg' | prepend: site.baseurl  }})

创建完成后，将此repository用git clone到本地项目文件夹（就是上篇文章里jetyll的工作目录）。
再将文件夹里所有文件push到master中。

_site文件夹是jetyll生成出的网页文件，Github Pages和你的本地环境一致，也会自动将代码编译生成到_site文件夹中，
所以我们不必将_site文件夹上传上去，一切等着Github Pages自动处理。

.gitignore是git用来排除某些不用上传的文件，在.gitignore中已经有声明了_site文件夹。我们在commit时会自动排除的。