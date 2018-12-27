# 监听手Q的挂起事件（visibilitychange）

[阅读原文](https://segmentfault.com/a/1190000011739488)

H5有一个事件叫 `visibilitychange` 可以用于监听当前页面是否被挂起。如下：
```
document.addEventListener("visibilitychange", () => {
    if(document.hidden) {
        // 页面被挂起
    }
    else {
        // 页面呼出
    }
});
```
但是呢，手Q不会触发这个事件！因为手Q的网页永远都不会被挂起，所以`visibilitychange`事件不会被触发。

### 解决方案1
使用[手Q sdk](http://pub.idqqimg.com/qqmobile/qqapi.js?_bid=152&quot)后使用
``` js
mqq.addEventListener("qbrowserVisibilityChange", function(e){
    if(e.hidden) {
        // 手Q被挂起
    }
    else {
        // 手Q被呼起
    }
});
```
### 解决方案2
``` js
document.addEventListener("qbrowserVisibilityChange", function (e) {
    if(e.hidden) {
        // 手Q被挂起
    }
    else {
        // 手Q被呼起
    }
});
```
