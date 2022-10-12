# LNK2019
```
无法解析的外部符号 “symbol”， 函数 "function" 中引用了该符号
```
>头文件有了，但是库呢？

## 参考

+ [MSDN](https://learn.microsoft.com/zh-cn/cpp/error-messages/tool-errors/linker-tools-error-lnk2019?view=msvc-140)

## 原因
> 很显然，你忘了将函数的实现导入进来


## 解决方案 
 +  将头文件的目录添加到项目配置中 `属性` > `链接器` > `常规` > `附加库目录`   
    通过 `宏` 来快速的定位到相对路径，如果你已经将这些 `库` 移动到项目目录的某处，常用的有：
    ``` sh 
    ${ProjectDir}  ${ProjectName} ...
    ```
    来组成某个相对目录
    ``` sh
    ${Project}lib/  =>  盘符:前置的目录/项目目录/lib/
    ```
    ![附加库目录](P1.png)   
    以及配置你需要引用到的 `库` 如 `mscorlib.dll` 、 `Kernel32.lib` （用 `;` 号分隔他们）
    ![附加依赖项](P2.png)    
    如果你无法确定哪一些库是你所用到的，请询问他们提供的 `开发文档` 或者 `带你入坑` 的人，或者...    
    **`把所有库全部导入进去`**   


---

# 想要[返回](../README.md)?