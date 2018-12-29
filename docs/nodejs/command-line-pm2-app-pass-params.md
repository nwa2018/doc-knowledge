# 通过命令行给pm2的app程序传递参数

[How to pass arguments to app using pm2?](https://stackoverflow.com/questions/28980307/how-to-pass-arguments-to-app-using-pm2)

``` js
pm2 start myServer.js --node-args="--production --port=1337"
```

``` js
pm2 start app.js -- --prod
```
