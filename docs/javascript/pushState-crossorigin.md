# pushState，replaceState无法使用非同源的地址

在手机浏览器里面，在特定的时机可以调用`pushState`或者`replaceState`方法替换浏览器上的链接，如此可以引导用户去调用系统默认分享功能去分享我们设定的地址，但是`pushState`，`replaceState`无法作用于非同源的地址

[stackoverflow里面的回答](https://stackoverflow.com/questions/14807921/html5-history-api-pushstate-from-a-domain-to-a-subdomain)
