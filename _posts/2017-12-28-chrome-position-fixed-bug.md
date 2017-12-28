---
layout:     post
title:      低版本下Chrome浏览器position:fixed定位问题
category: blog
description: 低版本下Chrome浏览器子元素position:fixed会相对于父元素定位而不是屏幕
---


父元素为绝对定位且有动画transform属性，子元素为position:fixed定位，则在低版本chrome浏览器（测试环境版本为41）下子元素是相对于父元素定位的而不是相对于屏幕定位，导致渲染错误，这时候可以把动画属性去掉，可以在页面动画完成后手动remove动画属性。