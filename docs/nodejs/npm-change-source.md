# npm换源

[原文链接](https://www.jianshu.com/p/0deb70e6f395)

### 国内优秀的npm镜像

淘宝`npm`镜像：[http://registry.npm.taobao.org/](http://registry.npm.taobao.org/)

### 如何使用
#### 临时使用
```
npm --registry https://registry.npm.taobao.org install express
```

#### 永久使用
```
npm config set registry https://registry.npm.taobao.org
// 配置后可通过下面方式来验证是否成功
npm config get registry
// 或npm info express
```
