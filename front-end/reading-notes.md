# 订阅邮件阅读笔记

> [Using the DOM like a Pro](https://itnext.io/using-the-dom-like-a-pro-163a6c552eba)

`querySelector` 和 `querySelectorAll` 模仿了jQuery `$` 函数。

`querySelectorAll` 返回的是静态的类数组 `NodeList`；不会随DOM的变化动态改变
 
 `getElementsByTagName`，`getElementsByClassName`返回的是动态的类数组 `HTMLCollection`，会随DOM的变化动态改变
 
![nodeList-vs-HTMLCollection](./nodeList-vs-HTMLCollection.png)

