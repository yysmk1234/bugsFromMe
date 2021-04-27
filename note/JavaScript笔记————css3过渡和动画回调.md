# JavaScript笔记————css3过渡和动画回调

css过渡和动画通常来说是可以直接用css处理，但是，会有一定的业务需要再某一些组件执行完动画以后继续操作。
### 1.计时器
通常的办法是通过计时器来计算动画结束时间。但是这种方案有一定的弊端：
·由于动画和延时函数并不一定是同一时间开始,导致函数和动画不同步
·会造成JS代码和CSS代码相互关联耦合,修改和维护比较麻烦
·存在多个动画需要回调时会造成代码混乱和臃肿
·在多个动画效果同时结束时会引起回调函数冲突

### 2.js事件
  js提供了两个相关事件来解决css过渡和动画的回调问题。即transtionend 和 animationend。
  
  ```
  document.getElementById("myDIV").addEventListener("transitionend", myFunction); //myFunction即为动画回调函数
  
  document.getElementById("myDIV").addEventListener("animationend", myFunction); //myFunction即为回调函数
  ```
  
