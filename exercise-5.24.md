---
sidebarDepth: 3
---

# 5.24练习 - 计算BMI

## 涉及知识点

- 函数

- 返回值

- 控制流

- round函数

- pow函数

- 内部与外部参数

- `_` 占位符

## Code Snippet

```swift
import UIKit

func calcBMI(_ weight: Double, _ height: Double) -> String {
    let bmi = round(weight / pow(height, 2))
    var result = ""
    
    if bmi == 15 || bmi <= 16 {
        result = "严重的体重不足"
    } else if bmi > 16 && bmi <= 18.5 {
        result = "体重过轻"
    } else if bmi > 18.5 && bmi <= 25 {
        result = "体重正常"
    } else if bmi > 25 && bmi <= 30 {
        result = "体重过重"
    } else if bmi > 30 && bmi <= 35 {
        result = "肥胖 I 级别 (中等肥胖)"
    } else if bmi > 35 && bmi <= 40 {
        result = "肥胖 II 级别 (严重肥胖)"
    } else if bmi > 40 {
        result = "肥胖 III 级别 (非常严重肥胖)"
    }
    
    return "BMI: \(bmi) 级别: \(result)"
}

print(calcBMI(52, 1.55))
```

## OutPut

```
BMI: 22.0 级别: 体重正常
```