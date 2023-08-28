# IC8 Python API:RLPy RTime
&emsp;&emsp;对应 [**官方网页（无）**](https://wiki.reallusion.com/IC_Python_API:RLPy_RTime)。
&ensp;&ensp;&ensp;&ensp;Corresponding [**official page(none)**](https://wiki.reallusion.com/IC_Python_API:RLPy_RTime).

&emsp;&emsp;最后编辑：2023.08.28
&ensp;&ensp;&ensp;&ensp;Last modified: 2023.08.28
___
### 介绍 - Description
&emsp;&emsp;该类主要用于表示动画中的时间单位。
___
### 类成员 - Class Methods
> #### **RLPy.RTime.__init__(self)**
&emsp;&emsp;该函数用于创建一个时间对象，默认为时间为 0。

**参数：**

&emsp;&emsp;无

**返回值：**

&emsp;&emsp;return - RLPy.RTime[OUT]: 时间对象

``` python {.line-numbers}
def run_script():
    time = RLPy.RTime()
    print(time.ToInt())
```

</br>
</br>

> #### **RLPy.RTime.FromValue(tTick)**
&emsp;&emsp;函数介绍。

**参数：**

&emsp;&emsp;**tTick** - int[IN]: 时间，单位毫秒

**返回值：**

&emsp;&emsp;return - RTime[OUT]: 时间对象

``` python {.line-numbers}
def run_script():
    time = RLPy.RTime.FromValue(1000)
    print(time.ToInt())
```
