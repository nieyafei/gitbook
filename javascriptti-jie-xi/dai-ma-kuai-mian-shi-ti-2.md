## 回答下面的代码块执行之后的结果
```

var num = 10;
var obj = {
    num:8,
    inner: {
        num: 6,
        print: function () {
            console.log(this.num);
        }
    }
}
num = 888;
obj.inner.print();
var fn = obj.inner.print;
console.log(typeof(fn));
fn();
(obj.inner.print)(); 
(obj.inner.print = obj.inner.print)(); 

```