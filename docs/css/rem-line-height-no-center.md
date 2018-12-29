# 使用rem设置line-height没有居中

[使用rem设置height和line-height相同时文字没有居中？](https://segmentfault.com/q/1010000006032019/)

手机端`rem`布局体系中，使用`height`与`line-height`无法垂直居中

原因是`12px`以下显示问题，字体太小，网上给的解决方案是先整体放大，再用`css3`缩小的方式解决，或者设置`line-height`为`1`，通过`padding`去垂直居中

但是在某些特定的场景，比如高度已经固定，以上解决方案无法解决，我单独用一个`div`包住了文字，并设置以下样式：
``` css
top: 50%;
line-height: 1!important;
transform: translateY(-50%);
float: left;
```
