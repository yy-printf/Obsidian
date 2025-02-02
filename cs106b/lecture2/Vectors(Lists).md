vector就相当于一个可伸缩的数组，vector（数据类型）自动分配内存
```cpp
Vector<int> nums {42,17,21,66,-1};

Vector<string> names;
name.add("Stu");
name.add("Marty");
name.insert(0,"Ed");
```
可以通过索引的方式来找其中的数据
![[36f993787eb161868f12806fcefece2f.jpg]]
上面是一些vector的基本用法

```cpp
for(string name :names){
 cout << name << endl;
}
```
用于将names中每个元素赋给name，然后打印
- 嵌套语句：```
vector<int> a {1};
vector<int> b {2,3};
vector<int> c {4,5,6};
vector<vector<int>> d ;
d.add(a);
d.add(b);
d.add(c);
cout << vv <<endl;//{{1},{2,3},{4,5,6}}
cout << vv[1][1] <<endl;//3
```
w