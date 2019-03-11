## 关于开发当中的event事件问题

#### 1.注册全局event对象

在公共文件中注册event对象，然后在不同的目录文件中引入，这样的话就可以进行不同目录之间通过event进行调用

event对象实例的 on 方法和 emit 方法都可以带参数

#### 2.event实例的删除事件监听的问题

removelistener方法需要两个参数，第一个是注册的事件名称，第二个是回调函数。关键就是这个回调函数上面。这个回调函数必须和 on 或者 addListener 中的回调
函数指向一个函数，也就是同一个函数

举个例子（可以看node文档）

```
let event = require('event');

let eventObject = new event.EventEmitter();

const callback = (args) => {
  //do sth
}

eventObject.on('test',callback);

eventObject.removeListener('test',callback)

```
如果是匿名函数或者其他，会导致移除监听失败
