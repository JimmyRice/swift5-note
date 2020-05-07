---
sidebarDepth: 3
---

# 4.15课时 - 数组

## 知识点

Swift 的数组索引会从 `0` 开始，让我们建立一个已 `Int` 作为数据类型的数组

```swift
let intArray = [1, 2, 3]
```

:::tip Swift 智能推断
Swift 会自动推断数据类型，因此我们并不需要手动声明这个是 `Int` 数据类型
:::

现在，当我们要取用数字 `1` 的时候，因为索引从 `0` 开始，因此我们使用以下方式调用

```swift
print(intArray[0])
```

那我们的 Console 将会输出

```
1
```

## 其他

实际上，Swift 的数组一般情况下是不能多个数据类型混杂在一起的，并不像类似于 JavaScript 一样的语言可以很随意的在一个数组中定义多个数据类型的值并调用

在 JavaScript 中你可以这么写

```javascript
var array = [1, "Hello, World", 3.14, true];
```

但是在 Swift 中你真的要这么做的话

```swift
let array = ["Hi", 3, 3.14, true] as [Any]
```

你需要在后面加入一个 `as [Any]`