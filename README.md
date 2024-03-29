# 算法笔试题技巧汇总

### 技巧1：
当题目中出现了num=x**n的时候，要立即想到n=math.log(num,x),可以很快速地解决最大边界问题。

### 技巧2：
利用set可以确定数组中是否有重复的元素。结合字符串的 str.count(),可以确定是哪一个字符出现了多次。

### 技巧3：引用自（https://github.com/cy69855522/Shortest-LeetCode-Python-Solutions）
set 中的 in 操作时间复杂度为 O(1)

dict.get 可以设置预设值，避免取到不存在的 key 时报错

遇到关于数组的问题，不妨先想想是否应该先排序

最短路径搜索问题通常使用 bfs

迭代器是缩小 space efficiency 的利器

让数字在一定范围内循环递增常常使用 % 操作

a << b 相当于 a * 2的b次方，a >> b 相当于 a // 2的b次方  


### 数学技巧1

计算三角形面积的两种算法公式：


1.海伦公式：S = sqrt(p*(p-a)*(p-b)*(p-c)), p = (a+b+c)/2， 其中a、b、c是指边长。
                    
2.坐标公式：S = |(x1 · y2 - x2 · y1) + (x2 · y3 - x3 · y2) + (x3 · y1 - x1 · y3)| / 2。x、y指的是坐标。

### 求最大公约数,辗转相除法
   
def fun1(a, b):
    x = a % b
    while (x != 0):
        a = b
        b = x
        x = a % b
    return b

