# IC7 Python API:RLPy RTime
&emsp;&emsp;对应 [**官方网页**](https://wiki.reallusion.com/IC_Python_API:RLPy_RTime)。
&ensp;&ensp;&ensp;&ensp;Corresponding [**official page**](https://wiki.reallusion.com/IC_Python_API:RLPy_RTime).

&emsp;&emsp;最后编辑：2023.08.14
&ensp;&ensp;&ensp;&ensp;Last modified: 2023.08.14
___
### 介绍 - Description
&emsp;&emsp;该类主要用于表示动画中的时间单位。
___
### 类成员 - Class Methods
> #### **RLPy.RTime.__init__(self, args)**
&emsp;&emsp;该函数用于创建一个事件对象，单位毫秒。

**参数：**

&emsp;&emsp;**args** - any[IN]: 时间参数

**返回值：**

&emsp;&emsp;return - RLPy.RTime[OUT]: 时间对象

``` python {.line-numbers}
def run_script():
    time1 = RLPy.RTime()
    print(time1.GetValue())
    time2 = RLPy.RTime(1000)
    print(time2.GetValue())
    time3 = RLPy.RTime(2000, RLPy.kMilliseconds)
    print(time3.GetValue())
```