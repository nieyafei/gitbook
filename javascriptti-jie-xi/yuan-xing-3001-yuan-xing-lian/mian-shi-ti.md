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
预编译的时候，window环境有{a:3,c:function...},执行的时候，执行functon() 有个{a:4},c()执行，因为其本身无a,因此调用最外面的window.a

如果想打出4的话，需要改一下

```

var a=3;
 function c(a){
    console.log(a);
 }
 (function(){
  var a=4;
  c(a);
 })();

```
> 结果是 4

我们来改一下

```

var a=3;
 function c(a){
    var a = 6;
    console.log(a);
 }
 (function(){
  var a=4;
  c(a);
 })();


```
> 结果是 6

下面来测试一下各个环境的a的值

```

var a=1;
 function c(a){
    var a = 6;
    console.log(a);
 }
 (function(){
  a++;
  var a=4;
  console.log(a);
  c(a);
 })();
 console.log(a);

```
>  结果是 4    6     1








