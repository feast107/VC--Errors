# C2784
```
“declaration”: 对于“type”，无法从“type”推导其模板参数
```

## 参考

+ [MSDN](https://learn.microsoft.com/zh-cn/cpp/error-messages/compiler-errors-2/compiler-error-c2784?view=msvc-170) 

---
# 情况

## 原因

+ 常规的情况下，由于模板参数不正确导致，参照[参考](#参考)能快速的解决他们
+ 非常规的情况下，你是不是使用了形似 
    ``` c++
    cin<<x ;
    ```
    它会被编译器认为是模板函数的调用而引发 [C2784](#c2784)

---
# 想要[返回](../README.md)?