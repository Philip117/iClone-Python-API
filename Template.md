# 编写格式
# ICX Python API:RLPy 类名
&emsp;&emsp;对应 [**<font color=RoyalBlue>官方网页</font>**](https://wiki.reallusion.com/IC8_Python_API:RLPy_REventCallback)。
&ensp;&ensp;&ensp;&ensp;Corresponding [**<font color=RoyalBlue>official page</font>**](https://wiki.reallusion.com/IC8_Python_API:RLPy_REventCallback).

&emsp;&emsp;最后编辑：2023.08.02
&ensp;&ensp;&ensp;&ensp;Last modified: 2023.08.02
___
### 介绍 - Description
&emsp;&emsp;类的介绍。

&emsp;&emsp;**<font color=Red>警告：。</font>**
___
### 类成员 - Class Methods
#### <div style="background: lightgray; padding: 8px;">RLPy.类名.函数</div>
&emsp;&emsp;函数介绍。

**参数：**

&emsp;&emsp;**参数名** - 参数类型[IN/OUT]: 参数介绍

**返回值：**

&emsp;&emsp;return - 返回值类型[OUT]: 返回值介绍

``` python {.line-numbers}
参考代码
```


# 编写案例
# IC8 Python API:RLPy REventCallback
&emsp;&emsp;对应 [**<font color=RoyalBlue>官方网页</font>**](https://wiki.reallusion.com/IC8_Python_API:RLPy_REventCallback)。
&ensp;&ensp;&ensp;&ensp;Corresponding [**<font color=RoyalBlue>official page</font>**](https://wiki.reallusion.com/IC8_Python_API:RLPy_REventCallback).

&emsp;&emsp;最后编辑：2023.08.02
&ensp;&ensp;&ensp;&ensp;Last modified: 2023.08.02

___
### 介绍 - Description
&emsp;&emsp;该类负责一些系统事件的回调管理。根据官方文档的说法，如果将 REventCallback 创建为局部变量会导致 iClone 的奔溃。回调函数中出现的错误也会导致 iClone 的奔溃，且不会有警告和报错，于是官方建议使用 Python 的 try-except 语法来捕获异常。

___
### 类成员 - Class Methods
#### <div style="background: lightgray; padding: 8px;">RLPy.REventCallback.OnAfterFileLoaded(self, nFileType)</div>
&emsp;&emsp;文件加载之后会被调用的回调函数，文件可以是从文件管理器拖进来的，可以是在 iClone 中点击导入进来，还可以是素材库中加入的，因为素材库中的素材本质上也是文件。

**参数：**

&emsp;&emsp;**nFileType** - int[IN]: 文件类型

**返回值：**

&emsp;&emsp;无

``` python {.line-numbers}
class MyREventCallback(RLPy.REventCallback):
    def __init__(self):
        RLPy.REventCallback.__init__(self)

    def OnAfterFileLoaded(self, nFileType):
        print("OnAfterFileLoaded\nFile type: {}".format(nFileType))

event_callback = None

def run_script():
    global event_callback
    event_callback = MyREventCallback()
    id = RLPy.REventHandler.RegisterCallback(event_callback)
```

