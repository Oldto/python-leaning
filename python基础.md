# python
在python中一切皆为对象
## 输出函数print
```
# 输出数字，不需要加引号
print(1)
# 输出字符串
print('hello world')
# 输出运算符
print(4+1)
# 将内容输出到文件中
fp = open('D:/PycharmProjects/vippython/test.txt','a+') #打开这个文件，如果不存在则创建文件，并且追加内容
print('hello world',file=fp)
fp.close()
# 不换行进行输出
print('hello','world')
```
## 转义字符与原字符
```
转义字符：\
换行：\n
print('hello\nworld')
返回：\r 输出的结果为world，会将hello吃掉
print('hello\rworld')
水平制表符：\t 输出的结果为hello   world,水平制表符会占4个位置，空的地方用空格表示
print('hello\tworld')
退格：\b 会向后退一个字符，吃掉o，输出hellworld
print('hello\bworld')
原字符：就是不希望转义字符生效，需要在字符串前面加上r或R
print(r'hello\nworld')
注意事项：在使用原字符时，字符串后面不能加\,\\是可以的
报错：print(r'hello\nworld\')
不报错：print(r'hello\nworld\\')
```
## 二进制与字符编码
```
二进制由01组成，而一组01有4中变换，如00、01、10、11，两组加起来是8种变换，也就是
8bit=1byte
1024byte=1kb
1024kb=1MB
1024MB=1GB
1024GB=1T
8个位置也就构成了256种变换，构造出ascii码表，其中有128种为国内使用，构造出不同的字符另外128种为国外使用
```
## python中的标识符和保留字
```
保留字：起名字时不能使用
import keyword
print(keyword.kwlist)

['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 
'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 
'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']

标识符：需要我们命名的都叫标识符
规则：
字母、数字、下划线
不能已字母开头
不能用保留字
严格区分大小写
```
## 变量
```
name='无敌风火轮'
print(name)

变量由3部分组成
- 标识 对象所存储的内存地址，使用id()获取
- 类型 对象所存储的数据类型，使用type()获取
1. 整数型--int(98)
2. 浮点型--float(9.8)
3. 布尔型--bool(ture,flase)
4. 字符型--str('人生苦短，我用python')
- 值 对象所存储的数据，可用print()打印
print('标识',id(name))
print('类型',type(name))
print('值',name)
当变量多次赋值时，会指向新的变量，而之前的会变为内存垃圾。
```
## 数字类型
默认是十进制标识，不同进制的表达方式
- 二进制--0b开头`print(0b11110)`
- 八进制--0o开头`print(0o155)`
- 十六进制--0x开头`print(0x1ef)`

![image](https://user-images.githubusercontent.com/71583369/149529645-83b565c9-45cd-4915-b885-c268ba29fca5.png)

## 浮点类型
由整数部分和小数部分组成，浮点类型在进行计算时会出现计算结果不准确的情况，这是因为计算机只识别二进制的导致。

## 布尔类型
用作判断真假，True（1）为真，Flase（0）为假

## 字符串类型
可以使用单引号、双引号、三引号，区别是单引号和双引号只能在一行使用，三引号可以多行使用
```
str1='人生苦短，我用python'
str2="人生苦短，我用python"
str3="""人生苦短，
我用python"""

str4='''人生苦短，
我用python'''
```
## 数据类型转换
不同的数据类型进行拼接时需要用到数据类型转换

![image](https://user-images.githubusercontent.com/71583369/149612761-33803a18-7739-478b-8ab5-4fe556936f02.png)

## 输入函数input()

![image](https://user-images.githubusercontent.com/71583369/149614633-e4bd5e95-a2ce-4dd1-8e4a-991493ede8fc.png)

```
mq=input('大王想要什么那')
print(mq)

# 加法运算
a=input('输入第一个数：')
b=input('输入第二个数：')
print(int(a)+int(b))
```
## 算数运算符
![image](https://user-images.githubusercontent.com/71583369/149615253-cba5971c-b7ec-4e61-a7d3-926e528831f3.png)

## 赋值运算符
![image](https://user-images.githubusercontent.com/71583369/149615329-d8b580f3-a09b-42dd-a8fc-7aa468d8bdc3.png)

解包赋值可进行数据交换
```
a,b=10,20
print(a,b)
#交换
a,b=b,a
print(a,b)
```
## 比较运算符
![image](https://user-images.githubusercontent.com/71583369/149617679-b5c628e5-99ca-41c4-8141-4fd11eda4b66.png)

## 布尔运算符
![image](https://user-images.githubusercontent.com/71583369/149617699-cfd4ce6a-745e-4f3f-85b8-efea64db80ea.png)

not取反   in 在里面  not in 不在里面
```
s='helloworld'
print('h'in s)
print('k' in s)
print('h' not in s)
print('k' not in s)
```
## 位运算符
![image](https://user-images.githubusercontent.com/71583369/149618616-8f1420c1-4ff2-4705-b7d2-dd0bc2aa1210.png)

```
位移
print(4 << 1) #向左移1位 相当于成2
print(4 >> 1) #向右移1位 相当于除2
```
## 运算符的优先级
![image](https://user-images.githubusercontent.com/71583369/149619041-84007da8-62f7-4a25-8f6b-87e0b6c341fd.png)















