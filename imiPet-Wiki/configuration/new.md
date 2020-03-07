# 非开发-配置

***
> 版本：2.4.2


新增进化形态展示，需要的可以自行写入，不需要的不用写入
``` yaml
pet:
    # 进化仓界面
    vgEvolution:
    # 进化后形态的展示
      show:
        # 位置
        x: 150
        y: 150
        # 尺寸
        size: 70
```
***
#####模型配置增删改内容
> 版本：2.4.0


***
> **[danger]** 删除内容

``` yaml
  # 宠物展示图 - 大
  #  推荐图片大小 250x250 或更大
  imageShowBig: ""
  # 宠物展示图 - 小
  imageShowSmall: ""
```
  
> **[success]** 增加内容


``` yaml
  # 宠物展示 - 实体绘制
  entityDraw:
    # 物品名称
    itemName: "§a§3§a§3§b§7§c§a§70"
    # 模型数据
    customModelData: 5000
    # 主界面
    vgHome:
      big:
        # 位置
        x: 95
        y: 150
        # 尺寸
        size: 100
      # 小(选择框)
      small:
        # 位置
        x: 15
        y: 26
        # 选择框递增X坐标(支持负数)
        addX: 10
        # 尺寸
        size: 20
    # 经验库界面
    vgExp:
      # 小(选择框)
      small:
        # 位置(已选择框)
        firstX: 88
        firstY: 56
        # 位置(待选择框)
        x: 15
        y: 26
        # 选择框递增X坐标(支持负数)
        addX: 10
        # 尺寸
        size: 20
    vgTransferPackWarehouse:
      # 小(选择框)
      small:
        # 位置(待选择框)
        x: 15
        y: 26
        # 选择框递增X坐标(支持负数)
        addX: 10
        # 尺寸
        size: 20
    # 进化仓界面
    vgEvolution:
      big:
        # 位置
        x: 65
        y: 100
        # 尺寸
        size: 70
      # 小(选择框)
      small:
        # 位置(已选择框)
        firstX: 65
        firstY: 161
        # 位置(待选择框)
        x: 15
        y: 26
        # 选择框递增X坐标(支持负数)
        addX: 10
        # 尺寸
        size: 20
    # 更新信息界面
    vgUpdateInfo:
      big:
        # 位置
        x: 95
        y: 150
        # 尺寸
        size: 100
      # 小(选择框)
      small:
        # 位置(已选择框)
        firstX: 35
        firstY: 201
        # 位置(待选择框)
        x: 15
        y: 26
        # 选择框递增X坐标(支持负数)
        addX: 10
        # 尺寸
        size: 20
    # 宠物仓库界面
    vgWarehouse:
      # 小(选择框)
      small:
        # 位置(待选择框)
        x: 40
        y: 72
        # 选择框递增Y坐标(支持负数)
        addY: 45
        # 尺寸
        size: 28
```