# SecureCRT zmodem transfer canceled by remote side报错
[解决SecureCRT的zmodem transfer canceled by remote side错误](http://www.linuxdiyf.com/linux/19997.html)

`centos`通过`lrzsz`上传文件，如果上传大一些的文件或者含有控制字符的时候`SecureCRT`提示：

!> zmodem transfer canceled by remote side

可以使用 `rz -e` 命令可以解决这个问题

