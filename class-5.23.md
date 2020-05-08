---
sidebarDepth: 3
---

# 5.23课时 - 控制流 (if / else)

## 知识点

在这一堂课中，解释了如何使用 `if` `else` 和 `else if` 的使用方法

```swift
if 条件 {
    代码
} else {
    代码
}
```

当一个条件被认定为 `true` 的时候被执行，如果没有符合条件的情况，就会被执行 `else` 的代码块

例子

```swift
let number = 10

if number > 20 {
    print("常量 number 大于 20")
} else {
    print("常量 number 小于 20")
}
```

输出

```
常量 number 小于 20
```

还有一种是 `else if`

```swift
if 条件 {
    代码
} else if 条件 { 
    代码
} else {
    代码
}
```

相当于多了一条路走

```swift
let number = 13

if number >= 20 {
    print("常量 number 大于或等于 20")
} else if number > 10 && number < 20 {
    print("常量 number 在 10 和 20 之间")
} else {
    print("常量 number 小于或等于 10")
}
```

输出

```
常量 number 在 10 和 20 之间
```