套路总结
=====
   sort的一些方式：
   ----
    topK：bucket sort
    slidewindow：deque
    
   丑数，构造因数组合
   ----
    下一丑数 = min（因数 * 之前乘过的最小丑数的下一个丑数）
    被选中的因数每次更新丑数
   
   list 遍历技巧
   ----  
    使用stack与list遍历配合，如果当前符合某条件则操作stack，最终stack为空或者满足其他条件
    比如括号，计算符号等题，本质上是dfs
