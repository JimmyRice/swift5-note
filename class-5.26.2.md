---
sidebarDepth: 3
---

# 5.26.2知识点部分 - 外部参数与内部参数

## 知识点

使用以下方式表达这个函数的参数有分为外部参数和内部参数

```swift
func 函数名(外部参数 内部参数) {
    代码
}
```

外部参数的名字在函数块外调用，内部参数在函数块内调用

例如

```swift
func saySomeThing(InputSomeWord text: String) {
    print(text)
}

saySomeThing(InputSomeWord: "Hello")

```

输出

```
Hello
```

在我们调用的时候用的是外部参数 `InputSomeWord`，在函数块内部的时候我们仍然使用 `text`

这节课还讲到了一个符号 `_` 下划线

下划线实际上是一个占位符，用在函数参数里面即告诉 Swift 这个参数没有名字

```swift
func saySomeThing(_ text: String) {
    print(text)
}

saySomeThing("Hello")
```

```
Hello
```