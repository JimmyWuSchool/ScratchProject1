# 主畫面
- 小地圖
- 玩家 &rarr; 在中間
- 移動的背景

## 移動背景
### func
```
paint_background(x, y, block_x, block_y)
```
使用這個func必須可以畫出背景
```
x: 玩家的x
y: 玩家的y
block_x: 一個背景方塊的邊長(x)
block_y: 一個背景方塊的邊長(y)
```
### pattern
![background_pattern](https://github.com/user-attachments/assets/2706ece5-287f-4926-a0b7-a3e7383f1623)


## 小地圖
### func
```
paint_map(x, y, enemys_x[],  enemys_y[])
```
使用這個func必須可以畫出背景
```
x: 玩家的x
y: 玩家的y
enemys_x[]: 一個列表所有怪物的x
enemys_y[]: 一個列表所有怪物的y
// 怪物的x和y不用導入到func中，直接設為全域array
```

# 生怪機制
- 200 pixel 內不會有怪
- 5000 pixel 外不會有
- 怪物會自然的隨機移動
  - 不可以超出邊界

## if
```
if player_distance >= 200 && player_distance <= 5000:
  make_enemy()
else:
  dont_make_enemy()
```

---

# 變數
```
player_x: 玩家的x
player_y: 玩家的y
enemys_x[]: 一個列表所有怪物的x
enemys_y[]: 一個列表所有怪物的y
```

---

# 注意
- 地圖總共 10000 * 10000
- 要有邊界
- 移動要有物理
- 範圍都是圓形的

# 如果有更多時間
- 美化
- 玩家有血量
- 玩家可以攻擊
- 怪物在玩家 150 pixel 內會追逐玩家
