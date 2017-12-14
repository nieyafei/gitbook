# 作用域面试题 ☆☆

## 代码块

```

var y = 'global';  
function test(x){  
    if(x){  
        var y ='local';  
    }  
    return y;  
}  
console.log(test(true));  

```
> 结果是 local

## 代码块

```

var y = 'global';  
function test(x){  
    (function(){  
        if(x){  
            var y = 'local';  
        }  
    })();  
    return y;  
}  
console.log(test(true));  

```

> 结果是 global

## 代码块

```

var y = 'global';  
function test(x){  
    {  
        if(x){  
            var y = 'local';  
        }  
    }  
    return y;  
}  
console.log(test(true));  

```
> 结果是 local


## 代码块

```

(function() {
 
var a = b = 5;
 
})();
 
console.log(b);

```
> 结果是 5

**此题如果严格模式下是：Uncaught ReferenceError: b is not defined**


