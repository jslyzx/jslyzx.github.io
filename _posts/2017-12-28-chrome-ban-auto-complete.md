---
layout: post
title: 关于chrome禁用密码自动填充
description: chrome有很多人性化的设计，样式也比较好看，但是有的时候这反而会带来困扰，比如密码自动填充会带来一个很丑的黄色背景
category: blog chrome html
---

chrome会自动给密码框加样式，主要是背景：
```
input:-webkit-autofill,
textarea:-webkit-autofill, 
select:-webkit-autofill {    
    background-color: rgb(250, 255, 189);    
    background-image: none;    
    color: rgb(0, 0, 0);
}
```
第一种方法当然是覆盖这个样式。
第二种方法是在旧版的谷歌浏览器中，可以使用以下方法:
```html
<form autocomplete="off">
```
或者
```html
<input autocomplete="off">
```
But,在新版的谷歌浏览器中，autocomplete=”off”已经失效，需要尝试以下方法:
```html
<!-- fake fields are a workaround for chrome autofill getting the wrong fields -->
<input style="display:none" type="text" name="fakeusernameremembered"/>
<input style="display:none" type="password" name="fakepasswordremembered"/>
```
用法是在form表单的加入这两句代码，然后name需要改成将要禁止填充的input。其原理是，谷歌浏览器会自动填充这个input，而不会填充你代码中实际展示的input，从而绕过谷歌浏览器的自动填充功能。

参考以下两个博客：

*[blog.csdn.net](http://blog.csdn.net/xiaoluodecai/article/details/53190489 "如何禁止谷歌浏览器自动填充密码")
*[stackoverflow.com](https://stackoverflow.com/questions/15738259/disabling-chrome-autofill "disabling-chrome-autofill")