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