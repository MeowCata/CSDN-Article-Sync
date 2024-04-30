**~~这是题解，~~ 这是练习**

### 代码实现
**定义输入不解释**
```cpp
#include <bits/stdc++.h>
using namespace std;
int cube[105][105]; //矩阵
int main ()
{
	int n; //矩阵边长
	scanf("%d",&n);
	for(int i=1;i<=n;i++) {
		for(int j=1;j<=n;j++) {
			cin>>cube[i][j]; //二层循环输入
		}
	}
    return 0;
}
```
#### **顺时针旋转`90°`**
```cpp
for(int i=1;i<=n;i++) {
	for(int j=n;j>=1;j--) {
		cout<<cube[j][i]<<' ';
	}
	cout<<'\n';
}
```
#### **顺时针（逆时针）旋转`180°`**
```cpp
for(int i=n;i>=1;i--) {
	for(int j=n;j>=1;j--) {
		cout<<cube[i][j]<<' ';
	}
	cout<<'\n';
}
```
**还有一种思路：旋转`180`度就等于旋转两次`90`度，所以可以循环两次旋转`90`度的代码**

**额，这种思路太 ~~笨~~ 不方便了，所以不建议使用**

#### **顺时针旋转`270°`**
```cpp
for(int i=n;i>=1;i--) {
	for(int j=1;j<=n;j++) {
		cout<<cube[j][i]<<' ';
	}
	cout<<'\n';
}
```
#### **水平翻转**
```cpp
for(int i=1;i<=n;i++) {
	for(int j=n;j>=1;j--) {
		cout<<cube[i][j]<<' ';
	}
	cout<<'\n';
}
```
#### 综合代码如下
```cpp
#include <bits/stdc++.h>
using namespace std;
int cube[105][105];
int main ()
{
	int n;
	cin>>n;
	for(int i=1;i<=n;i++) {
		for(int j=1;j<=n;j++) {
			cin>>cube[i][j];
		}
	}
	//turn 90 
	cout<<'\n';
	for(int i=1;i<=n;i++) {
		for(int j=n;j>=1;j--) {
			cout<<cube[j][i]<<' ';
		}
		cout<<'\n';
	}
	//flip
	cout<<'\n';
	for(int i=1;i<=n;i++) {
		for(int j=n;j>=1;j--) {
			cout<<cube[i][j]<<' ';
		}
		cout<<'\n';
	}
	//turn 270
	cout<<'\n';
	for(int i=n;i>=1;i--) {
		for(int j=1;j<=n;j++) {
			cout<<cube[j][i]<<' ';
		}
		cout<<'\n';
	}
	//turn 180
	cout<<'\n';
	for(int i=n;i>=1;i--) {
		for(int j=n;j>=1;j--) {
			cout<<cube[i][j]<<' ';
		}
		cout<<'\n';
	}
	return false;
}
```
#### **运行结果：**
![test](https://img-blog.csdnimg.cn/bb3923c4e9b3453dadf65b7e63b80d15.png)
**输出顺序：`顺时针旋转 90° → 水平翻转 → 顺时针旋转270° → 顺时针旋转180°`**
***
