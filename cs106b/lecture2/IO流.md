open a file;read each line ; close it(行读取)
```cpp
#include<fstream>
ifstream input;
input.open("poem.txt");
string line;
while(getline(input,line)){
cout<<line<<endl;
}
input.close();
```
cpp中读取文件方式：类型＋名称
如果我们要检查是否正确读入
```cpp
if(input.fail())
{
cout<<"womp womp"<<endl;
return 0;
}
```

返回错误自然会进入这个区间
请勿使用文件失败或结束作为循环条件测试；否则可能多打一行
（也可以用获取行失败来替代）
我们还有逐词读取的
```cpp
#include<fstream>
ifstream input;
input.open("poem.txt");
string token;
while(input>>token){
cout<<"here is a word"<< token <<endl;
}
input.close();
```

">>"流提取运算符（从左提取数据放入右侧d）
