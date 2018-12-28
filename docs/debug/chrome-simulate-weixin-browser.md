# Chrome 修改 user agent 简单模拟微信内置浏览器

### 微信和QQ内置浏览器UA
- 安卓QQ内置浏览器UA:
```
Mozilla/5.0 (Linux; Android 5.0; SM-N9100 Build/LRX21V) > AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 > Chrome/37.0.0.0 Mobile Safari/537.36 V1_AND_SQ_5.3.1_196_YYB_D > QQ/5.3.1.2335 NetType/WIFI
```

- 安卓微信内置浏览器UA:
```
Mozilla/5.0 (Linux; Android 5.0; SM-N9100 Build/LRX21V) > AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 > Chrome/37.0.0.0 Mobile Safari/537.36 > MicroMessenger/6.0.2.56_r958800.520 NetType/WIFI
```

- IOSQQ内置浏览器UA:
```
Mozilla/5.0 (iPhone; CPU iPhone OS 7_1_2 like Mac OS X) > AppleWebKit/537.51.2 (KHTML, like Gecko) Mobile/11D257 > QQ/5.2.1.302 NetType/WIFI Mem/28
```

- IOS微信内置浏览器UA:
```
Mozilla/5.0 (iPhone; CPU iPhone OS 7_1_2 like Mac OS X) > AppleWebKit/537.51.2 (KHTML, like Gecko) Mobile/11D257 > MicroMessenger/6.0.1 NetType/WIFI
```

### 在Chrome添加UA

打开`Chrome`调试工具 -> 点击右上角的三个点 -> 选择`Setting` -> `Devices` -> 点击`Add custom device`

