---
title: zhengqihui
date: 2022-11-06 20:11:23
tags:
---

## 标签插件

### 引用块

{% blockquote line_threshold:1 %}
没有提供参数，则只输出普通的 blockquote
{% endblockquote %}

{% blockquote David Levithan, Wide Awake %}
引用书上的句子
{% endblockquote %}
</br>
{% blockquote @DevDocs https://twitter.com/devdocs/status/356095192085962752 %}
引用 Twitter
{% endblockquote %}

### 代码块

{% codeblock %}
alert('Hello World!');
{% endcodeblock %}

{% codeblock lang:objc wrap:false %}
[rectangle setX: 10 y: 10 width: 20 height: 20];

<table>
    <thead>
        <tr>
            <th colspan="2">The table header</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>The table body</td>
            <td>with two columns</td>
        </tr>
    </tbody>
</table>
{% endcodeblock %}

{% codeblock Array.map %}
array.map(callback[, thisArg])
{% endcodeblock %}

{% codeblock _.compact lang:objc http://underscorejs.org/#compact Underscore.js line_number:true line_threshold:1 highlight:true first_line:10 mark:10,20 %}
_.compact([0, 1, false, 2, '', 3]);
=> [1, 2, 3]
_.compact([0, 1, false, 2, '', 3]);
=> [1, 2, 3]
_.compact([0, 1, false, 2, '', 3]);
=> [1, 2, 3]
_.compact([0, 1, false, 2, '', 3]);
=> [1, 2, 3]


_.compact([0, 1, false, 2, '', 3]);
=> [1, 2, 3]
_.compact([0, 1, false, 2, '', 3]);
=> [1, 2, 3]
{% endcodeblock %}

### 反引号代码块
```
alert('Hello World!');
```

```objc
[rectangle setX: 10 y: 10 width: 20 height: 20];
```

```_ Array.map http://underscorejs.org/#compact url
array.map(callback[, thisArg])
```

{% pullquote [class] %}
content
{% endpullquote %}

