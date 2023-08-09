# IC8 Python API:RLPy RApplication
&emsp;&emsp;对应 [**官方网页**](https://wiki.reallusion.com/IC8_Python_API:RLPy_RApplication)。
&ensp;&ensp;&ensp;&ensp;Corresponding [**official page**](https://wiki.reallusion.com/IC8_Python_API:RLPy_RApplication).

&emsp;&emsp;最后编辑：2023.08.03
&ensp;&ensp;&ensp;&ensp;Last modified: 2023.08.03
___
### 介绍 - Description
&emsp;&emsp;该类主要负责 iClone 层面的信息查询。
___
### 类成员 - Class Methods
> #### **RLPy.RApplication.GetCustomDataPath()**
&emsp;&emsp;在 iClone 中，素材库文件夹下有两个子文件夹，一个是 Reallusion Custom，另一个是 Reallusion Templates。该函数则是获取 Reallusion Custom 文件夹的绝对路径。

**参数：**

&emsp;&emsp;无

**返回值：**

&emsp;&emsp;return - str[OUT]: Reallusion Custom 文件夹的绝对路径

``` python {.line-numbers}
def run_script():
    path_custom_data = RLPy.RApplication.GetCustomDataPath()
    print(path_custom_data)
```

</br>
</br>

> #### **RLPy.RApplication.GetTemplateDataPath()**
&emsp;&emsp;在 iClone 中，素材库文件夹下有两个子文件夹，一个是 Reallusion Custom，另一个是 Reallusion Templates。该函数则是获取 Reallusion Template 文件夹的绝对路径。

**参数：**

&emsp;&emsp;无

**返回值：**

&emsp;&emsp;return - str[OUT]: Reallusion Template 文件夹的绝对路径

``` python {.line-numbers}
def run_script():
    path_template_data = RLPy.RApplication.GetTemplateDataPath()
    print(path_template_data)
```