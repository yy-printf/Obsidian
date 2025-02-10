```cpp
#include<iostream>
#include<string>
using namespace std;
int evaluateHelper(string exp, int& index)//通过地址传递时刻改变index
{
	if (exp[index] <= '9' && exp[index] >= '0')//isdigit
	{
		return exp[index++] - '0';//读到数字返回数字
	}
	else if (exp[index] == '(')//左括号则向前进一位
	{
		index++;
		int left= evaluateHelper(exp, index);
		char opr = exp[index];
		index++;//读操作符右边的数字
		int right = evaluateHelper(exp, index);
		index++;
		return  left + right;
	}
}
int main()
{
	int index = 0;
	string a = "7";
	string b = "(4+2)";
	string c = "((4+1)+(1+9))";
	cout << a << "=" << evaluateHelper(a, index)<<endl;
	index = 0;
	cout << b << "=" << evaluateHelper(b, index)<<endl;
	index = 0;
	cout << c << "=" << evaluateHelper(c, index)<<endl;
}

```
递归解决计算，将大问题拆分为小问题，逐步解决，在解决小问题时要注意与大问题间的连接关系