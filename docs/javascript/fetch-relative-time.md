# 获取相对时间

[JavaScript让时间显示为多久以前](https://segmentfault.com/a/1190000005625314)

经常的使用场景是使用`dateFormat`去格式化时间，但有时候我们也会需要取到相对时间，比如掘金官网

![](docs/javascript/image/fetch-relative-time1.jpg)

那么如何将时间戳转成相对时间呢？可以如下：

``` js
function gettime(createtime){
  var now=Date.parse(new Date())/1000;
  var limit=now-createtime;
  var content="";
  if(limit<60){
    content="刚刚";
  }else if(limit>=60 && limit<3600){
    content=Math.floor(limit/60)+"分钟前";
  }else if(limit>=3600 && limit<86400){
    content=Math.floor(limit/3600)+"小时前";
  }else if(limit>=86400 && limit<2592000){
    content=Math.floor(limit/86400)+"天前";
  }else if(limit>=2592000 && limit<31104000){
    content=Math.floor(limit/2592000)+"个月前";
  }else{
    content="很久前";
  }
  return content;
}
```
此外，也可以使用`npm`上的仓库[moment](https://www.npmjs.com/package/moment)(但是体积比较大)，[参考文档](http://momentjs.cn/docs/#/displaying/tonow/)
