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
    
    

    
    
    
    
    
    
    
    
    
    

