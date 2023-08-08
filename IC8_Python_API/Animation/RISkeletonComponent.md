# ICX Python API:RLPy RISkeletonComponent
&emsp;&emsp;对应 [**官方网页**]()。
&ensp;&ensp;&ensp;&ensp;Corresponding [**official page**]().

&emsp;&emsp;最后编辑：2023.08.07
&ensp;&ensp;&ensp;&ensp;Last modified: 2023.08.07
___
### 介绍 - Description
&emsp;&emsp;该类主要负责模型的骨骼和动画切片的管理。
___
### 类成员 - Class Methods
> #### **RLPy.RISkeletonComponent.AddClip(self, kTime)**
&emsp;&emsp;为模型添加一段切片。如果是 FBX 模型，则会返回 None。

**参数：**

&emsp;&emsp;**kTime** - RTime[IN]: 添加切片的时间

**返回值：**

&emsp;&emsp;return - RIClip[OUT]: 新创建的切片

``` python {.line-numbers}
def run_script():
    avatar = RLPy.RScene.GetAvatars(RLPy.EAvatarType_All)[0]
    skeleton_component = avatar.GetSkeletonComponent()
    clip = skeleton_component.AddClip(RLPy.RGlobal.GetTime())
    print(clip)
```

</br>
</br>