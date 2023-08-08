# ICX Python API:RLPy RDialogCallback
&emsp;&emsp;对应 [**<font color=RoyalBlue>官方网页</font>**](https://wiki.reallusion.com/IC_Python_API:RLPy_RDialogCallback)。
&ensp;&ensp;&ensp;&ensp;Corresponding [**<font color=RoyalBlue>official page</font>**](https://wiki.reallusion.com/IC_Python_API:RLPy_RDialogCallback).

&emsp;&emsp;最后编辑：2023.08.03
&ensp;&ensp;&ensp;&ensp;Last modified: 2023.08.03
___
### 介绍 - Description
&emsp;&emsp;这个类负责 RDialog 窗口的回调管理，只有三个回调函数：OnDialogShow()、OnDialogHide() 和 OnDialogClose()，分别在窗口显示、隐藏和关闭时触发。根据官方文档的说法和本人亲测，如果将 RDialogCallback 或它的子类创建为局部变量会导致 iClone 的崩溃，且不会有警告和报错，一般会在窗口关闭时崩溃。虽然官方文档建议使用 Python 的 try-except 语法来捕获异常，但是因为错误原因并不在回调函数内部，回调函数内的代码在崩溃前仍能正确执行，所以在回调内部捕获异常也没用。

&emsp;&emsp;**$\color{red}警告：请勿将该类或子类创建为局部变量。$**
\color{red}{警告：请勿将该类或子类创建为局部变量。}
___
### 类成员 - Class Methods
> #### <div style="background: lightgray; padding: 8px;">RLPy.RDialogCallback.OnDialogShow(self)</div>
&emsp;&emsp;该函数在窗口显示时被调用。

**参数：**

&emsp;&emsp;无

**返回值：**

&emsp;&emsp;无

``` python {.line-numbers}
class MyDialogCallback(RLPy.RDialogCallback):
    def __init__(self):
        RLPy.RDialogCallback.__init__(self)
    def OnDialogShow(self):
        print("OnDialogShow")
    def OnDialogHide(self):
        print("OnDialogHide")
    def OnDialogHide(self):
        print("OnDialogClose")
        return True

def run_script():
    rl_dialog = RLPy.RUi.CreateRDialog()
    dialog_callback = MyDialogCallback()
    rl_dialog.RegisterEventCallback(dialog_callback)
    rl_dialog.Show()
```
#### <div style="background: lightgray; padding: 8px;">RLPy.RDialogCallback.OnDialogHide(self)</div>
&emsp;&emsp;该函数在窗口隐藏时被调用，一般窗口很少隐藏感觉。

**参数：**

&emsp;&emsp;无

**返回值：**

&emsp;&emsp;无

``` python {.line-numbers}
class MyDialogCallback(RLPy.RDialogCallback):
    def __init__(self):
        RLPy.RDialogCallback.__init__(self)
    def OnDialogShow(self):
        print("OnDialogShow")
    def OnDialogHide(self):
        print("OnDialogHide")
    def OnDialogHide(self):
        print("OnDialogClose")
        return True

def run_script():
    rl_dialog = RLPy.RUi.CreateRDialog()
    dialog_callback = MyDialogCallback()
    rl_dialog.RegisterEventCallback(dialog_callback)
    rl_dialog.Show()
    rl_dialog.Hide()
```
#### <div style="background: lightgray; padding: 8px;">RLPy.RDialogCallback.OnDialogClose(self)</div>
&emsp;&emsp;该函数在窗口即将被关闭时被调用，在此之前会先调用回调函数 OnDialogHide()。

**参数：**

&emsp;&emsp;无

**返回值：**

&emsp;&emsp;return - bool[OUT]: 窗口真正关闭时会返回 True，但官方文档中手动返回 True

``` python {.line-numbers}
class MyDialogCallback(RLPy.RDialogCallback):
    def __init__(self):
        RLPy.RDialogCallback.__init__(self)
    def OnDialogShow(self):
        print("OnDialogShow")
    def OnDialogHide(self):
        print("OnDialogHide")
    def OnDialogHide(self):
        print("OnDialogClose")
        return True

def run_script():
    rl_dialog = RLPy.RUi.CreateRDialog()
    dialog_callback = MyDialogCallback()
    rl_dialog.RegisterEventCallback(dialog_callback)
    rl_dialog.Show()
    rl_dialog.Close()
```