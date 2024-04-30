### 一、字符串介绍与特征
**字符串简单说就是能够``存储字符的数组``，用法很多，我们来谈几个**
重点：**字符串总是以`\0`为结尾，不管是什么类型的字符串都是这样**
**字符串的头文件是`iomanip`** 
``#include <iomanip>``

### 二、字符串输入
**在C++中，字符串分为两种类型：`char`和`string`**
**它们的不同点很多，例如：**
**输入输出**
**`char`** 类型输入方式：**直接`cin`**
```cpp
#include <bits/stdc++.h>
using namespace std;

int main ()
{
	char ch;
	cin>>ch;
    return 0;
}
```
但是，这样写程序只会输入一个数，咱们写一个输出试试
```cpp
#include <bits/stdc++.h>
using namespace std;

int main ()
{
	char a;
	cin>>a;
	cout<<a;
    return 0;
}
```
运行结果：

![coding1](https://img-blog.csdnimg.cn/7ad0f17a61f34339a907c9613df87d52.png)
**好，问题来了，怎样才能完整的输出呢**
只要把`a`设大~~亿点~~就可以了
```cpp
#include <bits/stdc++.h>
using namespace std;

int main ()
{
	char a[1000000];
	cin>>a;
	cout<<a;
    return 0;
}
```
运行结果：

![coding2](https://img-blog.csdnimg.cn/15ebc082b9b9450191506686d6eab976.png)
你**也许**会发现，**字符串其实是数组！**

当然，也可以指定输出哪一位
```cpp
#include <bits/stdc++.h>
using namespace std;

int main ()
{
	char a[1000000];
	cin>>a;
	cout<<a[1]; //输出第2位
    return 0;
}
```

**对比`string`，`char`的缺点太多了**
**``string``的输入输出**
**输入方式：直接``cin``**
**输出方式：直接``cout``**

乍一看，好像跟``char``没什么不同的
**BUT，看看这个示例程序，你就知道``string``好在哪里了**
```cpp
#include <bits/stdc++.h>
using namespace std;

int main ()
{
	string a;
	cin>>a;
	cout<<a;
    return 0;
}
```
运行结果：

![coding3](https://img-blog.csdnimg.cn/42f1253e0dd24b798401530b48f899ca.png)
**我们发现：`string`类型允许用户输入很长的字符串，而`char`类型却做不到这一点，这也是为什么大家都喜欢用`string`-----方便！**
***
#### 重点！！！字符串输入都以` `(空格)、`Tab`和`Enter`(回车)为输入结尾
Example：
```cpp
#include <bits/stdc++.h>
using namespace std;

int main ()
{
	string ch;
	cin>>ch;
	cout<<ch;
    return 0;
}
```
![normal](https://img-blog.csdnimg.cn/97a022872d9e4796ab0e834ca5ad5b0d.png)

**但是，用`getline`函数却可以解决空格和`Tab`的问题**

示例代码：
```cpp
#include <bits/stdc++.h>
using namespace std;

int main ()
{
	string ch;
	getline(cin,ch); //注意！getline函数后括号内一定要打括号！而不是 >>
	cout<<ch;
    return 0;
}
```
![example](https://img-blog.csdnimg.cn/1e69123d248d4553a0054eacc189f316.png)

***
### 三、字符串长度
**`char`和`string`都有求长度函数**

1、**`char`类型求长度**
```cpp
#include <bits/stdc++.h>
using namespace std;

int main ()
{
	char a[1000];
	cin>>a;
	cout<<strlen(a); //strlen函数返回字符串的长度
    return 0;
}
```
运行结果：

![coding4](https://img-blog.csdnimg.cn/20a58e74558f49939b437733cfe42925.png)
当然，还有一个厉害的方法求长度...
```cpp
#include <bits/stdc++.h>
using namespace std;

int main ()
{
	char s[1000];
	int len=0;
	cin>>s;
	for(int i=0;s[i]!='\0';i++) {
		len++;
	}
	cout<<len;
    return 0;
}
```
**这个程序的原理是利用字符串的结尾为`\0`，循环求长度**

**2、`string`类型求长度**
```cpp
#include <bits/stdc++.h>
using namespace std;

int main ()
{
	string b;
	cin>>b;
	int len2=b.size(); 
	int len3=b.length();
	cout<<len2<<" "<<len3;
    return 0;
}
```
**`string`类型求长度有两个函数：`.size()` 和 `.length()`**

运行结果：
![coding5](https://img-blog.csdnimg.cn/4d3bd6bdc033401b85a305d88bcfb637.png)
### 四、字符串查找
在`Word`中，有可以查找字符或单词的功能，那么我们能不能用C++实现一个底层呢？
**字符串查找函数：`.find()`**
示例：
```cpp
#include <bits/stdc++.h>
using namespace std;

int main ()
{
	string ch="hello abc";
	cout<<ch.find("hello");
    return 0;
}
```
![find](https://img-blog.csdnimg.cn/c8b5a7248818483aa66530451439470b.png)
**可见，程序在第`1`个位置找到了`hello`**

现在，我们把每个出现的位置都输出出来
```cpp
#include <bits/stdc++.h>
using namespace std;

int main ()
{
	string ch,a;
	int pos=0;
	getline(cin,ch);
	getline(cin,a);
	while(ch.find(a,pos)!=string::npos) {
		pos=ch.find(a,pos);
		cout<<pos<<' ';
		pos++;
	}
	return 0;
}
```
![find1](https://img-blog.csdnimg.cn/ef878aaa81404c0ab7c689414c05e0bc.png)
***
### 五、字符串删除
**`ch.erase(m,n)`** 
``ch``是字符串变量名，此句代码的意思是**删除从`m`开始的第`n`项**
```cpp
#include <bits/stdc++.h>
using namespace std;

int main ()
{
	string ch="Hello ,nice to meet you.";
	cout<<ch.erase(6,1); //删除从第六项开始的一项
    return 0;
}
```
![coding](https://img-blog.csdnimg.cn/f331aa82e1464b1a9e98076e89a75152.png)

***
### 六、熟悉ASCII码
![ASCII](https://img-blog.csdnimg.cn/efdba404fecc4cfbbf5ae7a117b4dd75.png#pic_center)
**规律：每一个大写字母与相应的小写字母相差`32`，且两个相邻的大小写字母的ANSCII码都相差`1`**

### 七、实际应用
**1、洛谷[P5733](https://www.luogu.com.cn/problem/P5733)**

**AC代码：**
```cpp
#include <bits/stdc++.h>
using namespace std;

int main ()
{
    string ch;
    cin>>ch;
    for(int i=0;i<ch.length();i++) {
    	if(ch[i]>='a' && ch[i]<='z') ch[i]-=32; //是小写字母，就转换
	}
	cout<<ch;
    return 0;
}
```
**2、洛谷[P1914](https://www.luogu.com.cn/problem/P1914)**

**AC代码：**
```cpp
#include <bits/stdc++.h>
using namespace std;

int main ()
{
	string ch;
	int n;
	cin>>n>>ch;
	for(int i=0;i<ch.length();i++) {
		if(ch[i]+n>'z') ch[i]=ch[i]+n-26;
		else ch[i]=ch[i]+n;
	}
	cout<<ch;
    return 0;
}
```
**3、洛谷[P1308](https://www.luogu.com.cn/problem/P1308)**
```cpp
#include <bits/stdc++.h>
using namespace std;

int main ()
{
	string ch,src;
	int cnt=0,pos=0,k=0;
	getline(cin,src);
	getline(cin,ch);
	
	for(int i=0;i<ch.length();i++) {
		if(ch[i]>='A'&&ch[i]<='Z') ch[i]+=32;
	}
	
	for(int i=0;i<src.length();i++) {
		if(src[i]>='A'&&src[i]<='Z') src[i]+=32;
	}
	
	ch=" "+ch+" ";
	src=" "+src+" ";
	
	while(ch.find(src,pos)!=string::npos) { //found the word in scope
		pos=ch.find(src,pos);
		cnt++;
		if(cnt==1) k=pos;
		pos++;
	}
	
	if(cnt==0) cout<<-1;
	else cout<<cnt<<" "<<k;
	return 0;
}
```
**UPDATE：本文章最后更新于2020/7/1**
***
