# ExamGeneration

由[@Chernobyl](https://github.com/Pryriat)与[@-Gaveu](https://github.com/Gaveu)合力完成的四则运算题目与答案生成程序，可控难度，刷题体验良好。

~~妈妈再也不用担心我的学习~~



## 进展

基本实现了题目生成、计算、问题与答案本地文件存储、对错判断的功能。目前正在测试与误操作方面进行处理打磨。

-修复了漏显第一题的bug。



## 功能

ExamGeneration.exe -n 10 -r 50	//生成十道数值为50以内的题目，题目与答案存放在程序同目录下的Exercises.txt文件与Answers.txt文件中

ExamGeneration.exe -e Exercises.txt -a Answers.txt	//根据Exercises.txt中的题目，验证Answers.txt中的答案，分别列出正确与错误的题目数目和标号





## 调用示例

- 生成10道运算数值最大值为20的题目及计算其答案，并分别存放在程序同目录下的Exercises.txt文件与Answers.txt文件中：

```powershell
.\ExamGeneration.exe -n 10 -r 20
```

​	运行结果：

```powershell
1.  ( 2`9/10 * 8`4/6 ) - 6`1/8 = 19'1/120
2.  5`1/4 + ( 8/9 / 4`1/2 ) = 5'145/324
3.  7`1/3 * ( 7 + 7 ) = 102'2/3
4.  2/9 + ( 6 / 3 ) = 2'2/9
5.  5 * 4`6/8 - 9 = 14'3/4
6.  9`1/5 + ( 1`8/10 / 9 ) = 9'2/5
7.  ( 2`2/7 * 6`1/3 ) * 1`7/9 = 25'139/189
8.  2 + ( 7`5/7 - 7`1/5 ) = 2'18/35
9.  8 / ( 3`3/9 / 7 ) = 16'4/5
10.  1 * ( 2 + 3 ) = 5
Press any key to continue . . .
```



- 验证本地的Exercises.txt题目与Answers.txt中的答案：

```powershell
ExamGeneration.exe -e .\Exercises.txt -a .\Answers.txt
```

​	运行结果：

```powershell
Correct: 10 ( 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 )
Error: 0 ( )
```

