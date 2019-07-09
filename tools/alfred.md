# alfred

"Alfred 太好用了！"，感觉我用电脑的时候已经完全离不开 Alfred 了。
## 打开应用
`⌘ + space` 唤醒Alfred，直接输入应用名

## file Search
 - `find + 关键字`：搜索文件并在 finder 中显示
 - `open + 关键字`：搜索文件并打开
 - `in + 关键字`：搜索文件内容，这个厉害了，如果你只记得文件的部分内容想找到这个文件也可以用这个功能。

## Clipboard 剪贴板
可以选择剪贴板历史内容粘贴在指定位置，避免重复的复制操作
我的快捷键设置:`⌥⌘V`

## web Search
 内置了很多常用的搜索,基本已经够用了

 也可以增加自定义的搜索，下面是我的一些设置, 直接在浏览器打开下面想添加的搜索的`alfred://**`链接，根据提示操作即可，只需要两次确认操作，非常简单。
- **github**: `alfred://customsearch/Search%20github%20for%20%7Bquery%7D/gh/utf8/nospace/https%3A%2F%2Fgithub.com%2Fsearch%3Futf8%3D%25E2%259C%2593%26q%3D%7Bquery%7D`
- **stack overflow**: `alfred://customsearch/Search%20stackoverFlow%20for%20%7Bquery%7D/stof/utf8/nospace/http%3A%2F%2Fwww.stackoverflow.com%2Fsearch%3Fq%3D%7Bquery%7D`
- **explainShell**: 搜索shell命令的具体含义
  `alfred://customsearch/Search%20explainShell%20for%20%7Bquery%7D/explainshell/utf8/nospace/https%3A%2F%2Fexplainshell.com%2Fexplain%3Fcmd%3D%7Bquery%7D`
- **fontAwesome**: 搜索fontAwesome图标库
   `alfred://customsearch/Search%20FontAwesome%20icons%20for%20%7Bquery%7D/icon/utf8/nospace/https%3A%2F%2Ffontawesome.com%2Ficons%3Fd%3Dgallery%26q%3D%7Bquery%7D%26m%3Dfree`
- **code if**: 变量命名推荐
  `alfred://customsearch/Search%20codeIf%20for%20%7Bquery%7D/codeif/utf8/nospace/https%3A%2F%2Funbug.github.io%2Fcodelf%2F%23%7Bquery%7D`
- **知乎**： `alfred://customsearch/Search%20%E7%9F%A5%E4%B9%8E%20for%20%7Bquery%7D/zhh/utf8/nospace/https%3A%2F%2Fwww.zhihu.com%2Fsearch%3Ftype%3Dcontent%26q%3D%7Bquery%7D`
- **简书**： `alfred://customsearch/Search%20%E7%AE%80%E4%B9%A6%20for%20%20%7Bquery%7D/jsh/utf8/nospace/http%3A%2F%2Fwww.jianshu.com%2Fsearch%3Fq%3D%7Bquery%7D`
- **京东**： `alfred://customsearch/Search%20%E4%BA%AC%E4%B8%9C%20for%20%7Bquery%7D/jd/utf8/nospace/https%3A%2F%2Fsearch.jd.com%2FSearch%3Fkeyword%3D%7Bquery%7D%26enc%3Dutf-8%26wq%3D%7Bquery%7D%26pvid%3Df3c58b9984f24ff0a5090ddec45775f8`
- **淘宝**： `alfred://customsearch/search%20%E6%B7%98%E5%AE%9D%20for%20%7Bquery%7D/tb/utf8/nospace/http%3A%2F%2Fs.taobao.com%2Fsearch%3Foe%3Dutf-8%26f%3D8%26q%3D%7Bquery%7D`
- **网易云音乐网页版**： `alfred://customsearch/Search%20%E7%BD%91%E6%98%93%E4%BA%91%E9%9F%B3%E4%B9%90%20for%20%7Bquery%7D/music/utf8/nospace/http%3A%2F%2Fmusic.163.com%2F%23%2Fsearch%2Fm%2F%3Fs%3D%7Bquery%7D%26type%3D1`
- **搜狗微信公号文章**： `alfred://customsearch/Search%20About%20%E5%BE%AE%E4%BF%A1%20for%20%7Bquery%7D/wc/utf8/nospace/http%3A%2F%2Fweixin.sogou.com%2Fweixin%3Fp%3D01030402%26query%3D%7Bquery%7D%26type%3D2%26ie%3Dutf8`

上面这种添加方式使用的是搜索的默认图标，我们还可以给这些搜索设置自定义图标。
打开 `Alfred Preference` >> `Features` >> `Web Search`

在想要修改的条目上双击打开设置界面，然后将想要设置的图标拖动到右侧的小方块中即可
 ***

## [workflow](https://www.alfredapp.com/workflows/)
搜索workflow
- https://www.alfredapp.com/workflows/
- GitHub
- http://www.packal.org/

我推荐的：
- [hash](https://github.com/BigLuck/alfred2-hash):  支持MD5, SHA1, Base64, htpasswd, whirlpool and crc32 转换。唤醒Alfred，输入`md5 + 内容` 或 `base64 + 内容`
- [node](https://github.com/onvno/alfred-package-workflow/blob/master/package/node.alfredworkflow):搜索npm包。 唤醒Alfred，输入`node + 关键词`
- [ip 查询](https://github.com/zenorocha/alfred-workflows/tree/master/ip-address): 唤醒Alfred，输入`ip`, 会显示内外网的ip
- [Color](https://github.com/TylerEich/Alfred-Extras/releases)： 颜色转换，唤醒Alfred，输入才`c + color`， eg. `c + #ff0`
- [gitHub](https://github.com/gharlan/alfred-github-workflow) ： 唤醒Alfred，输入`gh + 内容`，这个比webSearch中 github 搜索强大好多。
- [显示 http 状态码含义](https://github.com/JoelQ/alfred-http) 唤醒Alfred，输入`http + 状态码`
- [Currency Convert](https://github.com/jin5354/alfred3-workflow-CurrencyConvert/releases) : 货币转换，eg. `cy + 100$`
- [有道翻译](https://github.com/whyliam/whyliam.workflows.youdao): `yd + 内容`
- [扇贝翻译](https://github.com/henter/Shanbay-Alfred2): `sb + 内容`

