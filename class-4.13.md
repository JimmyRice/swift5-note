---
sidebarDepth: 3
---

# 4.13课时 - 声明变量与随机数产生

## 知识点
### 声明变量与类型
大家在声明变量的时候，使用`var`即可；标准格式为`var + 变量名`

在声明变量后建议声明类型，一般来说初学常用类型为==Int(整数)==或者==String(字符串)==，请注意**开头大写**；标准格式为`var + 变量名: 类型 = 内容`

例如下面代码声明了一个名为**number1**的变量，类型是==Int(整数)==，数字为`6`

```swift
var number1: Int = 6
```

又例如下面代码声明了一个为**HelloWorld**的变量，类型是==String(字符串)==，内容为`Hello, World!`

```swift
var HelloWorld: String = "Hello, World"
```

### 产生随机数
在我们需要使用Swift产生**整数类**的随机数的时候，我们可以使用==Int.random(in: A...B)==，其中`A...B`是区间值；例如要生成1到50的随机数可以这么表达 ==(注意这里未赋值)==:

```swift
Int.random(in: 1...50)
```

### 输出
输出算是本节课程的小知识点，可以用于输出字符串和特定的变量与常量

例如输出`Hello, World`就这么写:

```swift
print("Hello, World")
```

输出一个1到50的随机数可以使用:

```swift
var randomNumber1 = Int.random(in: 1...50)

print(randomNumber1)
```

==注意这里的例子与教程中不太一样，因为在教程中属于**重新赋值**==

如果是重新赋值的情况，则不用在前面加上`var`，我们来模拟一下:

```swift
var randomNumber1: Int

randomNumber1 = Int.random(in: 1...50)

print(randomNumber1)
```

## 其他
1. 在Swift中类型有非常多种，初学有以下类型:

| 类型 | 中文 | 解释 |
|------|------|------|
|Int|整数|整数数字|
|String|字符串|字符串|
|Float|浮点数|32位二进制浮点数|
|Double|浮点数|64位二进制浮点数|
|Bool|布尔值|返回True(真) 或 False(假)|

## 建议
在该节课程中，Lebus[^Teacher]提到过:

> 他知道要使用**Int.random**是因为有一种逻辑，Int是整数，而random是随机的英文名，大家可以使用这个方法去尝试

这的确是一种方法，不过我还是建议各位尝试阅读[官方文档](https://swift.org/documentation/)或者借助文档工具来快速查询，例如:

* 在Mac平台下可以选择[Dash](https://kapeli.com/dash)

* 在Windows和Linux平台下可以选择[Zeal](https://zealdocs.org/)

[^Teacher]: Lebus为该系列教程的作者与讲师
