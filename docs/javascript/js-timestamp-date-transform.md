# js时间戳与日期格式之间的互转

[原文链接](https://segmentfault.com/a/1190000000481753)

### 将时间戳转换成日期格式
``` js
// 比如需要这样的格式 yyyy-MM-dd hh:mm:ss
var date = new Date(1398250549490);
Y = date.getFullYear() + '-';
M = (date.getMonth()+1 < 10 ? '0'+(date.getMonth()+1) : date.getMonth()+1) + '-';
D = date.getDate() + ' ';
h = date.getHours() + ':';
m = date.getMinutes() + ':';
s = date.getSeconds();
console.log(Y+M+D+h+m+s); //呀麻碟
// 输出结果：2014-04-23 18:55:49
```

### 将日期格式转换成时间戳
``` js
// 也很简单
var strtime = '2014-04-23 18:55:49:123';
var date = new Date(strtime); //传入一个时间格式，如果不传入就是获取现在的时间了，这样做不兼容火狐。
// 可以这样做
var date = new Date(strtime.replace(/-/g, '/'));

// 有三种方式获取，在后面会讲到三种方式的区别
time1 = date.getTime();
time2 = date.valueOf();
time3 = Date.parse(date);

/*
三种获取的区别：
第一、第二种：会精确到毫秒
第三种：只能精确到秒，毫秒将用0来代替
比如上面代码输出的结果(一眼就能看出区别)：
1398250549123
1398250549123
1398250549000
*/
```
