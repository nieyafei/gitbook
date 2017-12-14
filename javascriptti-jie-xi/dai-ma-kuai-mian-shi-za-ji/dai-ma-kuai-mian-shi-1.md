# 简单集合面试题 ☆☆

# 1. delete的使用

```

(function(x){
	delete x;
	return x;
})(1)

```

# 2. typeof

```

(function(){
	console.log(typeof arguments)
})()

# 结果：object
```

# 3. 代码题目

```

var h = function a(){
	return 23;
}
console.log(typeof a());

```

# 4. typeof题目

```

var x = 1;
if(function f(){}){
	x +=typeof f;
}
console.log(x);


# 结果 1undefined

```

# 5.声明提前

```

function test(){
	console.log(a);
	console.log(foo());
	var a = 1;
	function foo(){
		return 2;
	}
}

test();

```

> 结果是 undefined   2



























