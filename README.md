# JavaScript 笔记

## 基础

1. 当存在多对 script 标签时，其中一对中的代码出错，不会影响其他标签内的代码;

2. script 标签中添加属性：type:“text/javascript” 或 language:"JavaScript";

3. script 标签最好写在 body 标签内的最后;

4. 如果变量赋值null，则该变量的数据类型为object；（var ull = null;）

5. 数值的表示:
    1. 十进制：没有前导0的数值。（1,2,...,9.10,1）
    2. 八进制：有前缀0o或0O的数值，且只用到0-7的八个阿拉伯数字的数值。（0o1,0O2,03,...,07,010）
    3. 十六进制：有前缀0x或0X的数值。（0x1,0X2,...,0xa,...,0xe,0x10）
    4. 二进制：有前缀0b或0B的数值。（0b1,0B10,0b11）

6. 不要用小数比较小数；

7. 不要用NaN判断NaN，使用 isNaN() 方法判断是不是NaN

8. 字符串拼接：使用符号 + ； 判断字符串中字符个数：.length

9. js中的数据类型：
    1. 六种数据类型：字符串类型：string、数字类型：number、布尔类型：boolean、对象类型：object、函数类型：function、全局唯一不同的值：symbol
    2. 三种对象类型：Object、Date、Array；
    3. 两个不包含任何值的数据类型：null、undefined；

10. 类型转换：
    1. 转数字类型：
        1. Number()       严格模式，字符串中必须是数字，否则为 NaN;
        2. parseInt()     整数型；
        3. parseFloat()   小数型；
        4. 布尔转数字：true：1；false：0
        5. NaN:0
        6. undefined:NaN

       <font color=#FF0000>**注意，如果对非String使用parseInt()或parseFloat()，先将其转换为String然后在操作。</font>

    2. 转字符串类型：
        1. .toString()      有意义的字符串转换；
        2. String()         无意义的字符串转换;(Null 或 undefined)

    3. 转布尔类型：Boolean()
        1. 对于数字，除了0和NaN，其余的都是true；
        2. 对于字符串，除了空串，其余的都是true；
        3. null和undefined都是false；

    4. 隐式转换：
        1. 字符串类型：在任意数据类型后添加空串。<font color=#ff0000>原理和String()函数一样。</font>
        2. 数字类型：在任意数据类型前添加加号运算符。<font color=#ff0000>原理和Number()函数一样。</font>
        3. 布尔类型：在任意数据类型前添加两个非运算符。<font color=#ff0000>原理和Boolean()函数一样。</font>

11. 运算符
    1. 算数运算符：加法+ 减法- 乘法* 除法/ 取余% 自加++ 自减-- ；
    2. 赋值运算符：= ；
    3. 复合运算符：+= -= *= /= %= ；
    4. 逻辑运算符：与&& 或|| 非！；
    5. 关系运算符：< > <= >= == === != !== ;
    6. 三元运算符：变量=表达式1?表达式2:表达式3；

       <font color=#ff0000>**注意，++和-- 在参与运算时，符号在前，则先进行自加或者自减在参加运算，否则，先参加运算后进行自加或者自减。</font>

12. 字面量：在声明变量的同时进行赋值；

13. 表达式：值。一个表达式会产生一个值，可以放在任何一个需要值的位置。

14. 语句：行为。程序是由一系列语句组成的，如if语句。 

15. prompt() 方法用于显示可提示用户输入的对话框。

16. 分支语句：
    1. if-else 语句：一般用于做范围判断；
    2. switch-case 语句：一般用于特定值判断；

17. 循环语句：
    1. while语句：先进行条件判断，在执行循环体；
    2. do-while语句：先执行一次循环体，在进行判断；
    3. for语句
    
    <font color=red>*** 注意：break：循环中遇到break关键字时，跳出当前循环；continue：循环中遇到continue关键字时，直接进入条件判断</font>
18. document.write():在页面中输出流写文本（输出流写 HTML）
## 拓展

#### 变量交换：位运算

```javascript
var num1 = 10;
var num2 = 20;
num1 = num1 ^ num2;
num2 = num1 ^ num2;
num1 = num1 ^ num2;
```

#### 数字类型：整数，小数（浮点型：单精度、双精度）

1. int --- 整数
2. float --- 单精度浮点
3. double --- 双精度浮点

#### 斐波那契额数列

**黑马-js基础-day3-06continue练习