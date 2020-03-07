# 非开发-配置

***
> **[warning]** 提示
>
> 新版较旧版增删改内容：[点击查看](http://wiki.imipet.com/configuration/new.html)


***
#####基本属性-配置示例（必须）


``` yaml
pet:
  # 模型唯一ID
  #modelId: "default:pet"
  modelId: "demomodel:phantom_empress"
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
    # 进化后形态的展示
      show:
        # 位置
        x: 150
        y: 150
        # 尺寸
        size: 70
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
  #
  #  可用数学：
  #    () 括号
  #    * 乘法
  #    / 除法
  #    + 加法
  #    - 减法
  #    还要更多请看：https://www.runoob.com/jsref/jsref-obj-math.html
  #
  # 玩家获得经验的同时也额外存入到经验存储盒
  #   变量
  #     add_exp 玩家获得的经验值
  #   当然，玩家获得的经验不会因而减少
  addExpByPlayer: "(Math.random()*(add_exp*0.2))+(add_exp*0.1)"
  # 关于宠物经验等级公式
  #   变量
  #     level 宠物升级前的等级
  levelExpFormula: "30*(level*level*level+5*level)-10"
  # 关于宠物最低攻击公式
  #   变量
  #     level 宠物升级前的等级
  #     min_damage 宠物升级前得最低攻击
  addMinAttackFormula: "min_damage+0.3"
  # 关于宠物最高攻击公式
  #   变量
  #     level 宠物升级前的等级
  #     max_damage 宠物升级前得最高攻击
  addMaxAttackFormula: "max_damage+0.3"
  # 关于宠物活力公式
  #   变量
  #     level 宠物升级前的等级
  #     max_food 宠物升级前的最大活力
  addFoodFormula: "max_food+10"
  # 关于宠物最大血量公式
  #   变量
  #     level 宠物升级前的等级
  #     max_hp 宠物升级前的最大血量
  addMaxHPFormula: "max_hp+10"
  # 回复血量需求
  cureHP:
    requirement:
      # 需要经济
      #   回复一血需要多少经济
      money: 0.1
      # 是否允许通过MC回血药水对宠物回血
      potion: false
  # 关于宠物进化
  evolution:
    # 是否可以进化
    enable: false
    requirement:
      # 进化所需宠物等级
      level: 10
      # 进化所需经济
      money: 300
    # 点击进化按钮的信息
    text:
      - "&f                                            "
      - "&f它..."
      - "&f一个天使的化身"
      - "&f达到一定高度后，终将如仙境般的转化"
      - "&f"
      - "&6进化条件"
      - "&f需要达到 &c%imipet_evolutionlevel% &f级"
      - "&f"
      - "&6如果满足条件，请问，是否确定进化"
      - "&f"
      - "&7&l[&a点击确定&7&l]"
      - "&f"
    # 指定新的模型ID
    newModelId: "null:aaa"
  # 宠物活力值
  food:
    # 是否会消耗活力
    enable: true
    # 活力补充需求
    requirement:
      # 需要经济
      #   补充一活力需要多少经济
      money: 0.1
  # 基本值
  basis:
    display:
      # 默认的宠物名称
      name: "小天使"
      # 名称格式
      format: "&7[&6主人：&f%imipet_owner%&7] &f%imipet_name%"
      # 是否显示名称
      show: true
      # 可选：hd，tr
      useShow: hd
      # 全息
      hd:
        # 显示名称Y轴
        height: 2
        # 显示名称X轴
        x: 0
        # 显示名称Z轴
        z: 0
        formatList:
          - "&7[&6主人：&f%imipet_owner%&7][&flv.%imipet_level%&7]"
          - "&f%imipet_name%"
          - "&c血量 &f%imipet_nowhp%&7/&f%imipet_maxhp%"
      # 太弱全息
      tr:
        # 显示名称Y轴
        height: 2
        # 显示名称X轴
        x: 0
        # 显示名称Z轴
        z: 0
        formatList:
          - "&7[&6主人：&f%imipet_owner%&7][&flv.%imipet_level%&7]"
          - '&e%animations_typewriter?pause=3,reverse=true_%imipet_name%%<update:5>'
          - "&c血量 &f%imipet_nowhp%&7/&f%imipet_maxhp%"
    # 初始血量
    HP: 20
    # 初始伤害范围
    minDamage: 2
    maxDamage: 6
    # 初始活力值
    food: 20
    # 初始最极经验值
    exp: 100
    # 等级上限
    level: 100
    # 关于坐骑
    ride:
      # 是否允许坐骑
      enable: false
      # 是否为小型盔甲架(坐骑时)
      isSmall: true
      # 是否可以飞行，否则是跳跃
      canFly: false
  # 交互式功能
  interaction:
    # 显示宠物信息
    info:
      # 是否启用
      enable: true
      # 优先显示方式 (hd 或 vexview)
      show: tr
      # 全息
      hd:
        # 显示时长 (秒)
        stayTime: 6
        stringList:
          - "&f名称： %imipet_name%"
          - "&f血量 %imipet_nowhp%&7/&f%imipet_maxhp%"
        # 全息位置
        x: 1
        y: 1
        z: 0
      # 太弱全息
      tr:
        # 显示时长 (秒)
        stayTime: 6
        stringList:
          - 'item:<head:%player_name%>'
          - '&b名称 %animations_glow?normal=&8&l,start=&3&l,middle=&b&l,end=&3&l,size=5_%imipet_name%%<update:3>'
          - ''
          - '&c等级 %animations_pulse?color=cyan_%imipet_level%%<update:10>'
          - ''
          - '&e%animations_typewriter?pause=3,reverse=true_看什么看，没见过帅锅嘛%<update:5>'
        # 全息位置
        x: 1
        y: 3
        z: 0
  # 喂养功能
  eat:
    # 是否启用
    enable: true
    # 食物列表
    foodList:
      # 判断食物名称和Lore
      stringList:
        # 食物ID
        1:
          # 所需物品数量
          amount: 1
          # 所有名称列表
          name:
            - "苹果"
            - "&c月饼"
            - "&f冰心素块"
          # 所有Lore列表
          lore:
            - "&8奥&f力&8给&7之块"
            - "卡哇伊"
          script:
            - "addHP:10"
            - "addFood:10"
            - "command_op:gamemode adventure %player_name%"
        meizu:
          # 所需物品数量
          amount: 2
          lore:
            - "&8奥&f力&8给&7之块"
            - "嘻嘻哈哈"
          script:
             - "addHP:1"
             - "addFood:1"
             - "command_op:give %player_name% minecraft:apple"
```


***


####基本属性
***
#####模型代号
> **[warning] 注意以下两点**
>
> 在所有宠物模型中必须是唯一性
>
> （不可缺少符号 : ）


``` yaml
pet:
  modelId: "aaa:bbb"
```
***
#####宠物展示
主要用于VexView界面
``` yaml
pet:
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
    # 进化后形态的展示
      show:
        # 位置
        x: 150
        y: 150
        # 尺寸
        size: 70
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
***
#####基本值
主要用于设置玩家获得的新宠物的初始基本值
``` yaml
pet:
  # 基本值
  basis:
    display:
      # 默认的宠物名称
      name: "小天使"
      # 名称格式
      format: "&7[&6主人：&f%imipet_owner%&7] &f%imipet_name%"
      # 是否显示名称
      show: true
      # 可选：hd，tr
      useShow: hd
      # 全息
      hd:
        # 显示名称Y轴
        height: 2
        # 显示名称X轴
        x: 0
        # 显示名称Z轴
        z: 0
        formatList:
          - "&7[&6主人：&f%imipet_owner%&7][&flv.%imipet_level%&7]"
          - "&f%imipet_name%"
          - "&c血量 &f%imipet_nowhp%&7/&f%imipet_maxhp%"
      # 太弱全息
      tr:
        # 显示名称Y轴
        height: 2
        # 显示名称X轴
        x: 0
        # 显示名称Z轴
        z: 0
        formatList:
          - "&7[&6主人：&f%imipet_owner%&7][&flv.%imipet_level%&7]"
          - '&e%animations_typewriter?pause=3,reverse=true_%imipet_name%%<update:5>'
          - "&c血量 &f%imipet_nowhp%&7/&f%imipet_maxhp%"
    # 初始血量
    HP: 20
    # 初始伤害范围
    minDamage: 2
    maxDamage: 6
    # 初始活力值
    food: 20
    # 初始最极经验值
    exp: 100
    # 等级上限
    level: 100
    # 关于坐骑
    ride:
      # 是否允许坐骑
      enable: true
      # 是否为小型盔甲架(坐骑时)
      isSmall: true
      # 是否可以飞行，否则是跳跃
      canFly: true
```
其中，变量内容有如下
``` yaml
%imipet_owner%  主人名称
%imipet_name%  宠物名称
%imipet_level%  宠物等级
%imipet_nowexp%  宠物当前经验
%imipet_maxexp%  宠物最大经验
%imipet_nowhp%  宠物当前血量
%imipet_maxhp%  宠物最大血量
%imipet_nowfood%  宠物当前活力
%imipet_maxfood%  宠物最大活力
%imipet_damage% 宠物攻击力
```
***
#####交互式显示宠物信息
``` yaml
pet:
  # 交互式功能
  interaction:
    # 显示宠物信息
    info:
      # 是否启用
      enable: true
      # 优先显示方式 (hd 或 vexview)
      show: tr
      # 全息
      hd:
        # 显示时长 (秒)
        stayTime: 6
        stringList:
          - "&f名称： %imipet_name%"
          - "&f血量 %imipet_nowhp%&7/&f%imipet_maxhp%"
        # 全息位置
        x: 1
        y: 1
        z: 0
      # 太弱全息
      tr:
        # 显示时长 (秒)
        stayTime: 6
        stringList:
          - 'item:<head:%player_name%>'
          - '&b名称 %animations_glow?normal=&8&l,start=&3&l,middle=&b&l,end=&3&l,size=5_%imipet_name%%<update:3>'
          - ''
          - '&c等级 %animations_pulse?color=cyan_%imipet_level%%<update:10>'
          - ''
          - '&e%animations_typewriter?pause=3,reverse=true_看什么看，没见过帅锅嘛%<update:5>'
        # 全息位置
        x: 1
        y: 3
        z: 0
```
其中，变量内容有如下
``` yaml
%imipet_owner%  主人名称
%imipet_name%  宠物名称
%imipet_level%  宠物等级
%imipet_nowexp%  宠物当前经验
%imipet_maxexp%  宠物最大经验
%imipet_nowhp%  宠物当前血量
%imipet_maxhp%  宠物最大血量
%imipet_nowfood%  宠物当前活力
%imipet_maxfood%  宠物最大活力
%imipet_damage% 宠物攻击力
```
***
#####手持喂养
``` yaml
pet:
  # 喂养功能
  eat:
    # 是否启用
    enable: true
    # 食物列表
    foodList:
      # 判断食物名称和Lore
      stringList:
        # 食物ID
        1:
          # 所需物品数量
          amount: 1
          # 所有名称列表
          name:
            - "苹果"
            - "&c月饼"
            - "&f冰心素块"
          # 所有Lore列表
          lore:
            - "&8奥&f力&8给&7之块"
            - "卡哇伊"
          script:
            - "addHP:10"
            - "addFood:10"
            - "command_op:gamemode adventure %player_name%"
        meizu:
          # 所需物品数量
          amount: 2
          lore:
            - "&8奥&f力&8给&7之块"
            - "嘻嘻哈哈"
          script:
             - "addHP:1"
             - "addFood:1"
             - "command_op:give %player_name% minecraft:apple"
```
其中 script 是脚本  
目前仅支持如下（请严格遵守格式）
``` yaml
- "addHP:XXX" # XXX支持整数和小数点
- "addFood:XXX" # XXX仅支持整数
- "command_op:xxx a" # 以OP身份运行命令/xxx a 支持变量%player_name%
```
判断物品的详细内容  
系统首先从第一个开始判断，配对不成功会继续往下一行判断  
有一个地方值得注意：  
- 如果这样的**顺序**
``` yaml
lore:
  - "&8奥&f力&8给&7之块"
  - "卡哇伊"
name:
  - "苹果"
  - "&c月饼"
```  
根据代码逻辑，依然会先从**name**开始判断  

只要**name**或**lore**其中一行配对成功，就终止下一行判断，开始触发脚本
***
#####关于公式填项
> [warning]
>
> 数学算法主要使用JavaScript Math
>
> 具体请看目录中的 额外教程-数学算法


``` yaml
pet:
  #  可用数学：
  #    () 括号
  #    * 乘法
  #    / 除法
  #    + 加法
  #    - 减法
  #    还要更多请看：https://www.runoob.com/jsref/jsref-obj-math.html
  #
  # 玩家获得经验的同时也额外存入到经验存储盒
  #   变量
  #     add_exp 玩家获得的经验值
  #   当然，玩家获得的经验不会因而减少
  addExpByPlayer: "(Math.random()*(add_exp*0.2))+(add_exp*0.1)"
  # 关于宠物经验等级公式
  #   变量
  #     level 宠物升级前的等级
  levelExpFormula: "30*(level*level*level+5*level)-10"
  # 关于宠物最低攻击公式
  #   变量
  #     level 宠物升级前的等级
  #     min_damage 宠物升级前得最低攻击
  addMinAttackFormula: "min_damage+2"
  # 关于宠物最高攻击公式
  #   变量
  #     level 宠物升级前的等级
  #     max_damage 宠物升级前得最高攻击
  addMaxAttackFormula: "max_damage+3"
  # 关于宠物活力公式
  #   变量
  #     level 宠物升级前的等级
  #     max_food 宠物升级前的活力
  addFoodFormula: "max_food+10"
  # 关于宠物最大血量公式
  #   变量
  #     level 宠物升级前的等级
  #     max_hp 宠物升级前的最大血量
  addMaxHPFormula: "max_hp+10"
```
***
#####关于回复血量需求
``` yaml
pet:
  cureHP:
    requirement:
      # 需要经济
      #   回复一血需要多少经济
      money: 0.1
      # 是否允许通过MC回血药水对宠物回血
      potion: false
```
***
#####关于回复活力需求
``` yaml
  # 宠物活力值
  food:
    # 是否会消耗活力
    enable: true
    # 活力补充需求
    requirement:
      # 需要经济
      #   补充一活力需要多少经济
      money: 0.1
```
***
#####关于进化需求
``` yaml
pet:
  # 关于宠物进化
  evolution:
    # 是否可以进化
    enable: true
    requirement:
      # 进化所需宠物等级
      level: 10
      # 进化所需经济
      money: 300
    # 点击进化按钮的信息
    text:
      - "&f                                            "
      - "&f它..."
      - "&f一个天使的化身"
      - "&f达到一定高度后，终将如仙境般的转化"
      - "&f"
      - "&6进化条件"
      - "&f需要达到 &c%imipet_evolutionlevel% &f级"
      - "&f"
      - "&6如果满足条件，请问，是否确定进化"
      - "&f"
      - "&7&l[&a点击确定&7&l]"
      - "&f"
    # 指定新的模型ID
    newModelId: "demomodel:phantom_empress"
```
模型将进化为指定模型ID  
实际上就是改变形态，不会对宠物数据初始化  
但是，相关公式指向新模型ID
***

