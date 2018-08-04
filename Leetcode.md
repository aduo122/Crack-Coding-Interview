LinkedList Sum problems
----
  2.Add Two Numbers
    method 1 add number accordingly, add the additional number at last
    
  445.Add Two Numbers II
    method 1 get int numbers from the linkedlist first, then get the sum and turn into linkedlist as result
    method 2 iterate through the linkedlist, turn into stack, do the reverse iterate from stack
  
  43. Multiply Strings
    method 1 make function multiply, function add, iterate the small number to sum up the result.

N Sum Problems
----
  1. Two Sum
    method 1 brute force, iterate all the pairs, O(n^2)
    method 2 sort list, two pointer
    method 3 dictionary
  
  15. 3 Sum
    method 1 sort first, then two pointer, iterate through the first element
             no duplicate, need to skip some numbers, if it's the same with previous one
  16. 3 Sum Closest
    method 1 sort first, iterate through all the rest pairs, update result every time.
  
  18. 4 Sum
    method 1 sort first, iterate 2 layers make it 2 sum
    O(n^3)
  
  454. 4 Sum 2
    medhod 1 calculate sum of A,B permutation, calculate C,D permutation, then it's like 2 sum
    O(n^2)
  
  Sub question: Segment Tree
  
  560. Subarray Sum Equals K
    method 1 calculate subsum first, iterate newlist, store value in dic, check cur_sum - tar in dic 注意此处顺序！
  724. Find Pivot Number
    method 1 calculate sumall first, then iterate the current sum, check if fits
  523. modular segment tree
    method 1 use modular carry the sum, notice for k, [0,0,0,0] is valid result
  
  Sub Question: Combination Sum
  39.
  40. 
  
  Binary Search
  ----
  
