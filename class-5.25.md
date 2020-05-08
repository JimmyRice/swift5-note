---
sidebarDepth: 3
---

# 5.25课时 - for 循环 1

## 知识点

在 Swift 中建立 for 循环的语法如下

```swift
for 变量 in 遍历对象 {
    代码
}
```

在遍历元素的时候会让变量内的值更新，不同的遍历对象类型都会有不同的输出结果

```swift
for index in 1...5 {
    print(index)
}
```

```
1
2
3
4
5
```

```swift
let text = "Hello, World"

for index in text {
    print(index)
}

```

```
H
e
l
l
o
,
 
W
o
r
l
d
```

很显然，每次遍历都会让 index 更新，并且执行一次代码块里面的代码

因为代码块中要求 `print` 出 `index` 的值，因此你会看到如上结果

利用它，你可以去做一个简单的有关 `5` 的乘法程序

```swift
for index in 1...9 {
    print(index * 5)
}
```

```
5
10
15
20
25
30
35
40
45
```

使用`区间值`的时候，第一次运行 `index` 的值就是 `1`，然后执行代码块中的 `print(index * 5)`

因为 `index` 是 `1`，所以 `1 * 5` 等于 `5`

在第二次执行的时候 `index` 的值被更新为了 `2`，然后再执行代码块因此为 `2 * 5` 等于 `10`

以此类推直到区间值最后一个数字 `9` 执行完后 for 循环才会结束

使用 `where` 这个保留字可以对 for 循环设定条件

```swift
for 变量 in 遍历对象 where 条件 {
    代码
}
```

例如

```swift
let text = "Hello, World"

for index in text {
    print(index, terminator: "")
}

```

这个代码中包含了一个叫做 `terminator` 的函数是一个新鲜东西，用于将文本输出成标准输出格式，当然，这并不是核心知识点之一

来看下输出

```
Hello, World
```

接下来我们使用 `where` 这个保留字给我们的循环设定一个条件

例如

```swift
let text = "Hello, World"

for index in text where index != ","{
    print(index, terminator: "")
}
```

输出

```
Hello World
```

你发现了什么？

少了一个 `,` 符号

那是因为我们通过 where 下达了一个条件: 让 `index` 这个变量变成 **不等于 (没有)** `,` 这个符号

因此输出的时候，`Hello, World` 就变成了 `Hello World`