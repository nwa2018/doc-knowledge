# img标签src空则隐藏默认边框

[阅读原文](https://www.zhihu.com/question/27426689)

```
img[src=""],img:not([src]){opacity:0;}
```
或者图片加载失败的时候，加载默认图片
```
<img src='xxx.js' onerror="src='default.png'" />
```
