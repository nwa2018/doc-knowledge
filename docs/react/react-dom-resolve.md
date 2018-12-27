# 在react中如何插入待解析的dom字符串

[阅读原文](https://reactjs.org/docs/dom-elements.html)

在`vue`中可以直接使用`v-html`，非常方便

在`react`中可以如下使用
```
<div dangerouslySetInnerHTML={{ __html: '<p>some insert p tag</p>' }} />
```
