# 设置特定文件在 git diff 的时候不显示具体内容差异

有时候 git commit 的内容包含由机器产生的文本文件，这些文件的 diff 信息很多，占据太多的屏幕空间，我们可以将这些文件作为二进制数据被对待，不显示具体内容差异。

**具体实现：**

新建`.gitattributes`文件，
将不需要显示具体内容差异的文件当成二进制文件，例如`build/` 目录下面的所有文件，
可在`.gitattributes`文件增加
```
build/* -crlf -diff
```


当你在项目中运行git show或git diff时，不会比较不同的内容。

在Git 1.6及之后的版本中，可以用一个宏`binary`代替`-crlf -diff`。

以下写法和 `build/* -crlf -diff` 等价
```
build/* binary
```

修改`build/` 目录下的文件，运行 `git diff` 只提示 Binary files ... deffer, 没有具体信息，eg.
<pre>
> git diff
diff --git a/build/index.js b/build/index.js
index 4668562..ed0a8d2 100644
Binary files a/build/index.js and b/build/index.js differ
</pre>





***

refer to [自定义 Git - Git属性](https://git-scm.com/book/zh/v1/%E8%87%AA%E5%AE%9A%E4%B9%89-Git-Git%E5%B1%9E%E6%80%A7)
