# ICX Python API:RLPy RGlobal
&emsp;&emsp;对应 [**<font color=RoyalBlue>官方网页</font>**](https://wiki.reallusion.com/IC_Python_API:RLPy_RGlobal)。
&ensp;&ensp;&ensp;&ensp;Corresponding [**<font color=RoyalBlue>official page</font>**](https://wiki.reallusion.com/IC_Python_API:RLPy_RGlobal).

&emsp;&emsp;最后编辑：2023.08.04
&ensp;&ensp;&ensp;&ensp;Last modified: 2023.08.04
___
### 介绍 - Description
&emsp;&emsp;该类主要负责宏观上的时间线、播放器、动画事件等管理。
___
### 类成员 - Class Methods
#### <div style="background: lightgray; padding: 8px;">RLPy.RGlobal.GetTime()</div>
&emsp;&emsp;获取时间线当前的时间，即播放条当前位置对应的时间线时间，而非现实时间。

**参数：**

&emsp;&emsp;无

**返回值：**

&emsp;&emsp;return - RTime[OUT]: 时间线当前的时间

``` python {.line-numbers}
def run_script():
    cur_time = RLPy.RGlobal.GetTime()
    print(cur_time.GetValue())
```

#### <div style="background: lightgray; padding: 8px;">RLPy.RGlobal.SetTime(kTime, bSendEvent=True)</div>
&emsp;&emsp;设置时间线当前的时间，官方文档中未标明参数，阅读源码可以发现该函数有两个参数。

**参数：**

&emsp;&emsp;**kTime** - RTime[IN]: 设置的时间

&emsp;&emsp;**bSendEvent** - bool[IN]: 未知

**返回值：**

&emsp;&emsp;return - RStatus[OUT]: 设置成功与否

``` python {.line-numbers}
def run_script():
    time = RLPy.RTime(1000)
    RLPy.RGlobal.SetTime(time)
    cur_time = RLPy.RGlobal.GetTime()
    print(cur_time.GetValue())
```