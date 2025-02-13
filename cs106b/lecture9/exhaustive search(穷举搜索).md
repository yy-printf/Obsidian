```cpp
#include<iostream>
#include<string>
using namespace std;
void printAllBinaryHelper(int digits, string output) {
	if (digits == 0) {
		cout << output << endl;
	}
	else {
		printAllBinaryHelper(digits - 1, output + '0');
		cout << endl;
		printAllBinaryHelper(digits - 1, output + '1');
		cout << endl;
	}
}
int main()
{
	int digit;
	cin >> digit;
		string str = "";
		printAllBinaryHelper(digit,str);
	return 0;
}

```
利用递归搜索一切可能的值
