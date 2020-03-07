# 非开发-配置

***


#####骨骼部件-配置示例（非必须）

> **[warning] 前提**
> 
> 前提：如果没有通过API来注册模型

``` yaml
pet:
  part:
    head:
      itemName: "pet1"
	  customModelData: 11289
      isHead: true
      isBody: false
      isAddToSkeleton: false
      skeleton: "body"
      addBox:
        offsetX: 0
        offsetY: 2
        offsetZ: 0
        eulerAngleX: 0
        eulerAngleY: 0
        eulerAngleZ: 0
```
***
####基本内容
***
#####格式
要开始设计模型，就要从标准格式开始 

部件是可以无限添加（小心爆炸了，滑稽）
> **[danger] 注意**
>
> 为了让其它部件的六个值完全可用
>
> 请设置一个部件为头部并添加空闲状态动态，而相关动作动态教程请从目录中寻找


``` yaml
pet:
  part:
    # 部件或骨骼的ID，在本配置中必须唯一
    boneID1:
      ...
    boneID2:
      ...
```
***
#####物品名称
该填项会很好的支持OptiFine
``` yaml
pet:
  part:
    head:
      # 物品名称
      itemName: "pet1"
```
***
#####物品模型数据
如果不想要OptiFine，那么这个填项值得你拥有
> **[danger]** 注意
>
> 只有对Minecraft-1.14及以上版本有效


``` yaml
pet:
  part:
    head:
      # 物品模型数据
      customModelData: 15587
```
***
#####设置或连接部位
你可以设置该部件为 head头部 或 body身体，如果前两者不是，那么请选定连接到某部件 

此外，头部和身体是唯一的（即不可多部件设置同一个头部或身体），也可以为空的（即不选头部或身体） 

连接部位有什么用处？答：如果主部件有动作动态值，则其子部件会跟随主部件移动或旋转而移动或旋转
``` yaml
pet:
  part:
    # 部件或骨骼的ID
    #   这里是头部
    head:
      # 物品名称
      itemName: "pet1"
      # 是否为头部
      isHead: true
      # 是否设置为身体
      #   如果设置为头部，就不要设置为身体
      isBody: false
      # 如果不是上面两项
      #   那么这个为是否给指定骨骼添加该部件
      isAddToSkeleton: false
      # 如果 isAddToSkeleton 为 true
      #   那么请填入骨骼的ID
      skeleton: "body"
```
***
#####部件位置与角度设置
在 额外教程-addBox 详细内容会了解到的
``` yaml
pet:
  part:
    boneID1:
      # 这里包含所有可填值，不填默认为0，可以复制拿去使用
      addBox:
        offsetX:
        offsetY:
        offsetZ:
        eulerAngleX:
        eulerAngleY:
        eulerAngleZ:
```
