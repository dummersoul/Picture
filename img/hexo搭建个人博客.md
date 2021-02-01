---
title: hexo搭建个人博客
date: 2020-10-28 00:32:16
tags: hexo
aplayer: false
cover: /img/2.jpg
type: artitalk
---



```bash
hexo new "postName" #新建文章 
hexo new page "pageName" #新建页面
hexo help # 查看帮助 
hexo version #查看Hexo的版本

hexo n == hexo new 
hexo g == hexo generate 
hexo s == hexo server 
hexo d == hexo deploy

hexo s -g #生成并本地预览 
hexo d -g #生成并上传
```





## seo优化

### 百度收录

site:dummersoul.top

搜索后啥也没有，因为还未收录，在[百度资源站点管理](https://ziyuan.baidu.com/site/siteadd#/) 里添加我的网站，再选择一种方式验证（我用的CNAME验证）



在阿里云域名管理里添加一条解析

![image-20210113132605714](https://raw.githubusercontent.com/dummersoul/Picture/main/img/image-20210113132605714.png)

添加完成后，点击“完成验证”

![image-20210113132545741](https://raw.githubusercontent.com/dummersoul/Picture/main/img/image-20210113132545741.png)

### 生成sitemap

安装sitemap插件

```bash
npm install hexo-generator-sitemap --save     
npm install hexo-generator-baidu-sitemap --save
```

修改_config.yml配置文件，将url改为自己的url

```
url: https://dummersoul.top
```

**执行完之后就会在网站根目录生成sitemap.xml文件和baidusitemap.xml文件**

![image-20210113152149761](https://raw.githubusercontent.com/dummersoul/Picture/main/img/image-20210113152149761.png)

然后hexo g && hexo d 

网页可以直接访问baidusitemap.xml

然后将这个sitemap文件提交给[百度收录网址](https://ziyuan.baidu.com/linksubmit/index?site=https://dummersoul.top/)

![image-20210113140716156](https://raw.githubusercontent.com/dummersoul/Picture/main/img/image-20210113140716156.png)

等待收录成功就可以了。



### 谷歌收录

其实谷歌收录步骤和百度一样，先进行验证，再直接提交sitemap文件即可

[谷歌收录地址](https://www.google.com/webmasters/tools/home?hl=zh-CN)

![image-20210113152649434](https://raw.githubusercontent.com/dummersoul/Picture/main/img/image-20210113152649434.png)

![image-20210113152737430](https://raw.githubusercontent.com/dummersoul/Picture/main/img/image-20210113152737430.png)

添加DNS解析记录

![image-20210113153002998](https://raw.githubusercontent.com/dummersoul/Picture/main/img/image-20210113153002998.png)

![image-20210113152906340](https://raw.githubusercontent.com/dummersoul/Picture/main/img/image-20210113152906340.png)

添加sitemap

![image-20210113153156720](https://raw.githubusercontent.com/dummersoul/Picture/main/img/image-20210113153156720.png)

![image-20210113153237254](https://raw.githubusercontent.com/dummersoul/Picture/main/img/image-20210113153237254.png)

谷歌的效率比百度高几百倍，等都不用等的，就直接成功了。



## 参考

https://cloud.tencent.com/developer/article/1435802