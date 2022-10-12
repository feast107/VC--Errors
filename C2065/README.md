# C2065

# 典中典《**`“未定义的标识符”`**》


## 参考

 + # **[MSDN](https://learn.microsoft.com/zh-cn/cpp/error-messages/compiler-errors-1/compiler-error-c2065?view=msvc-170) 非常建议查看MSDN!!!**  
 > 首席主治医师 `微软` 将对您的病情进行持续的跟踪

---
# 情况

> 可能的情况非常多，这事我也说不准

## 可能的原因

+ 检查你的代码，保证每一个变量都得到了 `声明` 以及没有被 `重复声明`。

+ 检查你的代码，保证符号们 `''` `""` `{ }` `( )`  `[]` `;` 正确的将代码包围, 否则他们总是会跟   
    ## [C2143](../C2143/README.md)    
    成对的出现

+ 在某个 `不知名` 的VC++学习版中某个旧的 `不知名` 的 `C语言` 编译器 `MSVC` 不支持 `声明` + `表达式` 初始化如:
    ``` c
    int square = width * height;
    ```
    他们必须是:

    ``` c
    int square;
    square = width * height;
    ```
