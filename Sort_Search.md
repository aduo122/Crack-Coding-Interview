1.输入Vote List， 格式（time，name），给定时间t  
1.求t之前票数最高的人  

    sum保存票数max，返回  
2.求t之前topk  

    先遍历到t，求sum，再heapmin存sum，求topk的sum  
3.输入candidate的list， 求当candidate是top n的最后时间
 
2.长度n+1的数组，包含1-n，有且仅有一个数至少出现两次  
求该数字

    思路：桶排序，构造1 - n list，每个index存相应的数字，返回第一个重复的index
    
    注意：如果只重复一次，求和最好
    follow up：空间O（n）
    改变值：正负
    不改变值：循环遍历
    
3.你要把一个字符串完整输出到宽为w，高位h的屏幕上。  
你可以通过getHeight(intfontSize)的到一个字号的高度；  
通过getWidth(char c, int fontSize)得到一个字符对应字号的宽度。  
请问能使用的最大字号是多少？

    思路：字符串长度n，字符号长度m  
    对于字号k，可以依次写入字符，如果排得下则进行下一字号 -》 binary search
    宽度w brute force则需要m*n，针对字号二分则有nlogm

4.字符串比对  
有两个字符串  
其中一个比另一个多一个字母  
其余字母出现的顺序相同  
求这个字母

    思路：二分法，判断list1[:i] == list2[:i]
