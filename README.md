# cpp-primer

```

http://www.cnblogs.com/zhangziqiu/archive/2011/03/30/ComputerCode.html

====================

多行字符串字面值
std::cout << "xxx"
"yyy"

有的前缀/有的后缀 -> 指定字面值类型 如: L'a' u8"hi" 42ULL

====================

声明：使得名字为程序所知，定义：创建与名字关联的实体[内存分配]，初始化：具体值
extern int i; // 声明而非定义
int j;        // 声明并定义为默认值,未初始化
变量能且只能被定义一次，但可以多次声明

====================

引用(reference)
int ival = 1024;
int &refVal = ival; // refVal 是 ival 另一个名字

double dval = 3.14;
const int &ri = dval; // 此时 ri 绑定的是 dval 有编译器所生成的临时量[转int], 而非 dval
引用绑定到类型不同的临时量会报错


指针
int* p1;int* p2; == int *p1, *p2


     代码       |    名称      | 说明
-------------- | ------------ | ------------
int *const xxx | 常量指针 | 指向不可变，所指对象是否可变看情况 constexpr int *xxx
const int *xxx | 指向常量的指针 | 可指常量也可非常量，不能通过该指针改变所指对象的值。但可以通过其他途径改变
const int &xxx | 常量引用      | 可指常量也可指非常量，不能通过该引用改变所指对象的值。但该对象的值可以通过其他途径改变


https://blog.csdn.net/yusiguyuan/article/details/38454825
top-level const/顶层const: 指针本身是一个常量. 更一般情况下, 可以表示任意对象是一个常量
low-level const/底层const: 指针所指的对象是一个常量, 所指向谁是可更改的
const int *const xxx: 右侧顶层const, 左侧底层const, 这个指针同时拥有顶层与底层const性质。拷入拷出时要考虑对方有同样的底层const与数据类型限制。
一般允许非常量向常量转，反之不行。

https://www.cnblogs.com/alephsoul-alephsoul/archive/2012/10/10/2719192.html

====================

```
