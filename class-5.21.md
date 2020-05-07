---
sidebarDepth: 3
---

# 5.21课时 - 函数参数

## 知识点

函数中小括号内就是 **参数**

参数可以理解为是一个函数中所使用的变量，其他地方无法使用，只有特定函数可以使用

```swift
func repeatWord(word: String) {
    print(word)
}

repeatWord(word: "Hello")
```

输出结果为:

```
Hello
```

## 其他

如果有多个参数呢？使用 `,` 来将不同参数分开

```swift
func buyMeat(参数1, 参数2, 参数3) {
    代码...
}
```

上个例子

```swift
func buyMeat(money: Int, nums: Int, meatPrice: Int) {
    let price = nums * meatPrice
    print("你今天带上了 \(money) 块钱\n今日肉价 \(meatPrice) 一斤，你打算买 \(nums) 斤的肉\n因此一共需要 \(price) 块钱")
    if money < price {
        print("你的钱钱不够")
    } else {
        let leftMoney = money - price
        print("成功购买了 \(nums) 斤肉，支付 \(price)，找回 \(leftMoney) 块钱")
    }
}

buyMeat(money: 100, nums: 3, meatPrice: 30)
```

输出:

```
你今天带上了 100 块钱
今日肉价 30 一斤，你打算买 3 斤的肉
因此一共需要 90 块钱
成功购买了 3 斤肉，支付 90，找回 10 块钱
```