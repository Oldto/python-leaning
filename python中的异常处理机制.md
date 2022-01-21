# 被动掉坑的处理机制
![image](https://user-images.githubusercontent.com/71583369/150482913-8cd43efb-1492-4cd6-afe0-34cb9dde80d4.png)

![image](https://user-images.githubusercontent.com/71583369/150483513-bd681d0b-5cbc-42e6-bb44-c57549ff95b5.png)
```
# 被动掉坑的异常处理
try:
    a = int(input('请输入第一个整数：'))
    b = int(input('请输入第二个整数：'))
    c = a / b
    print(c)
except ZeroDivisionError:
    print('不可以输入0')
    print('over')
except ValueError:
    print('请输入正确的整数')
    print('over')
```
