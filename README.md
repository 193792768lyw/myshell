# myshell

## 简介

用C语言实现的一个简易的shell，能够接受用户输入的命令并执行操作。
程序运行后，会模拟shell使用getcwd()函数显示当前的路径，等待用户输入命令。程序逐次读取用户输入的指令后，将指令按空格拆分成多个字符串命令，然后判断该命令的类型。
* 若为exit，则调用自定义的exit函数，向该程序进程发送terminal信号结束该进程
* 若为help，则调用自定义的help函数展示该shell的信息
* 若为cd，则判断参数，调用chdir()函数修改当前的路径，并返回相应的结果。若修改成功，则使用getcwd()函数更新当前路径
* 若为其他命令，则调用自定义的函数去判断参数并执行

-------

## 功能
[x] 显示当前工作路径
[x] exit函数
[ ] help函数
[x] cd命令
[ ] 执行外部命令，判断无效命令
[ ] 实现管道
