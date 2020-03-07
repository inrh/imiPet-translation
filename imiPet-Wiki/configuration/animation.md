# 非开发-配置

***


#####动态动作-配置示例
``` yaml
pet:
  # 动作动态启用与否列表
  animationList:
    # 空闲状态
    idle: true
    # 移动状态
    walk: true
    # 攻击状态
    attack: true
  # 模型部件或骨骼配置
  part:
    # 部件或骨骼的ID
    head:
      # 动态设置
      # 空闲状态
      animationIdle:
        # 是否启用
        isAnimation: true
        # 设置帧数
        keyFrame:
          1:
            second: 0
            eulerAngleX: 0
            eulerAngleY: 0
            eulerAngleZ: 0
            offsetX: 0
            offsetY: 0
            offsetZ: 0
          2:
            second: 30
            eulerAngleX: 0
            eulerAngleY: 0
            eulerAngleZ: 0
            offsetX: 0
            offsetY: 0
            offsetZ: 0
      # 移动状态
      animationWalk:
        # 是否启用
        isAnimation: true
        # 设置帧数
        keyFrame:
          1:
            second: 0
            eulerAngleX: 0
            eulerAngleY: 0
            eulerAngleZ: 0
            offsetX: 0
            offsetY: 0
            offsetZ: 0
          2:
            second: 20
            eulerAngleX: 0
            eulerAngleY: 0
            eulerAngleZ: 0
            offsetX: 0
            offsetY: 0
            offsetZ: 0
      # 攻击状态
      animationAttack:
        # 是否启用
        isAnimation: true
        # 设置帧数
        keyFrame:
          1:
            second: 0
            eulerAngleX: 0
            eulerAngleY: 0
            eulerAngleZ: 0
            offsetX: 0
            offsetY: 0
            offsetZ: 0
          2:
            second: 5
            eulerAngleX: 0
            eulerAngleY: 0
            eulerAngleZ: 0
            offsetX: 0
            offsetY: 0
            offsetZ: 0
```
***
#####动作动态启用列表
``` yaml
pet:
  # 动作动态启用与否列表
  animationList:
    # 空闲状态
    idle: true
    # 移动状态
    walk: true
    # 攻击状态
    attack: true
```
***
#####动态设置
``` yaml
pet:
  part:
    boneID:
      # 动态设置
      # 某动作状态（可选：animationIdle、animationWalk、animationAttack）
      XXX:
        # 是否启用动态
        isAnimation: true
        # 设置帧数（不少于2个，可以无限个）
        keyFrame:
          1:
            # 触发动作事件（诸如走路）后多长时间调整部件的位置、角度
            second: 0
            # ...
            eulerAngleX: 15
            eulerAngleY: 0
            eulerAngleZ: 0
            offsetX: 0
            offsetY: 0
            offsetZ: 0
          2:
            second: 20
            eulerAngleX: 15
            eulerAngleY: 0
            eulerAngleZ: 0
            offsetX: 0
            offsetY: 0
            offsetZ: 0
          xx:
            ...
```