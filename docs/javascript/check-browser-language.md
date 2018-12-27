# JS如何判断浏览器的语言

[阅读原文](https://blog.csdn.net/clever101/article/details/78218356)

``` js
const JsSrc =(navigator.language || navigator.browserLanguage).toLowerCase();
if(JsSrc.indexOf('zh')>=0) {
   // 假如浏览器语言是中文
} else if(JsSrc.indexOf('en')>=0) {
    // 假如浏览器语言是英文
} else {
   // 假如浏览器语言是其它语言
}
```
