# webStorm

## plugins
### markdown-navigator
代替 markdown 插件，对 markdown 的支持更好
### translation
翻译，选中内容后从右键菜单选择操作或直接使用快捷键
   - `⌃⌘Y`：选择翻译器,可选项有google、Youdao、baidu; Youdao需要注册[有道智云](http://ai.youdao.com/gw.s)创建应用并绑定翻译实例，并在webStorm translation的设置中填写应用id 和应用秘钥。百度也需要类似操作。
   - `⌃⌘O`：翻译并替换
   - `⌃⌘U`：翻译
   - `⌃⌘I`：显示翻译对话框
   
记忆技巧：`⌃⌘` + `YOU&I` 
### AceJump
键盘控制光标跳转
   - `⌃;`： 输入关键词会在所有的匹配的关键词旁边高亮显示一写字母，输入字母可以使光标跳转的指定位置。
   - `⇧⌃;`： 可以快速跳转到指定行。也可以使用webStorm自由的快捷键`⌘L`快速实现行跳转，而使用AceJump更直观。 
### .ignore
快捷添加 gitignore 模板
### Background Image Plus
设置背景
### Material Theme UI
更多的主题样式
### Rainbow Brackets
彩色的括号

## 快捷键
- `double ⇧`: 搜索所有内容All。选中搜索到的内容按enter可跳转至该位置。以下快捷键打开的是相同的窗口，对应不同的子分类。
    - `⌘O`: 搜索Classes
    - `⇧⌘O`: 搜索文件Files
    - `⌥⌘O`: 搜索文件Symbols
    - `⇧⌘A`: 搜索Actions

- `⌘E`: 最近打开的文件
- 工具窗口
    - `F12`: 打开之前打开的工具窗口（Terminal,TODO,Version Control）
    - `⌘9`: 打开工具窗口Version Control
    - `⌥F12`: 打开工具窗口Terminal
- 光标跳转
    - `⌘L`: 跳转至行
    - `⌘B`: **跳转到变量声明处**； `⌘Y`: **小浮窗显示变量声明行**
    - `⌘[`,`⌘]`: 切换光标历史位置
- 文件结构Structure
    - `⌘F12`: 文件结构弹出式菜单
    - `⌘7`: 文件结构左侧目录栏展开与折叠
- 导航栏    
    - `⌘↑`: 跳转到导航栏， `↑`,`↓`,`←`,`→`，切换目录位置
***

### 同时编辑多处内容

#### 通用
手动选中的多个位置同时编辑

`按住 ⌥ 单击`: 光标在被点击的多处位置定位，可以同时编辑这些位置的内容

可用于为markdown文件批量添加关键词高亮
#### 内容替换
需要待编辑位置有相同的字符串
- `⌃G`： 选中内容后使用，可选中其他位置的相同内容并同时编辑
- `⌘R`： 在本文件搜索并替换
- `⇧⌘R`： 全局搜索替换，跨文件
#### 同时编辑多列内容
`⇧⌘8` ：Column Select Mode，切换列选择模式

编辑 markdown 文档的时候，常用来批量修改普通文本为列表模式，同时编辑多列的开头位置。

***

### 搜索和替换
- ⌘F 搜索
- ⌘R 替换
- ⌘G 查找下一个
- ⇧⌘G 查找上一个
- ⇧⌘F 按路径搜索，跨文件的全局搜索
- ⇧⌘R 按路径替换，跨文件的全局搜索替换

***

### 版本管理 git 操作
- `⌘K`: commit
- `⌥⌘K`: commit and push
- `⇧⌘K`: push
- `⌘T`: update project

***

### 插入新行
- `⇧Enter`: 在当前行下方新插入一行，光标在新行开头
- `⌘Enter`: 在当前行下方新插入一行，光标留在原来位置
- `⌥⌘Enter`: 在当前行上方新插入一行，光标在新行开头
- `⌘D`: 在当前行下方重复当前行内容

***

### 其他
- `⇧⌘U`: 切换选中英文的大小写
- `⇧⌘[`, `⇧⌘]`: 切换窗口顶部选项卡，包括各种窗口的顶部选项卡，eg. 切换主窗口文件选项卡，打开工具窗口时切换工具窗口上方的选项卡

- `⌘X`: 剪切当前行


- `⌘+`，`⌘-`: 收缩代码块
- `⇧⌘+`，`⇧⌘-`: 收缩整个文档的代码块

`⌥⌘L`: 格式化代码, 会自动调整好缩进及`[],{},()`处的换行等； `⌃⌥I`只调整缩进
`⇧⌥⌘L`: 打开格式化代码设置弹窗

`⌃⇧J`: 清除缩进变成单行

`tab`: 增大缩进
`⇧tab`: 缩小缩进
`⌃⌥I`: 快速调整缩进，自动调整好选中内容的缩进距离

### 代码补全
`⌥/`: 代码补全


## 设置
### 设置选中文字的背景颜色
我使用的Material Theme UI 的Theme选中文字的颜色和markdown中的代码块颜色一样，需要专门设置一下选中文字的背景颜色

1. `⌘，`打开Preference 
1. \> Editor 
1. \> Color Scheme 
1. \> General 
1. \> Editor 
1. \> Selection Background
1. 编辑颜色，双击颜色值可以打开调色盘。
1. 编辑完成点击 `APPLY` 后点击`OK`

### 设置光标颜色和光标所在行背景色
从上面的第5步开始分别设置 Caret 及Caret Row 改变光标的颜色和光标所在行的背景色

1. `⌘，`打开Preference 
1. \> Editor 
1. \> Color Scheme 
1. \> General 
1. \> Editor 
1. \> 设置 Caret 改变光标的颜色 
1. \> 设置 Caret Row 光标所在行的背景色 


## 其他
### webstorm内存溢出 配置参数
1. 菜单栏 help
1. \> Edit Custom VM options 
1. 编辑 `webstorm.vmoptions` 中的
  - 第二行：-Xms526m 
  - 第三行：-Xmx1024m 

### exclude node-modules

1. `⌘，`打开Preference 
1. \> Editor 
1. \> File Types
1. \> 编辑右侧窗口底部`Ignore files and folders`编辑框内容, 添加 `node-modules;` 
1. \> 点击`OK`按钮

