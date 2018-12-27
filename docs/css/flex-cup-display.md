# 通过flex实现圣杯布局

> 水平/垂直方向，首尾两部分宽度/高度定死，中间自动撑满整个div

使用`flex`布局，演示垂直方向

**html**
``` html
<div class="container">
  <div class="header"></div>
  <div class="body"></div>
  <div class="footer"></div>
</div>
```

**css**
``` css
.container {
  diplay: flex;
  height: 100%;
  flex-direction: column;  // 垂直方向布局
}
.header {
  height: 200px;
}
.footer {
  height: 300px;
}
.body {
  flex: 1;  // 会自动撑满
}
```
