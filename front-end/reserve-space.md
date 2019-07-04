# 保留空格

html 代码中的空格有时会被浏览器忽略，通常有以下两种情况:
1. 元素内容开头结尾处的空格会被完全忽略
2. 元素内容中间的多个连续空格会被合并为一个。

## 保留空格的方法
### 使用`&nbsp;`代替空格
**注意：有时候字符串中的`&nbsp;`是不会被转义的**
```html
<p>首&nbsp;&nbsp;&nbsp;尾</p> // 显示为： 首     尾
<p>"首&nbsp;&nbsp;&nbsp;尾"</p> // 有时候显示为：首&nbsp;&nbsp;&nbsp;尾
```




### 使用`<pre>` 标签包裹内容
代码：
```html
<pre>
   hello
       world
             !
</pre>
```
显示:
<pre>
   hello
       world
             !
</pre>
### CSS： white-space: pre
 [white-space](https://developer.mozilla.org/zh-CN/docs/Web/CSS/white-space) 属性设置如何处理元素内的空白，有 6 个值
 - **inherit**: 继承父元素
 - **normal**: 默认值，浏览器以正常方式显示空格——忽略头尾空格，合并中间空格。内容超出容器会自动换行显示。
 - **nowrap**: 禁止换行，内容超出容器也不换行。
 - **pre**: 按照`<pre>`标签的方式处理，保留所有空格和换行，内容超出容器也不换行。
 - **pre-wrap**: 保留所有空格和换行，但是内容超出容器自动换行。。
 - **pre-line**: 只保留换行符，其他显示方式同 normal。

