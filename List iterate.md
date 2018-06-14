1.Two char array

    #给两个char array，有一些char为backspace，判断两个array最终是否一致。
    1.stack time O（n），Space O（n）
    2.Space O（1）的方法
    指针，退回操作

    #i loop len(b)
    #compare a[-1-i],b[-1-i+t], unequal -> return false
    #counter for '/b', if counter > 0  -> t += 1

    #list1,list2

    if not list1:
      return list1 == list2
    t = 0
    counter = 0
    pointer = 0
    while pointer < len(list1):
      if counter > 0:
        t += 1
      if list1[-1-i] == '/b':
        counter += 1
        t += 1
      elif counter > 0:
        counter -= 1
      else:
        if len(list2) -1 -i + t < 0 or list1[-1-i] != list2[-1 - i +t]:
          return False
      i += 1
    return True


2.比特翻转  
12345678 -> 78563412  
给一个数，求翻转结果
    思路：
    两两遍历，i += 2每次，不行就加1
    注意：输入是str还是int

3.数字翻倍  
给定一个数组a和b，如果b里有和a一样的数字，把a翻倍，直到没有a。  
求a
    
    思路：brute force，b中的数字存为hashmap -> O（n）
         优化hashmap的方式？ 6，12，24 -> 48 同一组的数做预处理
    先构造hashmap
    dic[k] = -1
    if 2*k in dic:
        dic[k] = dic[2*k]
    else:
        dic[k] = 2*k
    
    可以预处理，也可以边算边处理。（如果-1就计算一遍，如果不是则返回dic[k]）

4.y轴对称  
给一些点，找一条y轴的平行线，点对于y对称。
    
    思路：1.x坐标均值一定是 对称轴x坐标
         2.遍历点，找该点对于对称轴的对称点。如果不存在，返回false；存在，则拿掉该点
         3.考虑corner case：该点在对称轴上
    
5.string求和  
求字符串表示的两个非负整数之和
    
    思路：从尾部扫并求和，记录进位
    注意null


6.有一个元素各不相同的数组，输出它的所有排列

[2,3,5]

输出：
[
  [2,3,5],
  [2,5,3],
  [3,2,5],
  [3,5,2],
  [5,2,3],
  [5,3,2]
]
    
    思路： O（n！），枚举或得结果。
    第一位为k，记录结果，以及helper(list（n去除k）)
    
    follow up：从小到大排列？
    dp，先sort
    helper function：
    从小到大每个数遍历，remove n，得到新的list，做helper（newlist），传递 n + helper 结果
    
7.螺旋矩阵
给你一个整数n，构建一个n*n的螺旋矩阵

    例如，n=4

    1   2   3  4
    12 13  14  5
    11 16  15  6
    10  9   8  7
    
    思路：构造空集，按照index依次填数，注意奇偶

8.整合字符
给你一堆字符串，把同字母异形的字符串放在一起。
例如：
输入：bit, tiger, tib, tbi, bbt, gerti

输出：[bit, tib, tbi], [tiger, gerti], [bbt]

    思路：每个字符构造group，构造disjoint set，再返回子节点

9.打台球  
一个房间四面镜子，
左下角有雷达发射器，
其余三个角各有一个接收器，
给出发射器发射的角度，
哪一个接收器最先接收到信号？

    思路：
    镜面对称构造平面，然后按照tan theta 找到下的袋。再按照穿过的mirror数量找回袋的标号
    注意没有下球的情况？？

10.字符串匹配  
first = abcdefgacde
second = ade
返回acde

    思路：
    brute force：遍历first，最短的返回。
    先选出第一个成立的list，pop出第一个字母，在后面找到相应的字母，再剔除不再second里的字母
    最后返回最短list

11. 括号匹配
返回括号是否有效

    思路：
    遍历原list，pop
    用stack记录，如果与pop匹配，下一个
    不匹配，如果左，放进去，如果右，报错
    最后stack为空，返回true

12. 一群人买票，知道自己位置以及队中每个人买票的数量。
每次每人买一张票，多的从新排队。求自己卖完时卖了多少票？

queue = {3,2,1,1}
pos = 2

ans = 6

    思路：
    brute force：每次pop(0),非0则append，O(ans)
    优化：
    pos前面最多买queue[pos]+1张票，之后最多买queue[pos]-1张票，scan一遍O(n)
    follow up：
    每次买K张？

13.输入一个矩阵
{1,2,3
 4,5,6
 7,8,9}
 
 target = 16
 求不超过target的最大子矩阵(难题)
 返回16
 {2，3
  5，6}
  
    思路：
    brute force：长枚举遍历，宽枚举遍历，m^2 * n^2
    优化：枚举长边

14.切割一个list，最多切成多少个，每个子list排序后整个list也排序了？
{1,3,7,5,3,1}

    思路：对于n，前面最大值要小于后面最小值，则可以切

15.给一堆矩形，求是否重合

    思路：左下，右上，看是否有重合遍历O（n^2）
    时间复杂度？优化？
    
    follow up：给一条线，看是否堵路？
    重合矩形最总成disjoint set，看最下端与最上端，是否堵路



16.每次每人买一张票，多的从新排队。求自己卖完时卖了多少票？

    思路：
    brute force， 买完再入队，O(res)
    优化：pos前，最多list[pos]
         pos后，最多list[pos]-1
         然后再sum
    

17.给n个点，问能组成几个正方形

    思路：
    iterate四个点，check 正方形 -> n^4
    优化1: 三个点，推理出第四个点 -> n^3
    优化2: 两个点，对角线，推理出剩下两个点 -> n^2
    
18 字符串匹配
给两个字符串，数字代表隐去的字母个数，求两个字符串是否相等  
如b4t2，b6r 返回True
    
    沟通：b12t 能否代表 b，1，2，t
    思路：同时遍历，相同则继续，都是数字则数字相减，数字大的保持不变
         数字与字母则数字减1，数字若不为零，指针不变
         最后同时指针指向tail
    follow up：
