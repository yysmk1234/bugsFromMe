## 关于node中的遍历异步问题

   开发的过程中发现node中的foreach函数中执行异步函数无法获取预定的结果。
   经过查找相关资料发现node中的`foreach` 没有实现异步函数，所以在`foreach`中的函数全是同步函数
   
   查过ES6 的官方文档，发现对于异步的遍历还是已经有官方遍历接口
   `for await of`
