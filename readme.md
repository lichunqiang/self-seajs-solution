pjax+seajs
----------------

### 为什么是pjax

如果你使用chrome等浏览器访问Github时，你会发现页面之间的点击是通过ajax异步请求的，同时页面URL也放生了变化。
并且能够很好的支持浏览器的前进与后退。

更多请看这篇博文：http://www.welefen.com/use-ajax-and-pushstate.html

### 与ajax的不同

传统的ajax有如下的问题：

1、可以无刷新改变页面内容，但无法改变页面URL

2、为了更好的可访问性，内容发生改变后，通常改变URL的hash

3、hash的方式不能很好的处理浏览器的前进、后退等问题

4、进而浏览器引入了onhashchange的接口，不支持的浏览器只能定时去判断hash是否改变

5、但这种方式对搜索引擎很不友好

6、twitter和google约定了使用#!xxx（即hash第一个字符为!），搜索引擎进行支持。

为了解决传统ajax带来的问题，HTML5里引入了新的API，即：history.pushState, history.replaceState

可以通过pushState和replaceState接口操作浏览器历史，并且改变当前页面的URL。

pushState是将指定的URL添加到浏览器历史里，replaceState是将指定的URL替换当前的URL。

### 查看效果

1. 未打包效果查看

http://blog.weifanfou.com/self-seajs-solution/index.html?dev

2. 查看打包后的效果

http://blog.weifanfou.com/self-seajs-solution/index.html

### 原理

可查看源代码，非常简单