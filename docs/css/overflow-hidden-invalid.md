# overflow:hidden某些低版本IOS手机浏览器上失效

以下代码在某些IOS版本`overflow: hidden`会失效
```
border-radius: 50px;
overflow: hidden
```

，需要加上以下样式
```
-webkit-mask-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAIAAACQd1PeAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAA5JREFUeNpiYGBgAAgwAAAEAAGbA+oJAAAAAElFTkSuQmCC);
```

[stackoverflow上的回答](https://stackoverflow.com/questions/5736503/how-to-make-css3-rounded-corners-hide-overflow-in-chrome-opera)
