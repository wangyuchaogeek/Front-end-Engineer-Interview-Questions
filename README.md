# Front-end-Engineer-Interview-Questions



## 1.JS中的事件循环(Event Loop)

JavaScript中的事件循环是一种用于处理异步代码的机制。它确保JavaScript代码在单线程的环境下能够正确地处理异步操作，并保持响应性。

事件循环的核心是一个循环，该循环不断地从事件队列中获取事件并执行它们。事件可以是用户交互、定时器到期、网络请求的响应等。事件循环的过程是基于"事件驱动"的。

下面是事件循环的简要步骤：

1. 执行同步代码：首先，JavaScript引擎会执行当前执行上下文中的同步代码，这些代码按照编写的顺序依次执行。
2. 处理异步代码：当遇到异步操作时，比如定时器、网络请求等，它们会被分发到相应的Web API中进行处理，并注册相应的回调函数。
3. 将回调函数加入事件队列：当异步操作完成时，相应的回调函数会被添加到事件队列中。事件队列是一个先进先出的数据结构。
4. 检查调用栈：在主线程空闲时，JavaScript引擎会检查调用栈是否为空。如果调用栈为空，表示同步代码已经执行完毕，可以开始处理异步代码。
5. 从事件队列中获取事件：JavaScript引擎会从事件队列中取出一个事件，并将其对应的回调函数放入调用栈中。
6. 执行回调函数：回调函数开始执行，处理相应的异步操作。如果回调函数中包含了其他的异步操作，将会重复前面的步骤。

这个过程会一直重复，直到事件队列中没有更多的事件为止。这样，JavaScript引擎就能保持响应性，并能够在单线程的环境中处理异步操作。

需要注意的是，事件循环中的微任务（microtask）和宏任务（macrotask）的执行顺序也很重要。微任务包括Promise回调、MutationObserver回调等，它们在当前宏任务执行完毕后立即执行。而宏任务包括setTimeout、setInterval等，它们会在下一次事件循环中执行。



常见的宏任务有：script（整体代码）/setTimout/setInterval/setImmediate(node 独有)/requestAnimationFrame(浏览器独有)/IO/UI render（浏览器独有）

常见的微任务有：process.nextTick(node 独有)/Promise.then()/Object.observe/MutationObserver

参考文章：[面试必问之 JS 事件循环](https://zhuanlan.zhihu.com/p/580956436)



## 2.js中的闭包

[js闭包详解](https://blog.csdn.net/weixin_41192489/article/details/124312822)



## 3.原型链

[如何回答面试中的JavaScript原型链问题](https://zhuanlan.zhihu.com/p/356980105)

[JavaScript 世界万物诞生记](https://zhuanlan.zhihu.com/p/22989691)



## 4.JS中的继承方式

[js的六种继承方式](https://blog.csdn.net/weixin_41759744/article/details/125299029)



## 5.ES6新特性

[ES6 新特性学习](https://www.jianshu.com/p/fc0b66786f1a)



## 6.BFC

[JS原理之BFC](https://juejin.cn/post/6844904023477223438)



## 7.em与rem的区别

em相对于父元素
rem相对于根元素





