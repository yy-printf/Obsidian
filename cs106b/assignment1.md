1:对程序崩溃的描述：无法点击任何按键，电脑一直处于加载状态，过一段时间自动退出
2```
```
string onlyConnectize(string phrase) {
    /* TODO: The next few lines just exist to make sure you don't get compiler warning messages
     * when this function isn't implemented. Delete these lines, then implement this function.
     */
    for(int i=0;i<phrase.size();i++)
    {
        if((int)phrase[i]>=97&&(int)phrase[i]<=122)phrase[i]-=32;
    };//全都化为大写
    string result;
    for(char ch :phrase)
    {
        if(ch=='C'||ch=='D'||ch=='F'||ch=='G'||ch=='H'||ch=='J'||ch=='K'||ch=='L'||ch=='M'||ch=='N'||ch=='P'||ch=='Q'||ch=='R'||ch=='S'||ch=='T'||ch=='V'||ch=='W'||ch=='X'||ch=='Y'||ch=='Z')
            result+=ch;
    }
    return result;
    }
    ```
```
将辅音字母提取出来，并大写转换，
几个要点
- for（）结构
- 字符串加减