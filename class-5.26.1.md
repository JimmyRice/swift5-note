---
sidebarDepth: 3
---

# 5.26.1知识点部分 - for 循环 2

## 知识点

在第一小结部分中的 For 循环知识点主要讲了 Swift 中一个叫做 `reversed()` 的函数

根据 [Apple Developer](https://developer.apple.com/documentation/swift/array/1690025-reversed) 官方文档的介绍，这个函数用于将一个 `合集` 按照反方向显示

来看一个简单的 Demo

```swift
for index in (1...5).reversed() {
    print("我有\(index)块蛋糕，吃了一块之后还剩下\(index - 1)块蛋糕")
}
```

输出

```
我有5块蛋糕，吃了一块之后还剩下4块蛋糕
我有4块蛋糕，吃了一块之后还剩下3块蛋糕
我有3块蛋糕，吃了一块之后还剩下2块蛋糕
我有2块蛋糕，吃了一块之后还剩下1块蛋糕
我有1块蛋糕，吃了一块之后还剩下0块蛋糕
```

很容易可以发现，这一次的输出是从 `5` 到 `1` 而不是从 `1` 到 `5`

区间值中可以将 (数字...数字) 替换成某个常量或者变量