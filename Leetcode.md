Sort Problems
====
  Merge Sort
  ----
  
  Quick Sort
  ----
  
  Bucket Sort
  ----
    41. First Missing Positive Number
    put the positive number to the according index, 
    if nega then ignore, else, switch
    notice the switch ending condition, 1.cur is nega or too large 2. cur is right place 3. cur is equal to target
    

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

    25. Reverse Linked List into K group
      find if there's k element behind
      then revese the list
      connect pre and current head
      
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
  
Bit Manipulation
====
  Math and Binary Search
  
    50 Pow(x, n)
      x ^ n -> x*x ^(n/2)
      
    372. Super Pow
      1337 could be generalized to n
    
Array Manipulation
====
  Palindrone
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
  
  String compare
  ----
  Simple iterate
  
    14 Longest Common Prefix
    
    54 Spiral Matrix
    recursive method
    
    59 Spiral Matrix II
    recursive method
    
  Two pointers, forward tracking and back tracking
  n^2 -> n
  
    11 Container With Most Water
    
    30 Substring with Concatenation of All Words
      Notice a word can be used only once, 
      create a dic for count each word, 
      create a flag for counting if reaches the goal
      
      if the fast pointer find duplicate in dic, move the slow pointer remove to the duplicated element
    
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
      
    44 Wildcard Matching
      ？ -> (i+1,j+1)
      * -> (i, j+1) or (i+1, j) or (i+1, j+1)
  

  Interval Questions
  ----
  Sort First, then iterate through the list 
  
    56 Merge Intervals
    
    57. Insert Interval
    difference senario
    left overlap, right overlap, outside all overlap, no overlap, first insert, last insert
    
Tree Structure
====
  Three iterate
  inorder, preorder, postorder
  
    94
    
    450. Delete Node in a BST
    consider no child -> delete, 
             one child -> link from parent
             two child -> left right most or right left most switch
     
     
  Recursive
    test left, right then consider self, record global
  
    109. Convert Sorted List to Binary Search Tree
    
    
    87. Scramble String
    consider change or not for each step.
    change -> l1 = s[:l] r2 = s[len(s) - l:]
    not change -> l1 = s[:l] r2 = s[:l]
    
    113. Path Sum II
    
    508. Most Frequent Subtree Sum
    backtracking, maintain a global value of count and result
    
    
    
Graph Problems
====
  DFS & BFS
  
    51 & 52. N-Queens
    DFS, if the result is possible, add current line to result, return result 
    
    886. Possible Bipartition
    BFS, pay attention to nodes not in dislike, dic[node] = [] or test node in dic each time
    pay attention to when to stop the queue. use the two set to check if child is visited already.
  
  Topological Sort
    
    DFS -> find cycle or find sink
    BFS -> each layer, get sink or return cycle
    
OO Program
====
    146 LRU & LFU
    intrinsically, is ordered dictionary
    
Geometry
====
    rectangle area
    
    skyline

Recursive and DP
====
    399. Evaluate Division
    1. revert index, zero excluded
    2. dfs see if there's a connection, store the result in memo
    
    
    873. Length of Longest Fibonacci Subsequence
    consider dp[i][j] as the sequence ending as  A[i] and A[j]
    then if (A[j]-A[i]), A[i] is previously calculated, we can return that and +1
    
    837. New 21 Game
    first solution, calculate dp[i] from pre (dp[i-w] +...+ dp[i]) * 1/W
    Time O(n): N*W
    
    second solution,
    store the (dp[i-w] +...+ dp[i]) as t_sum
    every time 
    dp[i] = t_sum * 1/W
    t_sum += dp[i] - dp[i-W]
    
 DP to Greedy
 
    376. Wiggle Subsequence
    DP solution: maintain a increase and decrease dic, {pointer: length so far, last num}
    each time consider current num is increasing or decreasing, update the dictionary
    
    Greedy: consider turning point, the turning point remain the same
    
 Space O(n^2) -> O(n)
 
    115. Distinct Subsequences
    Campare current number each time, if not same -> move sourse to next, 
                                             same -> move both to next
                                             
    since only looking at the next level, could only maintain one layer of numbers
    
Backtracking
====
  Construct composition questions
  
    46 & 47 Permutation
    Consider if allows duplication.
    for duplicates:
    if used or (i > 0 and nums[i] == nums[i-1] and !used[i-1]): continue //make sure to use the previous letter first
    
    Caution! before trans list, do a deep copy!
    Caution!! start from the worst case
  
    93. Restore IP Addresses
    Caution, IP rules: 1. <=255 2. "010", "00" invalid
    
    211. Add and Search Word - Data structure design
    construct Trie Tree
    or, use dic for indexing length
  
    526. Beautiful Arrangement
    667. Beautiful Arrangement II
      From backtracking -> dp or greedy
      
  Backtracking to Greedy
  
    60. Permutation Sequence
    for each digit, calculate the index, then find the num at index from nums.pop(i)
    
    306, 842 Slice into Fibonaci 
    first find the beginning two numbers
    then test if the following numbers are valid.
  
  Backtracking to DP
  
    89. Gray Code
    each new number just add a digit 1 in the front of reversed list
    
    131. Palindrome Partitioning
    Consider how to cut first slice, then recursively cut. 
    Use memoization to optimize
    
  Permutation
  
    31.next permutation
    iterate, find next large number, follows init
    
Game Strategy
====

    464. Can I win
    maitain a list for posible draws. consider I draw a number and nomatter what you draw, I win
    
Trie Problem
====
    For pattern matching, 2 ways
    1. brute force
    iterate and find all the first letter in the pattern
    see if the following letters matches the pattern


    Construct Trie
      character serie
      at each word, tag index
      mark end at each word
    
    Suffix Trie
    
    Roller 
    


    2.suffix tree
    when patterns are too much,
    suffix tree is good
  
    
    
    
    
    
    
    
    
    
    
