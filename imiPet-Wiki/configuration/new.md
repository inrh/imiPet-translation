# 非开发-配置

***
> 版本：3.0.0-Beta


对模型ID格式没有严格限制  
也就是说，可以不需要冒号 :  


删除了原来的模型配置以下的值  
pet.animationList  
pet.animationTime  
pet.part  
pet.entityDraw.itemName  
pet.entityDraw.customModelData  

手持喂养宠物的值调整了，更加简单
``` yaml
pet:
  # 关于手持喂养
  eat:
    # 是否启用
    enable: true
    # 格式为 标识符:数值:数量:脚本:脚本的值
    # 标识符仅支持 material name lore
    list:
      - 'material:APPLE:1:addHP:2'
      - 'name:&a卡哇伊:1:addFood:2'
      - 'lore:&a描述:1:command_op:give @player minecraft:apple 1'
```

坐骑的位置修改了，位于pet父节点下
``` yaml
pet:
  # 关于坐骑
  ride:
    # 是否允许坐骑
    enable: false
    # 是否为小型盔甲架(坐骑时)
    isSmall: true
    # 是否可以飞行，否则是跳跃
    canFly: false
```


新增以下值，所有模型由纹理包控制
``` yaml
pet:
  # 关于模型与动态模型
  animation:
    # 关于模型位置
    location:
      # 显示高度
      h: 1
    # 空闲状态
    idle:
      # 物品名称
      itemName: "§8"
      # 模型数据，仅支持1.14+
      customModelData: 10000
    # 行走状态
    walk:
      itemName: "§a"
      customModelData: 10001
    # 攻击状态
    attack:
      itemName: "§5"
      customModelData: 10002
      # 显示攻击动作动态时长，秒
      time: 5
```
