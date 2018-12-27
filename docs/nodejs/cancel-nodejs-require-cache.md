# 取消nodejs对require模块的缓存

[原文链接](https://cnodejs.org/topic/52aa6e78a9526bff2232aaa9)

``` js
delete require.cache[‘path/to/config’]
config = require(‘path/to/config’)
```
