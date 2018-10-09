---
title: hexo安装、常用指令、更换主题、文章分类
date: 2018-10-08 21:21:29
categories:
- hexo专题
tags:
- hexo
- web前端
---

## hexo 安装
实验环境： hexo 3.7.1

安装真的简单，直接按官网教程来：

    npm install hexo-cli -g
    hexo init <folder>
    cd <folder>
    npm install
    hexo server

安装完毕，如果是本地起的测试环境，直接可以通过 <http://localhost:4000> 访问。

## hexo常用指令

    生成静态文件：hexo generate 或 hexo g
    发表草稿：hexo publish [layout] <filename>
    启动服务器：hexo server 或 hexo s
    部署：hexo deploy 或 hexo d
    渲染文件：hexo render <file1> [file2] ...
    清除缓存文件 (db.json) 和已生成的静态文件 (public)：hexo clean



## 换主题--以aath为例
按装依赖：`npm install --save hexo-renderer-sass`

下载主题到themes文件夹下(注意路径，aath位于themes文件下)：`git clone -b master https://github.com/lewis-geek/hexo-theme-Aath.git themes/aath`


## 创建文章分类

    hexo new page categories
    
会在source目录下生成/categories/index.md
修改文件categories/index.md内容如下：
    
    
    ---
    title: 文章分类
    date: 2018-10-08 21:21:29
    type: "categories"
    ---
    
创建文章时，给文章添加"categories"属性。

    ---
    title: XXX文章标题XXX
    date: 2018-10-08 21:21:29
    categories: 
    - hexo专题
    ---
    
## 创建 标签
    hexo new page tags
会在source目录下创建/tags/index.md
修改文件内容如下：

    ---
    title: 标签
    date: 2018-10-08 21:52:46
    layout: tags
    ---

创建文章时，给文章添加"tags"属性

    ---
    title: XXX文章标题XXX
    date: 2018-10-08 21:21:29
    categories: 
    - hexo专题
    tags:
    - hexo
    - web前端
    ---



