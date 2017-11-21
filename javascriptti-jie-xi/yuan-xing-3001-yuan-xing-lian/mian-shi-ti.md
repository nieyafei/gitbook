# 面试小集合 ☆☆

## Array.isArray(Array.prototype)结果

> 结果是true

## Array.isArray(Array.__proto__)结果

> 结果是false


解答：

>Array.prototype ===>  结果是数组
Array.isArray():确定传递的值是否是一个 Array
Array.__proto__：原型指向了Object



## 代码块题

```
 var a=3;
 function c(){
    console.log(a);
 }
 (function(){
  var a=4;
  c();
 })();
 // 立即执行闭包
```
> 结果是 3

解答：

> js中变量的作用域链与定义时的环境有关，与执行时无关。执行环境只会改变this、传递的参数、全局变量等

