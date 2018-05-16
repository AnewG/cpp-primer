# cpp-primer

```

使用 cin 时会将换行符 '\n' 留在输入缓冲区，而 cin 本身在从输入缓冲区中读取内容的时候，会忽略空白字符(如空格，换行符等，使用 noskipws 标志可以改变这种行为)

http://www.cnblogs.com/zhangziqiu/archive/2011/03/30/ComputerCode.html

多行字符串字面值
std::cout << "xxx"
"yyy"

有的前缀/有的后缀 -> 指定字面值类型 如: L'a' u8"hi" 42ULL

```
