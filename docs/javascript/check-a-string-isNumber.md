# 判断一个字符串是否为数字

[js 判断字符串是否全是数字，求解](https://segmentfault.com/q/1010000007500899)

``` js
function isNumber(value) {
  return !Number.isNaN(Number(value))
}
```
