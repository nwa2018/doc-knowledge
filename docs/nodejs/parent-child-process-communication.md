# nodejs父子进程通信
[child_process中子进程与父进程之间的通信与断开连接](https://www.zybuluo.com/frank-shaw/note/505788)

### demo
``` js
//parent.js
var cp = require('child_process');
var n = cp.fork(__dirname + '/sub.js');
n.on('message', function(m) {
  console.log('Parent got message: ', JSON.stringify(m));
});
n.send({ hello: 'world' });
//sub.js
process.on('message', function(m) {
  console.log('Child got message: ', JSON.stringify(m));
});
process.send({ foo: 'bar' });
```

注意：

- `child_process`与`cluster`中的`master-worker`模式还是有一定区别的。不要混淆了。

- 注意，父进程和子进程 `send()` 是同步的，不要用来发送大块的数据。

- 发送 `{cmd: 'NODE_foo'}` 消息是特殊情况。所有包含 `NODE_`前缀的消息都不会被触发，因为它们是 `node` 的内部的核心消息，它们会在 `internalMessage` 事件里触发，尽量避免使用这个特性。

### 如何断开连接
父进程：`child.disconnect()`

子进程：`process.disconnect()`
