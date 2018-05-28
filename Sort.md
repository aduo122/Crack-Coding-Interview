1.输入Vote List， 格式（time，name），给定时间t
    1.求t之前票数最高的人
      sum保存票数max，返回
    2.求t之前topk
      先遍历到t，求sum，再heapmin存sum，求topk的sum
    3.输入candidate的list， 求当candidate是top n的最后时间
 
2.长度n+1的数组，包含1-n，有且仅有一个数至少出现两次，求该数字
    思路：桶排序，构造1 - n list，每个index存相应的数字，返回第一个重复的index
    
    注意：如果只重复一次，求和最好
    follow up：空间O（n）
    改变值：正负
    不改变值：循环遍历
