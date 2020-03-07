#有关纹理与部件的显示
***
#####前言
> **[warning]** 请注意
>
> 这里仅讲纹理与部件显示的有关内容，若想学习模型制作，请另寻教程
> 
> 所有模型的原版材质必须是钻石锄子


***
#####耐久值
> **[danger]** 注意
>
> 主要用于Minecraft1.8版本
>
> imiPet的未来新版本将不再支持耐久值功能，决定使用前请三思


我们先看一下配置模型，耐久值的显示会根据部件ID而显示
``` yaml
pets:
  # 模型部件或骨骼配置
  part:
    # 部件或骨骼的ID
    #   这里是头部
    head:
```
再剖解纹理包看看，我们会发现这些是要一致才能显示
<div align=center>![avatar](https://dev.tencent.com/u/inrhINRH/p/tuchuang/git/raw/75302fd804b746663e01c8fc93f1c5676017c1ce/QQ%E5%9B%BE%E7%89%8720191215134904.png)
<div align=center>![avatar](https://dev.tencent.com/u/inrhINRH/p/tuchuang/git/raw/75302fd804b746663e01c8fc93f1c5676017c1ce/QQ%E5%9B%BE%E7%89%8720191215135907.png)
<div align=center>![avatar](https://dev.tencent.com/u/inrhINRH/p/tuchuang/git/raw/75302fd804b746663e01c8fc93f1c5676017c1ce/QQ%E5%9B%BE%E7%89%8720191215135838.png)
 
 
至于耐久值原理，我不多讲了，毕竟现在流行OptiFine
***
#####高清修复
高清修复就是OptiFine
与原版相比之下，OptiFine则更简单了
不过它与部件ID无关，而与物品名称有关
``` yaml
pets:
  # 模型部件或骨骼配置
  part:
    # 部件或骨骼的ID
    #   这里是头部
    head:
      # 物品名称
      itemName: "pet1"
```
我们来剖解纹理包看看
``` yaml
type=item
items=minecraft:diamond_hoe
nbt.display.Name=pet1
model=./head
```
可以看到，minecraft:diamond_hoe是钻石锄子的名称，pet1是物品名称
更详细的教程请看：http://www.imipet.com/threads/15/
***
#####模型数据
如果不想要耐久值或高清修复，那么有模型数据值得选择
> **[danger]** 注意
>
> 但是，只支持Minecraft-1.14及以上版本


``` yaml
pets:
  # 模型部件或骨骼配置
  part:
    # 部件或骨骼的ID
    #   这里是头部
    head:
      # 模型纹理数据（1.14及以上版本可用）
      customModelData: 4127
```
剖解纹理包看看
<div align=center>![avatar](https://inrhinrh.coding.net/p/tuchuang/d/tuchuang/git/raw/9f107514aa90ace3f765b31cd193fd00eccccdc6/pack1.png)
***
#####常见问题
> 纹理包版本过低？


提示旧版本是材质包内pack.mcmeta文件设置问题
``` yaml
{
  "pack": {
    "pack_format": 3
  }
}
```
请根据需要，修改数字
1.8-1.12 pack_format=3
1.13-1.14 pack_format=4


> 如何将多个纹理包放入同一纹理包？


请看教程：http://www.imipet.com/threads/23/


> 纹理包是什么？客户端如何使用纹理包？


这么简单都不懂，纹理包也就是材质包，也就是资源包，我只是喜欢这么叫


纹理包放入客户端的位置：.minecraft\resourcepacks


然后在客户端按 ESC键，点击资源包，放入右侧完成后自动加载资源包