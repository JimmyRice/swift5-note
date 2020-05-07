---
sidebarDepth: 3
---

# 5.22课时 - 返回值 (Return)

## 知识点

使用以下语法告诉 Swift 这个函数有返回值

```swift
func 函数名(参数) -> 返回值数据类型 {
    代码...
    ...
    return
}
```

看个例子

```swift
import UIKit

func buyMeat(money: Int, nums: Int, meatPrice: Int) -> Int {
    print("今天肉价 \(meatPrice) 块钱一斤，你一共有 \(money) 块钱，打算要买 \(nums) 斤肉")
    let price = nums * meatPrice
    let leftMoney = money - price
    return leftMoney
}

let leftMoney = buyMeat(money: 100, nums: 3, meatPrice: 10)
```

现在这个常量 `leftMoney` 就被赋予了函数 `buyMeat` 的返回值 `70`

用 `print` 输出验证一下

```swift
print(leftMoney)
```

输出

```swift
今天肉价 10 块钱一斤，你一共有 100 块钱，打算要买 3 斤肉
70
```

## 其他

如果你需要返回多个返回值，可以考虑使用 **元组**

就像这样

```swift
func 函数名(参数) -> (数据类型1, 数据类型2, 数据类型3) {
    代码...
    ...
    return
}

let 变量 = 函数名()
```

当我要获取元组中的某个返回值的时候使用

```swift
print(变量.0) // 输出 数据类型1的数据
print(变量.1) // 输出 数据类型2的数据
print(变量.2) // 输出 数据类型3的数据
```

上个例子

```swift
import UIKit

func buyMeat(money: Int, nums: Int, meatPrice: Int) ->(Bool, Int, Int) {
    let price = nums * meatPrice
    let leftMoney = money - price
    print("你今天带上了 \(money) 块钱，准备去买 \(nums) 斤的肉\n今日的肉价是 \(meatPrice) 块钱一斤")
    if money < price {
        print("你的钱钱不够")
        return (false, money, leftMoney)
    } else {
        print("你成功购买了 \(nums) 斤的肉，一共花费 \(price) 块钱，找回 \(leftMoney) 块钱")
        return (true, money, leftMoney)
    }
}

func buyGame(money: Int, gamePrice: Int){
    print("你还剩下 \(money) 块钱，因此你想到要去氪游戏，氪氪氪氪带劲啦。\n氪完 \(gamePrice) 之后，你仅仅剩下 \(money - gamePrice) 块钱惹")
}

func start() {
    let money = 1000
    let nums = 3
    let meatPrice = 100
    let buyMeatReturn = buyMeat(money: money, nums: nums, meatPrice: meatPrice)
    if buyMeatReturn.0 != true {
        print("看来你不够钱买肉，交易取消了，去买游戏吧")
        buyGame(money: buyMeatReturn.1, gamePrice: buyMeatReturn.1)
    } else {
        print("看来你成功买了肉，你还剩下 \(buyMeatReturn.2) 块钱")
        buyGame(money: buyMeatReturn.2, gamePrice: buyMeatReturn.2)
    }
}

start()
```

输出

```
你今天带上了 1000 块钱，准备去买 3 斤的肉
今日的肉价是 100 块钱一斤
你成功购买了 3 斤的肉，一共花费 300 块钱，找回 700 块钱
看来你成功买了肉，你还剩下 700 块钱
你还剩下 700 块钱，因此你想到要去氪游戏，氪氪氪氪带劲啦。
氪完 700 之后，你仅仅剩下 0 块钱惹
```

或者试试另一种情况

```swift
import UIKit

func buyMeat(money: Int, nums: Int, meatPrice: Int) ->(Bool, Int, Int) {
    let price = nums * meatPrice
    let leftMoney = money - price
    print("你今天带上了 \(money) 块钱，准备去买 \(nums) 斤的肉\n今日的肉价是 \(meatPrice) 块钱一斤")
    if money < price {
        print("你的钱钱不够")
        return (false, money, leftMoney)
    } else {
        print("你成功购买了 \(nums) 斤的肉，一共花费 \(price) 块钱，找回 \(leftMoney) 块钱")
        return (true, money, leftMoney)
    }
}

func buyGame(money: Int, gamePrice: Int){
    print("你还剩下 \(money) 块钱，因此你想到要去氪游戏，氪氪氪氪带劲啦。\n氪完 \(gamePrice) 之后，你仅仅剩下 \(money - gamePrice) 块钱惹")
}

func start() {
    let money = 100
    let nums = 3
    let meatPrice = 100
    let buyMeatReturn = buyMeat(money: money, nums: nums, meatPrice: meatPrice)
    if buyMeatReturn.0 != true {
        print("看来你不够钱买肉，交易取消了，去买游戏吧")
        buyGame(money: buyMeatReturn.1, gamePrice: buyMeatReturn.1)
    } else {
        print("看来你成功买了肉，你还剩下 \(buyMeatReturn.2) 块钱")
        buyGame(money: buyMeatReturn.2, gamePrice: buyMeatReturn.2)
    }
}

start()
```

输出

```
你今天带上了 100 块钱，准备去买 3 斤的肉
今日的肉价是 100 块钱一斤
你的钱钱不够
看来你不够钱买肉，交易取消了，去买游戏吧
你还剩下 100 块钱，因此你想到要去氪游戏，氪氪氪氪带劲啦。
氪完 100 之后，你仅仅剩下 0 块钱惹
```