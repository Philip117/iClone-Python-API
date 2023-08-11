# IC7 Python API:RLPy RIFaceComponent
&emsp;&emsp;对应 [**官方网页**](https://wiki.reallusion.com/IC_Python_API:RLPy_RIFaceComponent)。
&ensp;&ensp;&ensp;&ensp;Corresponding [**official page**](https://wiki.reallusion.com/IC_Python_API:RLPy_RIFaceComponent).

&emsp;&emsp;最后编辑：2023.08.11
&ensp;&ensp;&ensp;&ensp;Last modified: 2023.08.11
___
### 介绍 - Description
&emsp;&emsp;该类主要用于设置角色的面部和头部控制。RIFaceComponent 数据包括 12 个面部骨骼、60 个面部变形和 24 个自定义变形。 你可以在 Face Puppet 界面中打开详细信息面板，按 Ctrl+F2 显示更详细的数据。前面的编号数据是60个变形数据，接下来是12个面部骨骼数据，其余的属于自定义集。 面部12块骨头中的少数骨头没有任何作用。如果数据名称标记为“N/A”，你可以判断它是否没有效果，因此无效。此外，需要设置表情剪辑才能创建表情键。
&emsp;&emsp;在官方文档中只有几个函数，但通过阅读源码并实际测试可知应该还有几个函数可用。
___
### 类成员 - Class Methods
> #### **RLPy.Animation.GetExpressionNames(self, strType)**
&emsp;&emsp;该函数不存在于官方文档中，但在源码中可以发现，而且该函数已经加入了 i8 的官方文档，但参数不同了。

**参数：**

&emsp;&emsp;**strType** - str[IN]: 未知参数的作用，但通过测试和比较 i8，可知若传参空串，即 ""，在 i8 中仍会返回全部面部节点，但在 i7 中会返回空，必须且只能传参 "Custom"

**返回值：**

&emsp;&emsp;return - tuple[str][OUT]: 模型的面部节点

``` python {.line-numbers}
def run_script():
    avatar = RLPy.RScene.GetAvatars(RLPy.EAvatarType_All)[0]
    facial_component = avatar.GetFaceComponent()
    expression_names = facial_component.GetExpressionNames("Custom")
    print(expression_names)
```