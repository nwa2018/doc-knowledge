# 让滚动的内容在IOS上滚动动作更平滑

默认情况下，网页在`IOS`上的`scroll`滚动就像在冰面上推冰球，轻轻一推，它会自动滚动并且减慢速度直至停止。而网页内容中同样需要将溢出内容以`scroll`的方式展示，直接使用`overflow:auto`并不能达到同样的效果，用手指触摸滑动时会变得生涩卡壳。于是需要给元素加上这样一个特殊属性：
```
-webkit-overflow-scrolling: touch;
```

延伸阅读：[iOS safari 如何阻止“橡皮筋效果”？](https://www.zhihu.com/question/22256539)
