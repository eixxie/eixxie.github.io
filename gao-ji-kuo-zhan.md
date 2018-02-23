# 高级扩展 {#articleHeader8}

> 掌握了“基本使用”，但有时候想要gitBook更美观，或者更符合我们自己的需求，则通过book.json配置进行自定义、以及安装一些常用的插件等。

## Book.json配置 {#articleHeader9}

> GitBook 在编译书籍的时候会读取书籍源码顶层目录中的 book.js 或者 book.json，这里以 book.json 为例，参考 GitBook 文档 可以知道，book.json 支持如下配置

```
{

    //样式风格配置格式

"styles"
: {

"website"
: 
"styles/website.css"
,

"ebook"
: 
"styles/ebook.css"
,

"pdf"
: 
"styles/pdf.css"
,

"mobi"
: 
"styles/mobi.css"
,

"epub"
: 
"styles/epub.css"

     },

    //插件安装配置格式


"plugins"
: [
"myplugin"
],

"pluginsConfig"
: {

"myPlugin"
: {

"message"
: 
"Hello World"

        }
     }    
}
```

## 自定义插件扩展 {#articleHeader10}

> 插件是扩展GitBook功能最好的方法。使得GitBook功能更加强大，例如，把数学公式显示支持，跟踪回访使用谷歌解析，…以toggle-chapters插件为例  
> toggle-chapters 插件的效果是默认只在目录导航中显示章的标题，而不会显示小节的标题，点击每一章或者每一节会显示当前章或节的子目录，如果有的话，但是同时会收起其它之前展开的章节。所以，个人认为不是非常实用，因为这样子用户不能快速跳转到没有展开的章节！

一、搜索、安装插件方式

1、编辑器方式（没成功）

![](https://segmentfault.com/img/bVyKAo)

2、通过GitHub方式

> www.plugins.gitbook.com

3、node.js命令方式

* 默认安装在以下路径

```
C:
\U
sers
\Q
GY
\A
ppData
\R
oaming
\n
pm
\n
ode_modules
```

* 把插件文件夹复制到

```
npm
install
gitbook-
plugin
-toggle-chapters
--save-dev
```

二、通过Book.json配置插件

```
"plugins"
: [
"toggle-chapters"
],

"pluginsConfig"
: {

"myPlugin"
: {

"message"
: 
"Hello World"

        }
     }
```



