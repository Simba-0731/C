# C语言常见概念

## main函数

每个 C 语⾔程序不管有多少⾏代码，都是从 main 函数开始执⾏的， main 函数是程序的⼊⼝，main 函数也被叫做：主函数。 main 前⾯的 int 表⽰ main 函数执⾏结束的时候返回⼀个整型类型的值。所以在 main 函数的最后写 return 0; 正好前后呼应。

• main函数是程序的⼊⼝

• main函数有且仅有⼀个

• 即使⼀个项⽬中有多个.c⽂件，但是只能有⼀个main函数（因为程序的⼊⼝只能有⼀个）

main()   主函数

## printf和库函数 

printf() 实现在屏幕上的信息打印

printf 是⼀个库函数，它的功能是在标准输出设备（⼀般指屏幕）上进⾏信息的打印。上⾯的代码是使⽤ printf 函数打印字符串。只要把想要打印的⼀串字符放在双引号中并传递给printf函数就可以打印。

在使用库函数的时候，是需要包含头文件的，比如：printf函数需要包含的就是stdio.h这个头文件，具体的方法就是：
```
#include <stdio.h>
```
%d - 打印整数

%c - 打印字符

%f - 打印小数 （默认小数点后会打印6位小数）

%s - 打印字符串

\0 是字符串结束的标志

## 转义字符

\?:在书写连续多个问号时使用，防止他们被解析成三字字母，在新的编译器上没法验证了。

\':用于表示字符常量'

\":用于表示一个字符串内容的双引号

\\:用于表示一个反斜杠，防止它被解释为一个转移字符

\a:警报，这会使得终端发出警报声或出现闪烁，或者两者同时发⽣

\b:退格键，光标回退⼀个字符，但不删除字符

\f:换⻚符，光标移到下⼀⻚。在现代系统上，这已经反映不出来了，⾏为改成类似于 \v

\n:换行符

\r:回⻋符，光标移到同⼀⾏的开头

\t:制表符，光标移到下⼀个⽔平制表位，通常是下⼀个4/8的倍数

\v:垂直分隔符，光标移到下⼀个垂直制表位，通常是下⼀⾏的同⼀列

下⾯2种转义字符可以理解为：字符的8进制或者16进制表⽰形式

• \ddd ：d d d表⽰1~3个⼋进制的数字。 如： \130 表⽰字符X

• \xdd ：d d表⽰2个⼗六进制数字。 如： \x30 表⽰字符0

\0 ：null 字符，代表没有内容， \0 就是 \ddd 这类转义字符的⼀种，⽤于字符串的结束标志，其
ASCII码值是
