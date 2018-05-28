1.每种蛋糕（weight，value），无限个，最多拿走重量x，求能拿走的最大价值？

    思路：
      背包问题，使用性价比剪枝
      n个蛋糕，每次n种情况，
        如果wn > w: 跳过
        else：
            helper（x-wn，value）
            dic 更新
        优化：性价比剪枝，
        for n中，每次选择的顺序：性价比高的先做helper操作

2.string 组成

    判断非空字符串能否由dic中的单词组成
    sortsortsort 和 [sort,boy], true
    jump 和[jum,mp] false
    
    思路：
    遍历list，word in dic -> if helper([i:]) return True
    优化：使用trie树构造dic

3.字母编码

    a-z编码1-26
    求给定数字的解码可能数
    
    思路：
    helper：
    返回一数编码 或两数编码结果 + helper（剩下数量）
    
    优化：
    当前结果由前两个结果决定，每次memo存两个，Space O（2）节省空间，时间相同

4.排任务

    给你一个任务列表，不同类型的任务由不同的大写字母表示，每个任务的完成时间都是1。
    两个相同类型的任务在安排的时候至少要间隔n个时间。
    请问任务完成的最短时间是多少？

    例如，
    任务系列：AABCCCDDD；n=3
    一个可行的最短时间安排是：CDABCDA_CD
    时间是：10
    
