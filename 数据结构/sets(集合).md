---
data: 2025-02-05
---

不储存重复单元的集合体
# 操作
支持的操作不多，但效率高
- add 
- remove 
- search(contains)

# 特点
集合是无序的，没有遍历的方法

# 类型
- set   比较快，元素以既定的顺序排列
- hashset   非常快，元素无序排列

# 使用方法

![[c19cfc5d874bea263c67ca01675a381e.jpg]]![[tempFileForShare_20250207-111230.jpg]]
# 遍历方法
```
for(type name : collection){
statements;
}
```
不能使用 int i 的索引操作        