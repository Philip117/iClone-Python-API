# IC8 Python API:RLPy RMath
&emsp;&emsp;对应 [**官方网页**](https://wiki.reallusion.com/IC8_Python_API:RLPy_RMath)。
&ensp;&ensp;&ensp;&ensp;Corresponding [**official page**](https://wiki.reallusion.com/IC8_Python_API:RLPy_RMath).

&emsp;&emsp;最后编辑：2023.10.12
&ensp;&ensp;&ensp;&ensp;Last modified: 2023.10.12
___
### 介绍 - Description
&emsp;&emsp;这个类负责数学运算相关的内容，包含三角函数、指数函数、对数函数、数值比较、随机数创建等。同时，它还提供一个常量值，例如零值、π 值等。
___
### 类成员 - Class Methods
> #### **RLPy.RMath.Abs(a)**
&emsp;&emsp;任意值取绝对值，并返回 float 类型。

**参数：**

&emsp;&emsp;**a** - int/float[IN/OUT]: 任意类型的值

**返回值：**

&emsp;&emsp;return - float[OUT]: 返回 float 类型的值

``` python {.line-numbers}
def run_script():
    value1 = -1
    value2 = -1.1
    print(RLPy.RMath.Abs(value1))
    print(type(RLPy.RMath.Abs(value1))) # 1.1
    print(RLPy.RMath.Abs(value2))
    print(type(RLPy.RMath.Abs(value2))) # 1.0
```

</br>
</br>

> #### **RLPy.RMath.AlmosyZero(tValue)**
&emsp;&emsp;判断给定值是否接近 0。

**参数：**

&emsp;&emsp;**tValue** - any[IN]: 给定值

**返回值：**

&emsp;&emsp;return - bool[OUT]: 给定值是否接近 0

``` python {.line-numbers}
def run_script():
    value1 = 0.1
    value2 = 0.00001
    value3 = 0.000001
    print(RLPy.RMath.AlmostZero(value1))    # False
    print(RLPy.RMath.AlmostZero(value2))    # True
    print(RLPy.RMath.AlmostZero(value3))    # True
```