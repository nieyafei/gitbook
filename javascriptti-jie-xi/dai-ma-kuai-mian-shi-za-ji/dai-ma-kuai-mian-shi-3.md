# 代码块面试 ☆☆☆

## 代码块题目

```

var obj = {
	name : "obj"
};
var name = "window";
function test(){
	var name = "scope";
	with(obj) {
		console.log(name);
	};
}
test();

```

> 结果：obj


## 代码块

```
var a = 25;
(function(){
	console.log(a);
	var a = 30;
}())
```

> 结果：undefined