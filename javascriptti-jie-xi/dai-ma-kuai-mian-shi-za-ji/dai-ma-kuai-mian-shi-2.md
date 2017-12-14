# 代码块面试集合2 

## 两个函数返回是一样吗

```

function foo1()
{
  return {
      bar: "hello"
  };
}

function foo2()
{
  return
  {
      bar: "hello"
  };
}

```

**结果：返回结果不一样**


