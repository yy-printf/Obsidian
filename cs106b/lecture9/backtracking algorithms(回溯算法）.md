```cpp
void diceSumHelper(int dice,int desiredSum,Vector<int>& chosen){
if(dice==0){
if(desiredSum==0){
cout<<chosen<<endl;
}
else {
for(int i=1;i<=6;i++){
chosen.add(i);
diceSumHelper(dice-1,desiredSum-i,chosen);
chosen.removeback;//通过此操作来更换不同位置的数字
}
}
}
}
```
这是通过计算出所有组合的三位数然后通过两个if来进行筛选
backtracking 通常使用三步骤结合 :
==choose C==
==explore the remaining decisions that could follow C==
==Un-choose C==
