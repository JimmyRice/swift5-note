---
sidebarDepth: 3
---

# 4.12课时 - IBOutlet和IBAction

## 知识点
### 操作
通过 ==按住Mac的control==按键并且==拖拽==到代码视图中可以创建**IBOutlet**与**IBAction**

### 组件
1. **IBOutlet**: IBOutlet是一个对象属性，建立连接后可以通过代码对控件属性进行修改

2. **IBAction**: IBAction可以允许用户与控件交互，用户操作后出发响应或者逻辑

## 其他
1. 命名规则(面向新手): 驼峰法(小驼峰)命名法指除了第一个单词，其他单词开头都大写；有小驼峰就会有大驼峰，大驼峰是所有单词开头都大写，常用于代码文件的命名

## 注意
1. **IBOutlet**中不可以直接修改变量或者常量的名字，如果需要修改，先断开与控件的连接再重新连接

2. ==额外知识==: 根据官方文档介绍，IBOutlet将会占用内存，请避免过多使用