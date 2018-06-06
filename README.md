# cpp-primer

```

使用 cin 时会将换行符 '\n' 留在输入缓冲区，而 cin 本身在从输入缓冲区中读取内容的时候，会忽略空白字符(如空格，换行符等，使用 noskipws 标志可以改变这种行为)

http://www.cnblogs.com/zhangziqiu/archive/2011/03/30/ComputerCode.html

多行字符串字面值
std::cout << "xxx"
"yyy"

有的前缀/有的后缀 -> 指定字面值类型 如: L'a' u8"hi" 42ULL

声明：使得名字为程序所知，定义：创建与名字关联的实体[内存分配]，初始化：具体值
extern int i; // 声明而非定义
int j;        // 声明并定义为默认值
变量能且只能被定义一次，但可以多次声明

引用(reference)
int ival = 1024;
int &refVal = ival; // refVal 是 ival 另一个名字

int* p1;int* p2; == int *p1, *p2

double dval = 3.14;
const int &ri = dval; // 此时 ri 绑定的是 dval 有编译器所生成的临时量[转int], 而非 dval

引用绑定到类型不同的临时量会报错
     代码       |    名称      | 说明
-------------- | ------------ | ------------
int *const xxx | 常量指针/top-level const/顶层const | 指向不可变，所指对象是否可变看情况 constexpr int *xxx
const int *xxx | 指向常量的指针/low-level const/底层const | 可指常量也可非常量，不能通过该指针改变所指对象的值。但可以通过其他途径改变
const int &xxx | 常量引用      | 可指常量也可指非常量，不能通过该引用改变所指对象的值。但该对象的值可以通过其他途径改变


```
