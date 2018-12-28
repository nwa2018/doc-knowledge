# nodejs全局安装的路径在哪

[阅读原文](http://www.cnblogs.com/chyingp/p/npm-install-difference-between-local-global.html)

全局模块的真实安装路径在`/usr/local/lib/node_modules/`下，

`/usr/local/bin`下的可执行文件是软链接，指向全局安装模块的可执行文件位置
