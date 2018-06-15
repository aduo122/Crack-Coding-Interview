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
