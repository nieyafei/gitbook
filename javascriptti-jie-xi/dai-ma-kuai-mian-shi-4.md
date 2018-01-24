## 代码块1

```
this.a = 20;
var test = {
	a:40,
	init:function(){
		console.log(this.a);
		function go(){
			//this.a = 60;
			console.log(this.a);
		}
		go.prototype.a = 50;
		return go;
	}
}
//var p = test.init();
//p();
new(test.init())();
```

> 结果：40  50


## 代码块2

**上述代码块1的代码的注释去掉之后的结果**

> 结果：40  60  40  60

## 代码块3
**修改一下代码块1的代码**

```
this.a = 20;
var test = {
	a:40,
	init:()=>{// 箭头函数
		console.log(this.a);
		function go(){
			//this.a = 60;
			console.log(this.a);
		}
		go.prototype.a = 50;
		return go;
	}
}
//var p = test.init();
//p();
new(test.init())();
```
> 结果： 20 50


## 代码块4

**去掉代码块3的注释的结果**

> 结果：20 60 60 60
