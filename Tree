1.更新树节点
    node的值 0，1，2
    child node 全0 则0， 全1则1，其他则2
    
    求更新某个node之后的tree
    
    思路：
    找到node，整个路径都会改变
    找node：dfs遍历，如果cur找到，则返回路径
    路径从底层依次更新至root
    
2.层数加权求和
    给一个嵌套的数组，计算里面元素的加权求和
    例如，[1, [2, 3], 4] = 1*1 + 2*2 + 3*2 + 4*1 = 15
    
    思路:
    helper(list, depth):
        sum = 0
        if temp is list => helper(temp, depth +1)
        else => sum += temp * depth
    follow up:
        1.树的情况
        2.树的求按列求和？
 3.三角dp
     给你一个三角形，计算从顶部到底部的最短路径和，每一步只能从上一层向临近的下一层移动。

    例如，

       3
      1 2
     2 1 3

    最短路径是3+1+1=5
