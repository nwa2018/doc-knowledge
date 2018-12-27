# js如何判断一个对象是否为空

#### 方法1：
```
function checkNullObj (obj) {
    return Object.keys(obj).length === 0
}
```
> Object.keys在低版本浏览不兼容，需要自行polyfill

#### 方法2:
```
if (JSON.stringify(data) === '{}') {
    return false // 如果为空,返回false
}
return true // 如果不为空，则会执行到这一步，返回true
```
#### 方法3：
for (var i in obj) { // 如果不为空，则会执行到这一步，返回true
    return true
}
return false // 如果为空,返回false
