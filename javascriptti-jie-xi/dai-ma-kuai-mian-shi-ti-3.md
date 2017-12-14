# 代码块面试题3 **☆**

## 代码块

```
function Person(name, age, sex) {
	var a = 0;// 私有化变量
	this.name = name;
	this.age = age;
	this.sex = sex;
	function sss() {
		a ++;
		console.log(a);
	}
	this.say = sss;
}
var oPersopn = new Person();
oPersopn.say();// 
oPersopn.say();// 
var oPersopn1 = new Person();
oPersopn1.say();// 

```

依次列出打印的结果

结果：
```
1    2    1

```

## 代码块

```

var fullName = "alibaba";
var obj = {
	fullName:"baidu",
	prop:{
		fullName:"tengxun",
		getFullName: function(){
			return this.fullName;
		}
	}
}
console.log(obj.prop.getFullName());// tengxun
var test = obj.prop.getFullName;
console.log(test());

```
> 结果： tengxun   alibaba



