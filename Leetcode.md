LinkedList 
====
  Sum problems
  ----
    2.Add Two Numbers
      method 1 add number accordingly, add the additional number at last
    
    445.Add Two Numbers II
      method 1 get int numbers from the linkedlist first, then get the sum and turn into linkedlist as result
      method 2 iterate through the linkedlist, turn into stack, do the reverse iterate from stack

    43. Multiply Strings
      method 1 make function multiply, function add, iterate the small number to sum up the result.
  Use Headers
  ----
    19. Remove Nth Node From End of List
      pre,cur,front. move front first n steps. 
      When front reaches end, cur indicates last n node, then use, pre.next = cur.next

    92. Reverse Linked List II
      use pre, cur, front nodes, 

N Sum Problems
====
    1 Two Sum
      method 1 brute force, iterate all the pairs, O(n^2)
      method 2 sort list, two pointer
      method 3 dictionary
  
    15 3 Sum
      method 1 sort first, then two pointer, iterate through the first element
               no duplicate, need to skip some numbers, if it's the same with previous one
    16 3 Sum Closest
      method 1 sort first, iterate through all the rest pairs, update result every time.

    18 4 Sum
      method 1 sort first, iterate 2 layers make it 2 sum
      O(n^3)
  
    454 4 Sum 2
      medhod 1 calculate sum of A,B permutation, calculate C,D permutation, then it's like 2 sum
      O(n^2)
  
  Sub question: Segment Tree
  ----
  
    560 Subarray Sum Equals K
      method 1 calculate subsum first, iterate newlist, store value in dic, check cur_sum - tar in dic 注意此处顺序！
    
    724 Find Pivot Number
      method 1 calculate sumall first, then iterate the current sum, check if fits
    
    523 modular segment tree
      method 1 use modular carry the sum, notice for k, [0,0,0,0] is valid result
  
  Sub Question: Combination Sum
  ----
    39
    
    40 
  
Binary Search
====
  index二分  
  左右边界为index，当左右index重合时跳出。通过A[index]来判断条件
  
    4 Median of Two Sorted Arrays
      中位数转化为找第K个数，分割两个数组，找到前面的最大值与后面的最小值
      利用二分法找到分割的ind
    
    33 Search in Rotated Sorted Array
      method 1 find pivot first, then search in the right part
      method 2 all together, 1 time search, every time test if nums[m] > nums[l]
    
    81 follow up of 33 duplicate number
      if cur == left or right, 
          left +=1 right -=1
  
    74 Search a 2D Matrix
      两次二分法
  
    240 Search a 2D Matrix II
      每一行二分搜索，由之前的结果得到右边的边界
  
  value二分
  左右边界为值，通过mid值来卡一些条件,通常关键词带有“第K个”
  
    378 Kth Smallest Element in a Sorted Matrix
    
    719 Find K-th Smallest Pair Distance
    
    786 K-th Smallest Prime Fraction
  

Array Manipulation
====
  palindrone
  ----
  substring for palindrone
  中心法遍历, 遍历string，以当前的为起始点，半径为0，向两边搜索，如果新的边界相等则半径+1 . 
  KMP 算法，类似trie树？
  
    5 Longest Palindromic Substring
      中心法搜索，记录当前最大半径，然后以最大半径起始搜，可以剪枝
    
    84. Largest Rectangle in Histogram
      iterate list, start from each position, find two edge of the rectangle
      optimize -> use stack for a ascending list, if find the next edge, calculate
    
    647 Palindromic Substrings
  
  subsequence
  DP法，从两头考虑，如果相同2+下一层，否则，两边分别减一找dp
  
    516 Longest Palindromic Subsequence
  
  string compare
  ----
  Simple iterate
  
    14 Longest Common Prefix
    
    54 Spiral Matrix
    
    
  Two pointers, forward tracking and back tracking
  n^2 -> n
  
    11 Container With Most Water
    
    42 Trapping Rain Water
    
    238 Product of Array Except Self
    
    75. Sort Colors
      left pointer for putting < to left, 
      right pointer for putting > to right, 
      the rest is just fine, cur pointer for getting cur value
    
    76. Minimum Window Substring
    brute force, n^2
    two pointer, move right for storing new character, move left for calculation result
    
    135. Candy
    front track, back track
    get max of both list to calculate
  
  DP, compare current, match or not, find result from next layer
  
    10 Regular Expression Matching
      if .*: if cur match, return (s[1:], p) or (s, p[2:])
             else: return (s, p[2:])
      make sure ahead if .* matches abc or aaa

Interval Questions
====
  Sort First, then iterate through the list 
  
    56 Merge Intervals
    
    57. Insert Interval
    difference senario
    left overlap, right overlap, outside all overlap, no overlap, first insert, last insert
    
Tree Structure
====
  Three iterate
    94
     
   
