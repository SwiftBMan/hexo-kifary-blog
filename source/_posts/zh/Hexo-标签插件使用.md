---
title: Hexo 标签插件使用
date: 2022-11-06 20:57:12
mathjax: false
mermaid: false
header: true
post_link: ''
description: 如何在 Hexo 博客中使用标签插件
sidebar: true
sticky: 10
tags:
  - Hexo
categories:
  - Hexo
---

### 引用块

{% blockquote %}
\{\% blockquote [author[, source]] [link] [source_link_title] \%\}</br>
content</br>
\{\% endblockquote \%\}
{% endblockquote %}

#### 例子

##### 没有提供参数，普通的 **blockquote**

{% blockquote %}
\{\% blockquote \%\}</br>
普通的 blockquote</br>
\{\% endblockquote \%\}
{% endblockquote %}

{% blockquote %}
普通的 blockquote
{% endblockquote %}

##### 引用书上的句子

{% blockquote %}
\{\% blockquote David Levithan, Wide Awake \%\}</br>
Do not just seek happiness for yourself. Seek happiness for all. Through kindness. Through mercy.</br>
\{\% endblockquote \%\}
{% endblockquote %}

{% blockquote David Levithan, Wide Awake %}
Do not just seek happiness for yourself. Seek happiness for all. Through kindness. Through mercy.
{% endblockquote %}

##### 引用链接

{% blockquote %}
\{\% blockquote Seth Godin http://sethgodin.typepad.com/seths_blog/2009/07/welcome-to-island-marketing.html Welcome to Island Marketing \%\}</br>
Every interaction is both precious and an opportunity to delight.</br>
\{\% endblockquote \%\}
{% endblockquote %}

{% blockquote Seth Godin http://sethgodin.typepad.com/seths_blog/2009/07/welcome-to-island-marketing.html Welcome to Island Marketing %}
Every interaction is both precious and an opportunity to delight.
{% endblockquote %}

### 代码块
{% quote %}
\{\% codeblock [title] [lang:language] [url] [link text] [additional options] \%\}</br>
code snippet</br>
\{\% endcodeblock \%\}
{% endquote %}

#### 例子

##### 普通代码块
{% blockquote %}
\{\% codeblock \%\}</br>
alert(\'Hello World!\');</br>
\{\% endcodeblock \%\}
{% endblockquote %}

{% codeblock %}
alert('Hello World!');
{% endcodeblock %}

##### 一个参数完整的代码块

{% blockquote %}
\{\% codeblock 这是一个 oc 代码 lang:objc http://www.baidu.com 百度搜索 line_number:true line_threshold:0 highlight:true first_line:0 mark:1 wrap:true \%\}</br>
[rectangle setX: 10 y: 10 width: 20 height: 20];</br>
[rectangle setX: 10 y: 10 width: 20 height: 20];</br>
\{\% endcodeblock \%\}
{% endblockquote %}

{% codeblock 这是一个 oc 代码 lang:objc http://www.baidu.com 百度搜索 line_number:true line_threshold:0 highlight:true first_line:0 mark:1 wrap:true %}
[rectangle setX: 10 y: 10 width: 20 height: 20];
[rectangle setX: 10 y: 10 width: 20 height: 20];
{% endcodeblock %}

### jsFiddle

在文中嵌入[jsFiddle](https://jsfiddle.net)，[jsFiddle](https://jsfiddle.net)是一款HTML, CSS, JAVASCRIPT在线调试工具
{% blockquote %}
\{\% jsfiddle shorttag [tabs] [skin] [width] [height] \%\}</br>
\{\% jsfiddle Kifary/zp6n3sh0/1  js,html,css,result light \%\}
{% endblockquote %}

### Gist
{% blockquote %}
\{\% gist 35b1d8ab0323a44c289b62f365b7a302 test1 \%\}</br>
\{\% gist 35b1d8ab0323a44c289b62f365b7a302 test2 \%\}
{% endblockquote %}

### iframe
使用 iframe 嵌入 [bilibili](https://www.bilibili.com) 视频
{% blockquote %}
\{\% iframe url [width] [height] \%\}</br>
\{\% iframe //player.bilibili.com/player.html?aid=730017073&bvid=BV11D4y167FQ&cid=819030469&page=1 930 542 \%\}
{% endblockquote %}
{% iframe //player.bilibili.com/player.html?aid=730017073&bvid=BV11D4y167FQ&cid=819030469&page=1 930 542 %}

使用 iframe 嵌入 [网易云音乐](https://music.163.com)

{% blockquote %}
\{\% iframe //music.163.com/outchain/player?type=0&id=2309983541&auto=1&height=430 330 450 \%\}</br>

\{\% iframe //music.163.com/outchain/player?type=0&id=2320041657&auto=1&height=90 330 110 \%\}</br>

\{\% iframe //music.163.com/outchain/player?type=0&id=2320041657&auto=1&height=32 298 52 \%\}
{% endblockquote %}
{% iframe //music.163.com/outchain/player?type=0&id=2309983541&auto=1&height=430 330 450 %}

{% iframe //music.163.com/outchain/player?type=0&id=2320041657&auto=1&height=90 330 110 %}

{% iframe //music.163.com/outchain/player?type=0&id=2320041657&auto=1&height=32 298 52 %}

### Image
{% blockquote %}
\{\% img [class names] /path/to/image [width] [height] '"title text" "alt text"' \%\}</br>
\{\% img https://cdn.jsdelivr.net/gh/SwiftBMan/iFigureBed/Blogs/Kifary/android-chrome-512x512.png 100 100 \%\}
{% endblockquote %}

{% img https://cdn.jsdelivr.net/gh/SwiftBMan/iFigureBed/Blogs/Kifary/favicon.ico 44 44 %}

### Link
{% blockquote %}
\{\% link text url [external] [title] \%\}</br>
\{\% link 百度一下 https://www.baidu.com [external] [超连接] \%\}
{% endblockquote %}

{% link 百度一下 https://www.baidu.com [external] [超连接] %}

### Include Code
{% blockquote %}
\{\% include_code [title] [lang:language] [from:line] [to:line] path/to/file \%\}</br>
\{\% include_code file lang:javascript from:1 to:20 file.js \%\}
{% endblockquote %}
{% include_code file lang:javascript from:1 to:20 file.js %}

### Youtube
{% blockquote %}
视频</br>
\{\% youtube lJIrF4YjHfQ \%\}</br>
播放列表</br>
\{\% youtube PL9hW1uS6HUfscJ9DHkOSoOX45MjXduUxo 'playlist' \%\}</br>
禁止 YouTube cookie</br>
\{\% youtube lJIrF4YjHfQ false \%\}</br>
\{\% youtube PL9hW1uS6HUfscJ9DHkOSoOX45MjXduUxo 'playlist' false \%\}
{% endblockquote %}

### [引用文章](https://hexo.io/zh-cn/docs/tag-plugins#引用文章)
{% blockquote %}
\{\% post_path Hexo-标签插件使用 false \%\}</br>
\{\% post_link Hexo-标签插件使用 '<b>插件使用</b>' false \%\}
{% endblockquote %}

{% post_path Hexo-标签插件使用 false %}</br>
{% post_link Hexo-标签插件使用 插件使用 false %}

### [Embed image](https://hexo.io/zh-cn/docs/tag-plugins#Embed-image)

### [Raw](https://hexo.io/zh-cn/docs/tag-plugins#Raw)

### [文章摘要和截断](https://hexo.io/zh-cn/docs/tag-plugins#文章摘要和截断)

