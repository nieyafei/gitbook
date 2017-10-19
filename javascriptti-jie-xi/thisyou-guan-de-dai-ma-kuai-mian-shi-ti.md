下面的代码块输出到控制台的结果是什么，为什么？


```

var myObject = {
    foo: "bar",
    func: function() {
        var self = this;
        console.log("outer func:  this.foo = " + this.foo);
        console.log("outer func:  self.foo = " + self.foo);
        (function() {
            console.log("inner func:  this.foo = " + this.foo);
            console.log("inner func:  self.foo = " + self.foo);
        })()
    }
}
myObject.func();

```

输出结果如下：

```
outer func:  this.foo = bar
outer func:  self.foo = bar
inner func:  this.foo = undefined
inner func:  self.foo = bar

```

在外部函数func中的，this指向的对象是myObject,因此self也指向this
