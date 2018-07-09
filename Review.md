套路总结
=====
   sort的一些方式：
   ----
    topK：bucket sort
         T:O(n) S:O(n)
    slidewindow：deque
    
    heap:
        T:O(n) S: O(n) for build 
        T:O(logn) S:O(n) for insert and rearrange
    
   丑数，构造因数组合
   ----
    下一丑数 = min（因数 * 之前乘过的最小丑数的下一个丑数）
    被选中的因数每次更新丑数
   
   list 遍历技巧
   ----  
    使用stack:如果当前符合某条件则操作stack，最终stack为空或者满足其他条件
              比如括号，计算符号等题，本质上是dfs
              
    two pointer: 左边向右， 右边向左
   
   中位数
   ----
    中位数 <=> 找到第len/2小的数
    
   Sampling
   ----
    reservoir sampling 特点：不知道长度，遍历一遍后，每个元素取到机会均等
    方法：对于kth，替换的概率为（1/k）,之后不变的概率： 1/k * k/k+1 * k+1/k+2 * ... * n-1/n = 1/n 很巧妙
   
   图遍历技巧
   ----
    前状态
    操作
    后状态
    
    从两端遍历，n^2 -> 1/4 * n^2
    
    典型例题：
    1.W/B格子问题，不能到边界的W格子数量 
      思路：从边界开始遍历，设置一个visited防止环
      
    2.背包问题
      思路：每一个元素考虑要不要
      优化：可以先sort一下，大数优先
   
   拓扑排序
   ----
    入度出度计数，每次pop入度为0的，如果剩下还有东西则有环
   
   树结构
   ----
    in order 左上右
    pre order 上左右
    post order 左右上
    recursive, iterative法
    
    线段树：二分左右，子树为前后两段各自的和，适用于求和问题
   
