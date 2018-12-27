# 在express中如何设置response的header

在`nodejs`中，可以通过以下代码设置`header`
```
res.writeHead(200, {
    'Content-Length': 123
})
```
在`express`中这么写会报错`Error: Can't render headers after they are sent to the client`，原因是`express`对原生的`http`模块进行了重新封装，可以调用其提供的API去设置`header`，如下
```
res.header('Content-Length', 123)
```

[express官网](https://www.express.com/)
