# 原型链面试题 ☆☆

## 代码块

```

function Name(){
    this.name=function(){
        console.log("killua")
    }
}
function Firstname(){
    this.firstname=function(){
        console.log("L")
    }
}
Name.prototype = new Firstname();
var he = new Name();
console.log(he.name); //"killua"
console.log(he.firstname); //"L"

```


## 代码块

```

function Elem(id){
this.elem = document.getElementById(id)
}
Elem.prototype.html = function(val){
    var elem = this.elem
    if(val){
        elem.innerHTML = val
        return this //链式操作
    }else{
        return elem.innerHTML
    }
}
Elem.prototype.on = function(type, fn){
    var elem = this.elem
    elem.addEventListener(type, fn) //addEventListener() 方法用于向指定元素添加事件句柄
}
var div1 = new Elem('div1')
div1.html('<p>hello killua</p>').on('click',function(){
	alert('clicked');
	div1.html('<p>javascript</p>')
})

```



