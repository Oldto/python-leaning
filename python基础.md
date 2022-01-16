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

## 程序的组织结构
任何程序都可以由顺序结构、判断结构、循环结构构成。

## 对象的布尔值
在python中所有的对象都有一个布尔值，获取对象布尔值，使用函数bool()

对象的布尔值为False的
- False
- None
- 空字符
- 空列表
- 空元素
- 空字典
- 空集合
- 0
```
print(bool(False)) #False
print(bool('')) #空字符串
print(bool(""))
print(bool(0)) #0
print(bool([])) #空列表
print(bool(list()))
print(bool({})) #空字典
print(bool(dict()))
print(bool(())) #空元组
print(bool(tuple()))
print(bool(set())) #空集合
```
其他对象的布尔值为True

## 判断结构
#### 单分支结构
![image](https://user-images.githubusercontent.com/71583369/149623041-aa23b573-8abe-4c6a-8abf-542ecac0ff05.png)
```
if表达式:
 条件执行体
```
代码
```
money=2000
wm=int(input('请输入取款金额：'))
if wm<=money:
    money-=wm
    print(money)
```
#### 双分支结构
```
# 判断输入的数字奇偶性
num = int(input('请输入整数：'))

#判断
if num%2==0:
    print(num,'是偶数')
else:
    print(num,'是奇数')
```
#### 多分枝结构
![image](https://user-images.githubusercontent.com/71583369/149623814-6017fc99-c25d-497e-b6ff-8d30cc59d5ec.png)
```
# 成绩判断
count = int(input('请输入成绩：'))
if 90<=count<=100:
    print('A级')
elif 80<=count<=89:
    print('B级')
elif 70<=count<=79:
    print('C级')
elif 60<=count<=69:
    print('D级')
elif 0<count<=59:
    print('E级')
else:
    print('输入错误')
```
#### 嵌套if
![image](https://user-images.githubusercontent.com/71583369/149625905-5a04662f-a8f9-42db-8c35-95877312da07.png)
```
# 购买5000产品打7折 4000产品打8折 3000产品打9折 低于3000打9.5折
answer=str(input('要买产品嘛？y/n'))
money=float(input('价格'))
if answer=='y':
    if money>5000:
        print('打7折',money*0.7)
    elif 4000<=money<=4999:
        print('打8折',money*0.8)
    elif 3000<=money<=3999:
        print('打9折',money*0.9)
    else:
        print('打9.5折',money*0.95)

else:
    print('滚蛋')
```
#### 条件表达式
![image](https://user-images.githubusercontent.com/71583369/149627164-10bd2422-10ac-4565-b411-5c248e58b422.png)
```
# 比较大小
num_a=int(input('请输入第一个整数'))
num_b=int(input('请输入第二个整数'))
print(str(num_a)+'大于'+str(num_b) if num_a>num_b else str(num_a)+'小于'+str(num_b))
```
## pass语句
![image](https://user-images.githubusercontent.com/71583369/149627837-2543f1d5-4be8-4421-9f59-e092fff7f7a7.png)

## range()函数
![image](https://user-images.githubusercontent.com/71583369/149643960-e660d403-9e42-431e-a019-d20477ab0597.png)
```
# 不指定起始位,默认从0开始，不包括0，步节为1
print(list(range(10)))

# 指定起始位和结束位
print(list(range(1,10)))

# 指定起始位和结束位，指定步节
print(list(range(1,10,2)))
```
相同步节在内存中存储的大小是一样的。

## 循环结构
![image](https://user-images.githubusercontent.com/71583369/149644794-90dcc45e-8cb6-4e1b-9a81-227abd621547.png)
```
# 求出0到4的累加值
a=0
count=0
while a<5:
    count+=a
    a+=1
print('和为',count)
```
求1到100之间偶数之和
```
a=0
count=0
while a<=100:
    count+=a
    a+=2
print(count)

a=1
sum=0
while a<=100:
    if a%2==0:
        sum+=a
    a+=1
print('和为',sum)
```
## for in 循环
![image](https://user-images.githubusercontent.com/71583369/149646076-75a2fec5-d66e-4eb9-8160-e29151ddb2e0.png)
```
 # 1-100之间的偶数和，使用for_in
sum=0
for i in range(1,101):
    if i%2==0:
        sum+=i
print('和',sum)

# 遍历字符串
for a in 'python':
    print(a)
# 不定义变量使用下划线
for _ in range(5):
    print('人生苦短，我用python')
```
## 流程控制break
![image](https://user-images.githubusercontent.com/71583369/149646914-63c1faef-3dd6-47a9-8257-e5ccd1746b25.png)
```
'''for i in range(3):
    pwd=input('请输入密码')
    if pwd=='888':
        print('输入正确')
        break
    else:
        print('输入不正确')'''

a=0
while a<3:
    pwd=input('请输入密码')
    if pwd=='888':
        print('输入正确')
        break
    else:
        print('输入不正确')
    a+=1
```














