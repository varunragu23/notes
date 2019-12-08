 
 
 
## Easy (153)
** 0. [Hamming Distance.java] (https://github.com/awangdev/LintCode/blob/master/Java/Hamming%20Distance.java) ** Level: Easy Tags: []
      
bit: XOR, &, shift >>



---

** 1. [Happy Number.java] (https://github.com/awangdev/LintCode/blob/master/Java/Happy%20Number.java) ** Level: Easy Tags: []
      
Basic Implementation of the requirements.

Use HashSet to save the viewed values. If repeated, return false.



---

** 2. [HashWithArray.java] (https://github.com/awangdev/LintCode/blob/master/Java/HashWithArray.java) ** Level: Easy Tags: []
      



---

** 3. [Heaters.java] (https://github.com/awangdev/LintCode/blob/master/Java/Heaters.java) ** Level: Easy Tags: []
      
first step:
Question type, it takes time to understand the meaning of the question:
Literally and drawing, it is to set the housing one by one, the distance around the house needs to be enough to reach the heater. The goal is to recruit as small a radius as possible, so it is necessary for the house and heater to be close together.
Set the house in the for loop, move the heater as an interval, and reach the first suitable interval. This is the smallest ideal radius at the moment. Take this value and compare it with the predetermined radius.
After the comparison, continue to move the house, and then try to move the heater interval to match.

The second step:
Binary Search

note!
The title does not say whether the given array is sorted, we must sort to be able to move between ranges or binary search.
TODO:
http://www.cnblogs.com/grandyang/p/6181626.html



---

** 4. [IndexMatch.java] (https://github.com/awangdev/LintCode/blob/master/Java/IndexMatch.java) ** Level: Easy Tags: []
      
Ordered, suppose there is such a number: target.        
The number to the left of target must not be greater than index, and the number to the right of target must be greater than index.     
This allows binary search.O (logn)



---

** 5. [Insert Node in a Binary Search Tree .java] (https://github.com/awangdev/LintCode/blob/master/Java/Insert%20Node%20in%20a%20Binary%20Search%20Tree%20. java) ** Level: Easy Tags: [BST]
      

Add something to the Binary Search Tree and you will definitely find a suitable leaf to add.

So: That is to say, when someNode.left or someNode.right is null, it is where the insert node is.

Find that someNode according to the normal Binary Search Tree law.



---

** 6. [Jewels and Stones.java] (https://github.com/awangdev/LintCode/blob/master/Java/Jewels%20and%20Stones.java) ** Level: Easy Tags: [Hash Table]
      
1524017454

Give J and S two strings. The character in J is unique jewelry, the character in S contains jewelry and stones. Find how many jewelry in S

#### Basic HashSet



---

** 7. [Longest Univalue Path.java] (https://github.com/awangdev/LintCode/blob/master/Java/Longest%20Univalue%20Path.java) ** Level: Easy Tags: []
      
Figure out what path means: connect the edge of a node.
To find MAX, you can define a max variable in the class scope.

Use the minimum amount of code to summarize several different situations: left == root, right == root, or left == root == right.



---

** 8. [Matrix Zigzag Traversal.java] (https://github.com/awangdev/LintCode/blob/master/Java/Matrix%20Zigzag%20Traversal.java) ** Level: Easy Tags: []
      
Analyze 4 steps: right, left-bottom, down, right-up    
Pay attention to the index when implementing. A little patience



---

** 9. [Minimum Absolute Difference in BST.java] (https://github.com/awangdev/LintCode/blob/master/Java/Minimum%20Absolute%20Difference%20in%20BST.java) ** Level: Easy Tags : [BST]
      

BST: inorder-traversal: first left node (adding to stack till left leav), then process stack.peek (mid node), then add rightNode && dive to rightNode.left leaf



---

** 10. [O (1) Check Power of 2.java] (https://github.com/awangdev/LintCode/blob/master/Java/O (1)% 20Check% 20Power% 20of% 202.java) ** Level: Easy Tags: [Bit Manipulation]
      



---

** 11. [Partition Array by Odd and Even.java] (https://github.com/awangdev/LintCode/blob/master/Java/Partition%20Array%20by%20Odd%20and%20Even.java) ** Level : Easy Tags: [Array, Two Pointers]
      

-More normal start / end partition pointer is similar to: when condition meet, swap
-Clean up TODO



---

** 12. [Pascal's Triangle II.java] (https://github.com/awangdev/LintCode/blob/master/Java/Pascal's%20Triangle%20II.java) ** Level: Easy Tags: []
      
Simple processing of array list.



---

** 13. [Permutation Index.java] (https://github.com/awangdev/LintCode/blob/master/Java/Permutation%20Index.java) ** Level: Easy Tags: []
      
The opposite of Permutation Sequence. Thoughts are similar.

The title is Easy, after a long thinking, analysis:    
Each digit number skips multiple possibilities that are less than the beginning of the number.

Take [6, 5, 2] as an example. We look for 6, 5 and 2 as the first few of the permudation.     
Normal ordering, which is the first of the permutation, should be [2, 5, 6]      
If you want to change from the first place, 2, to 6, how many possibilities are you going to cross?     
Quite simply, just ask: how many numbers are less than 6? (2, 5). Each number becomes head, and has its own set of changes, there are (n-1)! Possibilities.

The practice of this question: each (n-1)! Add up. Note: (n-1) means, how many permutations does the leading number (2,5) bring out, which is not (n-1)! Well.
	In this step, calculating the number is simple: (there are several numbers less than 6) × (how many numbers are left after removing the head)!

All the above are sacrificed in order to push 6 to the throne.

So after pushing 6 up, there are still others.

Continue to see 5, 2    
6 It is determined that the variable condition of the latter permutation may be [6, 5, 2], and then it may be [6, 2, 5].

Same process, look at the second 5 of the given array, count it as follows:     
1. How many numbers are less than 5?     
2. Apart from 5, how many numbers can be facillary?     
3. The same. Multiply the result by the second step.      

Finally, it depends on the last element 2.


After seeing all 6,5,2, add up.     
It is [6, 5, 2], all the lives you have stepped on!

My explanation is too vivid. Because it took so long to think ...



---

** 14. [Recover Rotated Sorted Array.java] (https://github.com/awangdev/LintCode/blob/master/Java/Recover%20Rotated%20Sorted%20Array.java) ** Level: Easy Tags: [Array ]
      

The meaning of rotate is that there is a point break, and the array from one side is selected and placed on the other side.
Rotate in three steps:
first half of rotate
second half of rotate
rotate all

Note that the breakpoint is found first.


---

** 15. [Reshape the Matrix.java] (https://github.com/awangdev/LintCode/blob/master/Java/Reshape%20the%20Matrix.java) ** Level: Easy Tags: []
      
Read the examples to understand the meaning of the questions.
Sort out counter case. Basic implementation



---

** 16. [Reverse String.java] (https://github.com/awangdev/LintCode/blob/master/Java/Reverse%20String.java) ** Level: Easy Tags: []
      
Similar to Reverse Integer.
Can use StringBuffer or two pointer reverse head / tail



---

** 17. [Search Insert Position.java] (https://github.com/awangdev/LintCode/blob/master/Java/Search%20Insert%20Position.java) ** Level: Easy Tags: []
      
General binary search.
At the end, determine which position to return.


---

** 18. [Shortest Word Distance.java] (https://github.com/awangdev/LintCode/blob/master/Java/Shortest%20Word%20Distance.java) ** Level: Easy Tags: []
      
Find short distance, wordB can be before and after wordA; at the same time, you only need to calculate the distance of a recent up to date.
Greedy constantly changes the A / B index and then compares it.



---

** 19. [Single Number.java] (https://github.com/awangdev/LintCode/blob/master/Java/Single%20Number.java) ** Level: Easy Tags: []
      
Bit XOR: When two bits are different, return 1. 
The title is about to extinguish all recurring numbers and leave the one that appears once.



---

** 20. [String Permutation.java] (https://github.com/awangdev/LintCode/blob/master/Java/String%20Permutation.java) ** Level: Easy Tags: []
      
Store #of occurrences in HashMap, add the first string and subtract the second string. Finally, see if there is any judgment that is not equal to 0.



---

** 21. [Trailing Zeros.java] (https://github.com/awangdev/LintCode/blob/master/Java/Trailing%20Zeros.java) ** Level: Easy Tags: [Math]
      



---

** 22. [Two Strings Are Anagrams.java] (https://github.com/awangdev/LintCode/blob/master/Java/Two%20Strings%20Are%20Anagrams.java) ** Level: Easy Tags: []
      
Method 1: char ascii with count [256]   
Pit: don't imagine this is a 26letter lowercase. May not be true.

Method 2: If it is other character encoding, not just utf16-encoding (java char)?   
Then continue to do it with strings



---

** 23. [Valid Sudoku.java] (https://github.com/awangdev/LintCode/blob/master/Java/Valid%20Sudoku.java) ** Level: Easy Tags: [Enumeration, Hash Table]
      

#### Hash Set
-Store visited value with HashSet.
-Validate row, col, and block in the nest for loop.     
-The validate block uses the growth law of i and j.    
-To put it bluntly, i && j is an index that grows from 0 to n. How to use it is flexible. This method solves all operations in the same nest for loop.
-`int c = 3 * (i% 3) + j% 3;` // make use of how i and j increases
-`int r = 3 * (i / 3) + j / 3;`

#### A bit Slower approach
-I did block validation alone: ​​I saw 4 layers of for when I validated the block. In fact, it is n ^ 2
-Maybe the code is a little more complicated



---

** 24. [Word Pattern.java] (https://github.com/awangdev/LintCode/blob/master/Java/Word%20Pattern.java) ** Level: Easy Tags: []
      
Each char represents a pattern. Use HashMap <char, str>.
But that's not enough. If a also matches dog, b also matches dog. For example, pattern = "abba", str = "dog dog dog dog".
So the second HashMap <str, char> is the other way around.
Make sure that pattern and str correspond one-to-one.



---

** 25. [Find Anagram Mappings.java] (https://github.com/awangdev/LintCode/blob/master/Java/Find%20Anagram%20Mappings.java) ** Level: Easy Tags: [Hash Table]
      

It is relatively simple. Use HashMap to store the index list. Finally, iterate through the array A again, and enumerate all the elements.
O (n)



---

** 26. [Judge Route Circle.java] (https://github.com/awangdev/LintCode/blob/master/Java/Judge%20Route%20Circle.java) ** Level: Easy Tags: [String]
      

Simple character checking. In all directions, plus, minus or minus.



---

** 27. [Island Perimeter.java] (https://github.com/awangdev/LintCode/blob/master/Java/Island%20Perimeter.java) ** Level: Easy Tags: [Hash Table]
      

#### Brutle
-4 walls per grid; -2 for each shared wall (the walls are two sides, -1 * 2)
-The final result is just fine.

#### Hash Table
-Don't think too much about using HashMap. But also think about it:
-Store all the blocks connected to each block in the list with the current block as the key. Then you need to convert the 2D coordinates into an index.
-At the end of the map, all key-values ​​should have value-key reverse mapping, so it can be eliminated for a long time, and each elimination is a shared wall.
-A little optimization: DFS finds all the islands. If the map of island is very large, and the island itself does not play, it is suitable for optimization.
-But the overall code is too complicated. It is not recommended to write.




---

** 28. [Power of Three.java] (https://github.com/awangdev/LintCode/blob/master/Java/Power%20of%20Three.java) ** Level: Easy Tags: [Math]
      

method 1:
Power of 3: 3 ^ x == n?
It means that n / 3 is always divided, and finally it can be equal to 1, then there is n / = 3, check n% 3, and finally see if the result is the method of dividing to 1. Use while loop.

Method 2:
If n is power of 3, then x of 3 ^ x must be a number smaller than n. Then you can do binary serach between 0 and n, but it is slower.

Method 3:
Ingenious idea. The largest 3 ^ x integer is 3 ^ 19. Then find this number, it must be divisible by n. One step in place.



---

** 29. [Plus One.java] (https://github.com/awangdev/LintCode/blob/master/Java/Plus%20One.java) ** Level: Easy Tags: [Array, Math]
      

Simple implementation, add 1, carry. The only tricky place, if you want one more last, it must be 10000 ... This mode, you can take a shortcut, directly come to an array of +1 size, and then the first bit = 1.
Note that converting to long is not reasonable, too much memory is used.


---

** 30. [Power of Two.java] (https://github.com/awangdev/LintCode/blob/master/Java/Power%20of%20Two.java) ** Level: Easy Tags: [Bit Manipulation, Math ]
      

Same as powerOfThree: you can loop, check mod; you can also use binary search to find the appropriate number.



---

** 31. [Reverse Vowels of a String.java] (https://github.com/awangdev/LintCode/blob/master/Java/Reverse%20Vowels%20of%20a%20String.java) ** Level: Easy Tags : [String, Two Pointers]
      

vowels: vowels. All reverse vowels are required.

##### Method 1: two pointer.
-Two pointers before and after, run inside the while loop.
-Pay attention to i <j. Once you meet, break.
-Find the right one, just do swap.
-StringBuffer can be used with sb.setCharAt ().
-O (n)
##### Method 2:
Take out all vowels, put them in reverse. O (n)



---

** 32. [Guess Number Higher or Lower.java] (https://github.com/awangdev/LintCode/blob/master/Java/Guess%20Number%20Higher%20or%20Lower.java) ** Level: Easy Tags : [Binary Search]
      

binary search formula



---

** 33. [Trim a Binary Search Tree.java] (https://github.com/awangdev/LintCode/blob/master/Java/Trim%20a%20Binary%20Search%20Tree.java) ** Level: Easy Tags : [BST, Tree]
      

method 1:
Suitable for reviewing BST. Treat each node with DFS. Note the characteristics of BST: all left nodes are smaller than the current node, and all right nodes are larger than the current node.

Use [L, R] to cut according to the meaning of the question. If node.val <L, directly drop the left side of the node, and return node.right. The same is true for R.
The division system is, DFS leftNode, rightNode. Then connect to node.left, node.right.

Method 2: Use iteration, not written yet.



---

** 34. [Array Partition I.java] (https://github.com/awangdev/LintCode/blob/master/Java/Array%20Partition%20I.java) ** Level: Easy Tags: [Array]
      

Give a string of numbers, size = 2n, find pairs, and then need to sum of min (pair) max.

(a1, b1), (a2, b2), ..., (an, bn) which makes sum of min (ai, bi) for all i from 1 to n as large as possible.

#### Sort, basics
-Starting from the result, you only need to find the result of the addition without emphasizing the specific match.
-Just write an example
-Find the rule of arranging single digits, and then consider the same rule of negative and positive numbers, then you can find the method of permutation.
-sort, O (nlogn)




---

** 35. [1-bit and 2-bit Characters.java] (https://github.com/awangdev/LintCode/blob/master/Java/1-bit%20and%202-bit%20Characters.java) * * Level: Easy Tags: [Array]
      

method 1:
Greedy.
Counting from the first bit: If a 1 is encountered, it must be jumped by two digits; if a 0 is encountered, it must be jumped by one digit.
loop to end, and see if index reaches the end.

Method 2:
I did it with DP hard: 
1. If the i-bit is 0, then dp [i-1] or dp [i-2] true is enough.
2. If the i bit is 1, then the i-1 bit must be 1 to satisfy the rule, and dp [i-2] needs to be true.



---

** 36. [Non-decreasing Array.java] (https://github.com/awangdev/LintCode/blob/master/Java/Non-decreasing%20Array.java) ** Level: Easy Tags: [Array]
      

When comparing ascending order, three digits i-1, i, i + 1 must be estimated.
Write down the relationship between i-1, i + 1, and then make a reasonable fix.

You need to really fix the array, because loop through will use the number after the fix for comparison.



---

** 37. [Max Consecutive Ones.java] (https://github.com/awangdev/LintCode/blob/master/Java/Max%20Consecutive%20Ones.java) ** Level: Easy Tags: [Array]
      

Basic. Math.max track results.
Remember to clear the result object after there is a loop for external operations.



---

** 38. [Find All Numbers Disappeared in an Array.java] (https://github.com/awangdev/LintCode/blob/master/Java/Find%20All%20Numbers%20Disappeared%20in%20an%20Array.java) ** Level: Easy Tags: [Array]
      

method 1:
Change to the correct position.
You need to be careful with handle i, because you don't know what is changed to nums [i], so you must clean it up in place to move on.

Method 2:
to mark!
Very clever use of the mark method, marked as a negative number, proves visit.
Preserve the negative number of the original number, so you can continue to use the absolute value of this negative number to find the position where the original number should be set. Very clever!

Method 3:
to mark!
Similar to method 2, it is also marked. This time, a number greater than n is added (because the title gives n a border), and finally check it. To not exceed Integer.MAX_VALUE, take the remainder before adding n each time.

Although the method of marking is fast, it is relatively hacky. It is probably not used in regular code.




---

** 39. [Maximum Average Subarray I.java] (https://github.com/awangdev/LintCode/blob/master/Java/Maximum%20Average%20Subarray%20I.java) ** Level: Easy Tags: [Array , Subarray]
      
time: O (n)
space: O (1)

Simply find sum of fixed window k, and at the same time max avg, and the remainder at the end.



---

** 40. [Largest Number At Least Twice of Others.java] (https://github.com/awangdev/LintCode/blob/master/Java/Largest%20Number%20At%20Least%20Twice%20of%20Others.java) ** Level: Easy Tags: [Array]
      

Find the maximum value, and the second largest value, and see if it fits the question.
Analyze the meaning of the question, the simplest method, you can loop twice: find the most value; compare.
But in fact, as a counterexample: if one is not satisfied, it is enough to oppose this 'at least twice of alllll others'.



---

** 41. [Toeplitz Matrix.java] (https://github.com/awangdev/LintCode/blob/master/Java/Toeplitz%20Matrix.java) ** Level: Easy Tags: [Array]
      

It seems that there are no algorithmic features, that is, the basic operation of array, and then split into a helper function to do repeated calculations and cut the code.
Pay attention to the boundary of check MxN.



---

** 42. [Sum of Two Integers.java] (https://github.com/awangdev/LintCode/blob/master/Java/Sum%20of%20Two%20Integers.java) ** Level: Easy Tags: [Bit Manipulation]
      

a ^ b is: incomplete addition.
a & b is: all possible rounds. a & b << 1 is the form of rounding to the left.

Goal: first add a ^ b naked, calculate the carry; then add the result and carry naked, and then calculate the carry of this round; then: naked price, calculate the carry ... until the carry == 0. 

So, first record the number of carry: carry. Then a ^ b is not completely added once. Then b is used to put the remaining carry, move one bit at a time, and continue adding until b cycles to 0.

After the first round a ^ b, the meaning of b itself disappeared. The parameter should be renamed next.
sum = a ^ b; // sum without adding carries
nextCarry = (a & b) << 1;

Substitute a, b for other variable names, which is better understood.

Bit Operation    
Steps: 
   a & b: the number of rounds that can occur per bit       
   a ^ b: the value that each bit may leave in this operation, XOR operation         
   Each time, the remainder is shifted by 1 digit, and then stored in b. loop until b == 0    

(http://www.meetqun.com/thread-6580-1-1.html)



---

** 43. [Swap Bits.java] (https://github.com/awangdev/LintCode/blob/master/Java/Swap%20Bits.java) ** Level: Easy Tags: [Bit Manipulation]
      

Simple, but a lot of knowledge:
1. Hex 0xaaaaaaaa is 1010101 .... 1010; 0x55555555 is 01010101 .... 0101
2. You can use these two hex to get singular and negative numbers. If you need to take other patterns, you can also do it.
3. x is likely to be a negative number, so right-shift should use logic shift, >>> to avoid leading negative complements.



---

** 44. [Intersection of Two Arrays II.java] (https://github.com/awangdev/LintCode/blob/master/Java/Intersection%20of%20Two%20Arrays%20II.java) ** Level: Easy Tags : [Binary Search, Hash Table, Sort, Two Pointers]
      

method 1:
Use HashMap: store a nums1, then check against map with nums2. Time / space: O (n)

Method 2:
Binary search? Requires array sorted. Otherwise time O (nlogn) is not worth it.
[Not done, wrong]



---

** 45. [Majority Element.java] (https://github.com/awangdev/LintCode/blob/master/Java/Majority%20Element.java) ** Level: Easy Tags: [Array, Bit Manipulation, Divide and Conquer]
      

#### Vote count
-vote ++, vote--the rest is winner. Time O (n), Space O (1)
-Majority Number means more than half. The number of more than half will have at least vote> = 1: match current majority number, vote ++; if not, vote--. 
-Note: there must be a majority number for the assert valid input. Otherwise this method will not work. [1,1,1,2,2,2,3] is an invalid input, the result is 3, of course it is wrong.

#### HashMap count occurance
-Time, Space: O (n)

#### Bit manipulation
-TODO

#### Related Problems
-Majority Number II, over 1/3, then divided into three parts, countA, countB to calculate the two that appear at most.
-Majority Number III, over 1 / k, then naturally divided into k parts. HashMap is used here.



---

** 46. [Nested List Weight Sum.java] (https://github.com/awangdev/LintCode/blob/master/Java/Nested%20List%20Weight%20Sum.java) ** Level: Easy Tags: [BFS , DFS]
      

Give a list of integers, the list may have a nest list. Calculate the total sum. The rule, if it is a nested list, each depth is a depth, sum must be multiplied by depth.

#### DFS
-New interface to understand: object contains integer or object
-Visit all && sum, consider dfs.
-bottom-> up is easier: pick nested object and execute dfs, which returns sum of it, add with (level value * weight).
-Simple processing of nested structure, dfs increases depth.
-time: visit all nodes eventually, O (n), space O (n)
-Note1: not multiplying on overall level sum. Only multiply level with single value at this level.
-Note2: top-> bottom is not necessary: ​​there is not need of passing added object into next level.

#### BFS
-bfs, queue, handle queue.size ().
-use a level variable to track levels



---

** 47. [Same Tree.java] (https://github.com/awangdev/LintCode/blob/master/Java/Same%20Tree.java) ** Level: Easy Tags: [DFS, Tree]
      

Give two binary trees to see if the two trees are identified.

#### DFS
-DFS. Determine leaf condition, && with all dfs (sub1, sub2).
-I have to walk through all the nodes anyway, so dfs is more suitable and easy to write.

#### BFS
-Two queues store all current level nodes of each tree. Check equality, check queue size.
-Populate next level by nodes at current level.



---

** 48. [Convert Sorted Array to Binary Search Tree.java] (https://github.com/awangdev/LintCode/blob/master/Java/Convert%20Sorted%20Array%20to%20Binary%20Search%20Tree.java) ** Level: Easy Tags: [DFS, Divide and Conquer, Tree]
      

As the title, build balanced BST from sorted array

#### DFS
-Binary Search Tree Features: The nodes on the left are smaller than the nodes on the right. 
-height balance, subtree height difference <1, the left and right sub trees must be shared equally. DFS (num, start, end)
-At each level, find the middle point, then divide 2 halves, continue with dfs
-Divide and Conquer
-time / space: O (n), visit all nodes, no redundant visits.



---

** 49. [Add Digits.java] (https://github.com/awangdev/LintCode/blob/master/Java/Add%20Digits.java) ** Level: Easy Tags: [Math]
      

Method 1: The common practice is to add the numbers according to the intent, double-while loop. The first layer of loop is O (n), and then the second layer of loop is a lot less digits, overall O (n)

Method 2: Find the mathematical rule. Every 9 digits, the mod will start to repeat, so you can find the answer indirectly by taking the mod for all numbers. O (1)



---

** 50. [Valid Anagram.java] (https://github.com/awangdev/LintCode/blob/master/Java/Valid%20Anagram.java) ** Level: Easy Tags: [Hash Table, Sort]
      

HashMap



---

** 51. [Binary Tree Paths.java] (https://github.com/awangdev/LintCode/blob/master/Java/Binary%20Tree%20Paths.java) ** Level: Easy Tags: [Backtracking, Binary Tree , DFS]
      

Give a binary tree, return all root-to-leaf path

#### DFS, backtracking
-Find all paths, bfs / dfs all works. Dfs will be simplier to write
-Recursive: Forked.dfs.
-top-> bottom: enumerate current node into the list, carry to next level, and backtrack
-top-> bottom is trivial to consider: path flows from top-> bottom

#### DFS, bottom-> up
-We can also take current node.left or node.right to generate list of results from the subproblem
-let dfs return list of string candidates, and we can run pair the list with currenet node, once they come back.
-TODO: can write code to practice

#### Iterative
-Iterative, a non-recursive exercise
-Because the list needs to be shortened each time, a Stack is added to store the level
-This problem is simpler with dfs, because the path from beginning to end is found, which is the pattern of dfs




---

** 52. [Linked List Cycle.java] (https://github.com/awangdev/LintCode/blob/master/Java/Linked%20List%20Cycle.java) ** Level: Easy Tags: [Linked List, Two Pointers]
      

#### Two Pointer: Slow Fast Pointer
-O (1) sapce: use fast and slow pointers. One runs .next, one runs .next.next. Once, fast will catch up with slow because of cycle.
-At that time, slow.val = fast.val.

#### Hash Table
-O (n) space: Use HashMap, always add elements. If there are duplicates, then obviously there is Cycle



---

** 53. [Min Stack.java] (https://github.com/awangdev/LintCode/blob/master/Java/Min%20Stack.java) ** Level: Easy Tags: [Design, Stack]
      

Double Stack: One normal stack, and the other minStack stores the current minimum level. Note the maintenance of changes in minStack

In addition, if you want maxStack, it is similar



---

** 54. [Implement Queue using Stacks.java] (https://github.com/awangdev/LintCode/blob/master/Java/Implement%20Queue%20using%20Stacks.java) ** Level: Easy Tags: [Design , Stack]
      

#### Double Stack
Draw a picture, know that the last stack is the reverseStack: pop (), peek (), empty () are all on this stack, no transformation is required.
Push () does the stack and reverseStack dumps back and forth.
Compared to the old code, dumping in PUSH is easier to read.

#### Previous notes
Double Stack. One is equal to queue and the other is backfillStack.
Tricky: It is backfilled during pop () and peek (), and waits until the stack is used up before backfilling.
Write an example to know that if you backfill early, stack.peek () is not the head of the queue.




---

** 55. [Reverse Integer.java] (https://github.com/awangdev/LintCode/blob/master/Java/Reverse%20Integer.java) ** Level: Easy Tags: [Math]
      

#### method 1
Add x% 10 each time, then x keeps decreasing ~ 0
Pay attention to handling MAX_VALUE, MIN_VALUE
The symbol is not important, it is processed directly, and it is also retained.

#### Method 2
Convert to String and then reverse
Space O (n), time O (n)



---

** 56. [Sqrt (x) .java] (https://github.com/awangdev/LintCode/blob/master/Java/Sqrt (x) .java) ** Level: Easy Tags: [Binary Search, Math ]
      

#### s- qrt (int x)
-Understand the meaning of the question, find a value that can be m * m = x from [0, x].
-Note, if you ca n’t find it, ask the examiner what value to return: It makes sense because return int will be rounded, so returning a square up to x is fine.
-Note the use of long for mid, as it is likely to exceed the maximum int.

#### sqrt (double x)
-Bisection float number, the end should be defined by precision.
-Still dichotomy, but the judgment condition becomes: while (end-start> eps)
-eps = 1e-12, i.e. accuracy to 1e-12



---

** 57. [First Bad Version.java] (https://github.com/awangdev/LintCode/blob/master/Java/First%20Bad%20Version.java) ** Level: Easy Tags: [Binary Search]
      

Binary Search

According to the nature of isBadVersion, determine how to end = mid or start = mid.     
isBadVersion is directional. One point is wrong, and the other is wrong.



---

** 58. [Meeting Rooms.java] (https://github.com/awangdev/LintCode/blob/master/Java/Meeting%20Rooms.java) ** Level: Easy Tags: [PriorityQueue, Sort, Sweep Line]
      

-Pay attention to the joint points to take into account the situation of all meetings, do not accidentally miss the joint points
-The meeting was Superman. Move instantly to the next meeting

#### method 1:
Find if there is an overlap. PriorityQueue After sorting according to start time, compare current and peek: current.end> peek.start?

#### Method 2: Sweep line
-class Point {pos, flag}, PriorityQueue sort. Count
-Is a type of problem with Number of Airplanes in the Sky



---

** 59. [Binary Tree Inorder Traversal.java] (https://github.com/awangdev/LintCode/blob/master/Java/Binary%20Tree%20Inorder%20Traversal.java) ** Level: Easy Tags: [Hash Table, Stack, Tree]
      

Inorder traverse Binary Tree

#### Recursive
-Recursive on your own, without helper function
-Divide and Conquer, with helper (dfs) method
-O (n) time, no extra space

#### Iterative: Stack
-Add left nodes all the way   
-Print curr   
-Move to right, add right if possible
-O (n) time, O (h) space
  
Note that stack.pop () must add curr = curr.right after adding the left-most child.

Without moving right, a dilemma is likely to occur:
The next round of curr is to find its left-most child, and repeating curr and curr.left repeatedly will infinite loop, always up and down on the left.

#### HashMap
How?



---

** 60. [Change to Anagram.java] (https://github.com/awangdev/LintCode/blob/master/Java/Change%20to%20Anagram.java) ** Level: Easy Tags: [String]
      

Random title in HackerRank: Give a string, everything in half, see how many characters the two halves will change, can become anagram.

-Cut the two halves into two Strings A and B. Int count [26] respectively, ++,-.
-Record the frequency of 26 lower case letters. If all offset, it is anagram.
-Note: In the end, count should be divided by 2: different letters, and count will be added to and subtracted from different letter positions, then the calculation is just repeated. So divide by two

-Note: Write your own in HackerRank: Scanner, import java.util, non-static method ... etc.



---

** 61. [Classical Binary Search.java] (https://github.com/awangdev/LintCode/blob/master/Java/Classical%20Binary%20Search.java) ** Level: Easy Tags: [Binary Search]
      

#### Binary Search Template
-while: start + 1 <end
-mid = start + (end-start) / 2;
-Compare by mid
-Double check start, end.




---

** 62. [Climbing Stairs.java] (https://github.com/awangdev/LintCode/blob/master/Java/Climbing%20Stairs.java) ** Level: Easy Tags: [DP, Memoization, Sequence DP]
      

Each step can take 1 or 2 steps, find out how many ways to climb the ladder in total.

#### Recursive + Memoization
-Recursion is well written, but repeated calculations, timeout. Time: O (2 ^ n)
-O (2 ^ n): each n can spawn 2 dfs child, at next level, it will keep spawn. Total 2 ^ n nodes will spawn.
-Use global variable int [] memo to help reduce double counting
-O (n) time, space

#### DP
-The principle of addition, the last step is determined by the first two moves: dp [i] = dp [i-1] + dp [i-2]
-Basic sequence DP, int [] dp = int [n + 1];
-DP [] is stored as 1-based index
-dp [i]: count # of ways to finish
-Need to know the status of dp [n], but the maximum coordinate is [n-1], so int [n + 1]
-dp [0] often has special status
-O (n) space, time

#### Sequence DP, scrolling array
-[i] only associates with [i-2], [i-1].
- %2
-O (1) space



---

** 63. [Closest Binary Search Tree Value.java] (https://github.com/awangdev/LintCode/blob/master/Java/Closest%20Binary%20Search%20Tree%20Value.java) ** Level: Easy Tags : [BST, Binary Search, Tree]
      

Give a BST, and a double target, and find the closest number.

#### Recursive
-when less than curr val, consider left
-when greater than curr val, consider right
-dfs to the end, then compare each layer, then return

#### Binary Search
-Records found closest
-Binary Search, according to current node position,
-Find node.val == target, or finish walking, return closest



---

** 64. [Binary Tree Preorder Traversal.java] (https://github.com/awangdev/LintCode/blob/master/Java/Binary%20Tree%20Preorder%20Traversal.java) ** Level: Easy Tags: [BFS , DFS, Stack, Tree]
      

#### Recursive
-Add root, left, then right. Obvious
-Divide and conquer
-Actually no helper function is needed

#### Iterative
-First add root, then push the bottom of the stack (root.right) at the end of the process, then push root.left
-Stack: push curr, push right, push left.   



---

** 65. [Closest Number in Sorted Array.java] (https://github.com/awangdev/LintCode/blob/master/Java/Closest%20Number%20in%20Sorted%20Array.java) ** Level: Easy Tags : [Binary Search]
      

-A variant of Binary Search, LintCode can't run any further.
-Consider mid-1, mid + 1.
-Once there is no mid = target.index. Then the target will eventually narrow down at (mid-1, mid) or (mid, mid + 1)   



---

** 66. [Complete Binary Tree.java] (https://github.com/awangdev/LintCode/blob/master/Java/Complete%20Binary%20Tree.java) ** Level: Easy Tags: [BFS, Tree]
      

A complete binary tree is a binary tree in which every level, except possibly the last,

is completely filled, and all nodes are as far left as possible

#### BFS
-When a node with null children appears for the first time, the leaf level is reached, mark flag = true;
-From now on, queues should no longer have nodes and children; left / right children of nodes appearing behind the queue should all be null
-Otherwise there is a problem, return false;




---

** 67. [Compare Strings.java] (https://github.com/awangdev/LintCode/blob/master/Java/Compare%20Strings.java) ** Level: Easy Tags: [String]
      

See if StringA includes all StringB characters.

#### Basic Implementation
-Compare sizes, null.
-Then use int [] to count chars from A, count [x] ++. Then compare chars in B, count [x]-
-If count [c] <0, then false.
-O (n)



---

** 68. [Contains Duplicate.java] (https://github.com/awangdev/LintCode/blob/master/Java/Contains%20Duplicate.java) ** Level: Easy Tags: [Array, Hash Table]
      

Unordered array, find if there are duplicate elements, return true / false.

#### HashSet
-No brain: HashSet.
-Time O (n), Space O (n)

#### Sort, Binary Search
-Arrays.sort (x): Time O (nLogN), Space O (1)
-After sorting, the repeating numbers will be sorted together, then binary search



---

** 69. [Contains Duplicate II.java] (https://github.com/awangdev/LintCode/blob/master/Java/Contains%20Duplicate%20II.java) ** Level: Easy Tags: [Array, Hash Table ]
      

Unsorted array, find out if there are duplicate elemenets: the necessary condition is that the size of the index i, j of these two elements differ by at most k.

#### HashSet
-Very cleverly control the value in HashSet to [i-k, i] according to the conditions of k range
-Each time you add new elements to the set, subtract the element at the end of the index from the set
-Set.add (x) will return false if it encounters duplicates.
-Once there is a repetition in this range of length k, the conditions are met. 
-Time O (n)

#### HashTable <value, List of duplicates>
-Record the index of each element value in the list
-Once there are duplicate element repeats, put the entire list of indexes out, and check if there are any matching conditions: (index-i) <= k
-Time O (nm), m = # of duplicates

#### The difference between these two approaches is artistic
-Method 1 is to limit the selection of selected dates, and remove them if they are not qualified, then once there are duplicates, then it must be certain, and the rest will not be viewed.
-Method 2 is to find the index that meets the conditions and process it centrally, but all candidates will be selected
-It ’s like recruiting people: one is to stop when you are good; the second is to see everyone and choose the best one. Obviously the first is faster.




---

** 70. [Nim Game.java] (https://github.com/awangdev/LintCode/blob/master/Java/Nim%20Game.java) ** Level: Easy Tags: [Brainteaser, DP, Game Theory]
      

#### Brainteaser
-Famous Nim games
-Write some and find that the situation after n = 4,5,6,7,8 ... etc is regular: Whoever gets 4 first loses.
-It is very simple in the end n% 4! = 0, time, space O (1)

#### DP
-Formally and regularly, just like coins in a line, do it first hand first
-Can roll array to optimize space
-Time O (n), of course, this question will timeout, you can use braineaser to write the result.



---

** 71. [Convert Integer A to Integer B.java] (https://github.com/awangdev/LintCode/blob/master/Java/Convert%20Integer%20A%20to%20Integer%20B.java) ** Level : Easy Tags: [Bit Manipulation]
      

How many bits do I need to change to convert Integer A to Integer B?

#### Bit Manipulation
-a ^ b shows the digits with different binary codes in the bit format.
-Each time (a ^ b) >> i moves by i, then & 1 actually means that the number is left.
-count 
-It's practical ^ find different bits, >> shift, & 1 mask



---

** 72. [Cosine Similarity.java] (https://github.com/awangdev/LintCode/blob/master/Java/Cosine%20Similarity.java) ** Level: Easy Tags: [Basic Implementation]
      

According to the formula of Cosine Similarity, basic implementation



---

** 73. [Count 1 in Binary.java] (https://github.com/awangdev/LintCode/blob/master/Java/Count%201%20in%20Binary.java) ** Level: Easy Tags: [Bit Manipulation]
      

count how many 1 in a 32-bit number binary format

#### Bit Manipulation
-shift >> i 
-apply mask & 1

#### Convert to string O (n) space
You can put integer-> string-> char array.



---

** 74. [Count and Say.java] (https://github.com/awangdev/LintCode/blob/master/Java/Count%20and%20Say.java) ** Level: Easy Tags: [Basic Implementation, String ]
      

Introduce a method of counting numbers, and then read the result of the previous line for each line, and calculate it line by line. Ask what is the nth line?

#### Basic Implementation
-Mainly because the meaning of the question is difficult to understand, very misleading. When the question is understood, there are actually no algorithm requirements.
-Count duplicates and print



---

** 75. [Paint House.java] (https://github.com/awangdev/LintCode/blob/master/Java/Paint%20House.java) ** Level: Easy Tags: [DP, Sequence DP, Status DP ]
      
time: O (nm), m = # of colors
space: O (nm)

To paint n houses, and the cost [] [] of nx3. Find the minimum cost to paint all houses.

#### Sequence DP
-Find the min cost of dp [i], but do not know what color the last house chooses, then iterate through the colors of the last house (i-1)
-While selecting the color of the last house, find the lowest cost according to the color of dp [i-1] / cost + cost [i-1]
-Consider the last position of DP (color selection): color status needs to be attached to DP [i]: define a two-dimensional array, one of which is status
-dp [i] [j]: the minimum cost of painting the j color in the first i houses.
-dp [0] [j] = 0: 0th house, no cost
-Calculation order: Counting from each house [0 ~ n], first for loop
-Then select the color of the ith house, and then select the color of the (i-1) th house. Double for loop, skip same color

#### Rolling Array
-Observe that index [i] is only related to [i-1], so 2 digits are sufficient,% 2



---

** 76. [Longest Continuous Increasing Subsequence.java] (https://github.com/awangdev/LintCode/blob/master/Java/Longest%20Continuous%20Increasing%20Subsequence.java) ** Level: Easy Tags: [Array , Coordinate DP, DP]
      

Find the length of the continuous continuous rising subsequence.

#### Coordinate DP
-1D coordinate, the subscript of dp, is the state of index i
-Find the maximum value, dp [i] = longest subsequence at index i
-If nums [i]> nums [i-1], dp [i] = dp [i-1] + 1
-If it does not continue to rise, then dp [i] = 1, repeat
-maintain max

#### Basic
-Use a number to store current count, maintain max



---

** 77. [House Robber.java] (https://github.com/awangdev/LintCode/blob/master/Java/House%20Robber.java) ** Level: Easy Tags: [DP, Sequence DP]
      
time: O (n)
space: O (n) or rolling array O (1)

Search for houses, the adjacent ones cannot touch. Each house has value, find max.

#### Sequence DP
-dp [i]: max gain from the first i house
-Look at the previous one or two of the last ending state, and then consider the current situation
-Find out the relationship between the current [i] and the previous [ix] situation: it is not possible to connect the house, then consider the situation of dp [i-2] directly
-Sequence DP, new dp [n + 1];

#### Rolling Array
-[i] 'is only relevant for the first two seats [i-1], [i-2]'
-Mark [i], [i-1], [i-2] with% 2.
-Others use curr / prev to represent coordinates when scrolling. Here% 2 is more abstract, but more practical.




---

** 78. [Find All Anagrams in a String.java] (https://github.com/awangdev/LintCode/blob/master/Java/Find%20All%20Anagrams%20in%20a%20String.java) ** Level : Easy Tags: [Hash Table, Sliding Window]
      

Much like Permutation in String. Give short string p, long string s.

Find the starting index of all p's anagram (permutation) in s.

#### HashTable
-count character apperance
-Note the tricks of countS, countP: only O (26) for comparison
-Overall timeO (n)
-Be careful not to use an int [] count to technically check 0, the complexity is O (n)



---

** 79. [Count Primes.java] (https://github.com/awangdev/LintCode/blob/master/Java/Count%20Primes.java) ** Level: Easy Tags: [Hash Table, Math]
      

Count: all prime numbers less than n.

#### Prime number definition
-> = 2 has no common divisors other than itself and 1.   
-There is another way to define: this n, is there an i less than n, and achieve: i * i + # of i = n. If there is, it is not prime   

#### Steps
-A boolean bar, isPrime []. Then from i = 2, all become true.
-hash key: the number itself
-Then use the nature of this factor, non-prime meets the conditions: self * self, self * self + self ... etc.     
-So check every j, j + i, j + i + i, and mark all non-prime as false.     
-Finally, just count the remaining true numbers.   



---

** 80. [Delete Node in a Linked List.java] (https://github.com/awangdev/LintCode/blob/master/Java/Delete%20Node%20in%20a%20Linked%20List.java) ** Level : Easy Tags: [Linked List]
      

Given Singlely linked list, delete an arbitrary node (cannot be a head node)

#### Basic
-update node.val
-Link curr.next to curr.next.next



---

** 81. [Excel Sheet Column Number.java] (https://github.com/awangdev/LintCode/blob/master/Java/Excel%20Sheet%20Column%20Number.java) ** Level: Easy Tags: [Math ]
      

#### Math
-26-bit operation, thinking based on 10-bit operation
-'A'-'A' = 0. So char-'A' + 1 = corresponding digits in the title
-Or: 26-bit operation is the same as 10-bit: num + = digit per digit * Math.pow (26, number number)




---

** 82. [Excel Sheet Column Title.java] (https://github.com/awangdev/LintCode/blob/master/Java/Excel%20Sheet%20Column%20Title.java) ** Level: Easy Tags: [Math ]
      

#### Basic Conversion
-26 bits
-From the end, mod% 26 can get the last number remain = n% 26
-Special: When remain = 0, which means n is a multiple of 26, the end should be 'Z'
-After recording 'Z', n--




---

** 83. [Flip Game.java] (https://github.com/awangdev/LintCode/blob/master/Java/Flip%20Game.java) ** Level: Easy Tags: [String]
      

#### String
-You can use sb.replace (i, j, "replacement string")
-Simply press window = 2 to scan
-Turned from '++' to '-'
-O (n)



---

** 84. [Implement strStr () .java] (https://github.com/awangdev/LintCode/blob/master/Java/Implement%20strStr () .java) ** Level: Easy Tags: [String, Two Pointers]
      

Give two strings A, B, find one B at the beginning of A.

#### Two Pointer
-Find the starting position of B in A, and see if the substring from this point is equal to B.
-Quite a lot of pits, these can help optimize:
-1. When B is "", that is, B can be found in the actual position of A .... index = 0.
-2. edge condition: if haystack.length () <needle.length (), it must be wrong, return -1
-3. If the remaining length after a certain index, A is shorter than the length of B, it is also a misunderstanding, return -1



---

** 85. [Last Position of Target.java] (https://github.com/awangdev/LintCode/blob/master/Java/Last%20Position%20of%20Target.java) ** Level: Easy Tags: [Binary Search]
      

Give a sorted integer array, find the last index where the target appears. There are duplicate numbers in the array

There are duplicates, not the end point, continue binary search



---

** 86. [Length of Last Word.java] (https://github.com/awangdev/LintCode/blob/master/Java/Length%20of%20Last%20Word.java) ** Level: Easy Tags: [String ]
      

Give a String with lower case character and ''. Find the length of the last single word

#### basics
-Look for '' from the end and find the calculated length
-Remember to s.trim (), remove the leading and trailing spaces



---

** 87. [Longest Increasing Continuous subsequence.java] (https://github.com/awangdev/LintCode/blob/master/Java/Longest%20Increasing%20Continuous%20subsequence.java) ** Level: Easy Tags: [Array , Coordinate DP, DP]
      

https://leetcode.com/problems/longest-continuous-increasing-subsequence/description/

O (n) runs for 2 times.
O (1) uses two ints to store: every time it reaches the point i, the point i meets the condition or does not satisfy all the longestIncreasingContinuousSubsequence.
Features: One run back, the ans will continue to be compared with the left ans; what is the maximum value in all cases.



---

** 88. [Maximum Subarray.java] (https://github.com/awangdev/LintCode/blob/master/Java/Maximum%20Subarray.java) ** Level: Easy Tags: [Array, DFS, DP, Divide and Conquer, PreSum, Sequence DP, Subarray]
      
time: O (n)
space: O (n), O (1) rolling array

Give a list of arrays, unsorted, can have negative / positive num. Find the maximum of the sum of the numbers in the subarray in the middle of the array

#### Sequence DP
-dp [i]: the maximum sum of the first i elements, including last element (i-1), the possible subarray.
-init: dp = int [n + 1], dp [0]: first 0 items, does not have any sum
-Because of the continuous sequence, when the condition is not met, it will break. That is: need to take curr num, regardless => can drop prev max in dp [i]
-track overall max 
-init dp [0] = 0; max = MIN_VALUE because there are negative numbers
-Time, space O (n)
-Rolling array, space O (1)

#### Divide and Conquer, DFS
-Find a mid piont, consider 3 cases: only the left, only the right, cross-mid
-left / rigth case, direct dfs
-corss-mid case: continuous sum max from left + continous sum max from right + mid
-continuous sum max from one direction:


---

** 89. [Median.java] (https://github.com/awangdev/LintCode/blob/master/Java/Median.java) ** Level: Easy Tags: [Array, Quick Select, Quick Sort]
      

Given an unordered array, find median (the number in the middle after sort).

#### Quick Select
-Same as the template for `kth largest element in an Array`.
-Different from quickSort, it only needs to recurring in half of the list each time, so the time complexity of O (logn) is reduced to O (n)
-quickSelect finds the smallest kth element
-Using this principle, find the minimum value of kth, then if == target index, we find our median
-Quick select template to be familiar with, you may want it all at once, but you ca n’t write it
-Main steps: partition, dfs, only recur on one part of the array 




---

** 90. [Middle of Linked List.java] (https://github.com/awangdev/LintCode/blob/master/Java/Middle%20of%20Linked%20List.java) ** Level: Easy Tags: [Linked List]
      

Find the middle node of the Linked List

-Fast and slow hands
-Don't care if slow is in the end, because fast must come first.
-Make sure fast, fast.next is not Null



---

** 91. [Singleton.java] (https://github.com/awangdev/LintCode/blob/master/Java/Singleton.java) ** Level: Easy Tags: [Design]
      

Let a class be a singleton



---

** 92. [Remove Linked List Elements.java] (https://github.com/awangdev/LintCode/blob/master/Java/Remove%20Linked%20List%20Elements.java) ** Level: Easy Tags: [Linked List]
      

Remove all targets from the linked list

#### Basics
-If match: node.next = head.next;
-If not match, node and head move together



---

** 93. [Fibonacci.java] (https://github.com/awangdev/LintCode/blob/master/Java/Fibonacci.java) ** Level: Easy Tags: [DP, Math, Memoization]
      

#### Memoization
-fib [n] = fibonacci (n-1) + fibonacci (n-2);

#### DP array.
-Scrolling array, simplified DP

#### recursively calculate
-recursively calculate fib (n-1) + fib (n-2). The formula is fine, but the time is too long, timeout.




---

** 94. [Palindrome Linked List.java] (https://github.com/awangdev/LintCode/blob/master/Java/Palindrome%20Linked%20List.java) ** Level: Easy Tags: [Linked List, Two Pointers]
      

#### Reverse Linked List
-The Palindrome concept is very simple, but it is difficult to get random access coordinates in the Linkde List: so half of the ListNode needs to be flipped
-reverse linked list: traverse the beginning
-Use the speed to find the mid point
-Time O (n), and does not require additional space (just reverse the internal order of half a list), so space O (1)

#### Previous Note
-Palindrome must be equal on both sides
-linkedlist cannot reverse iterating, then reverse the list, bloom from the middle for comparison.



---

** 95. [Reverse Linked List.java] (https://github.com/awangdev/LintCode/blob/master/Java/Reverse%20Linked%20List.java) ** Level: Easy Tags: [Linked List]
      

#### Reverse List
-Basic operation of Linked List: every insert at the beginning
-Use head to cycle through all nodes
-No additional space required
-Time O (n), Space O (1)



---

** 96. [Intersection of Two Linked Lists.java] (https://github.com/awangdev/LintCode/blob/master/Java/Intersection%20of%20Two%20Linked%20Lists.java) ** Level: Easy Tags : [Linked List]
      

For two linked lists, ask which node starts, and the two linked lists start to overlap?

#### Basics
-Length list, find overlap
-If the length is different, cut the extra length of the long list
-After the starting point is the same, the coincidence point will arrive at the same time
-Time O (n) * 2, constant space



---

** 97. [Palindrome Permutation.java] (https://github.com/awangdev/LintCode/blob/master/Java/Palindrome%20Permutation.java) ** Level: Easy Tags: [Hash Table]
      

For String, see if the permutation can be Palindrome

#### Hash, or ASCII array
-count occurrance
-Only one odd # appearance can be accepted.
-Consider all 256 ASCII codes, if you want to expand, use HashMap <Character, Integer>
-Note, cannot assum lower case letter. It should be at least all ASCII codes



---

** 98. [Valid Palindrome.java] (https://github.com/awangdev/LintCode/blob/master/Java/Valid%20Palindrome.java) ** Level: Easy Tags: [String, Two Pointers]
      

Verify that the string is palendrome. Only alphanumeric is considered, other characters can be ignored

#### Check Palindrome
-Two pointers before and after, move to the middle to see if the letters overlap

#### filter alphanumeric
-You can use ASCII code to filter manually, as long as it is between '0' ~ '9', 'a' ~ 'z', 'A'-'Z'
-You can also use regular expression: match all these letters, which is [a-zA-Z0-9]
-Any match of these letters is the opposite: "[^ a-zA-Z0-9]". Test: https://regex101.com/



---

** 99. [Implement Stack using Queues.java] (https://github.com/awangdev/LintCode/blob/master/Java/Implement%20Stack%20using%20Queues.java) ** Level: Easy Tags: [Design , Stack]
      

As the title.

#### Queue, pouring water
-Two Queues, pouring water interactively
-Swap with a Temp

##### Practice 1
-The logic is in push:
-1. x put q2.
-2. q1 all offer / append to q2.
-3. Use a Temp for swap q1, q2.
-The head of q1 is always the last value added.


##### Practice 2
-The logic is in top () / pop (), every time you change the water, check the last item.




---

** 100. [Implement Stack.java] (https://github.com/awangdev/LintCode/blob/master/Java/Implement%20Stack.java) ** Level: Easy Tags: [Stack]
      

Just use a data structure, implement stack.

#### Stack, first in, last out
-ArrayList: return / remove the last item of the ArrayList.
-2 Queues



---

** 101. [Invert Binary Tree.java] (https://github.com/awangdev/LintCode/blob/master/Java/Invert%20Binary%20Tree.java) ** Level: Easy Tags: [BFS, DFS, Tree]
      

#### DFS
-Simple handling of swap
-recursively swap children

#### BFS
-BFS with Queue
-Process one node at a time, swap children; then add child to queue
-Until the queue process is complete



---

** 102. [Maximum Depth of Binary Tree.java] (https://github.com/awangdev/LintCode/blob/master/Java/Maximum%20Depth%20of%20Binary%20Tree.java) ** Level: Easy Tags : [DFS, Tree]
      

Give a binary tree, find the deepest depth

#### DFS
-I have to walk through all the nodes here, so dfs is very suitable
-Divide and conquer. 
-Maintain a maximum value: Math.max (maxDepth (root.left), maxDepth (root.right)) + 1;
-Note check root == null

#### Note
-BFS is doable as well, but a bit more code to write: tracks largest level we reach



---

** 103. [Minimum Depth of Binary Tree.java] (https://github.com/awangdev/LintCode/blob/master/Java/Minimum%20Depth%20of%20Binary%20Tree.java) ** Level: Easy Tags : [BFS, DFS, Tree]
      

#### BFS
-Shortest path; minimum depth: Think of BFS, check level by level, BFS can make sure you find results faster
-depth definition: reach to a leaf node, where node.left == null && node.right == null
-BFS using queue, track level.


#### DFS
-Divide and Conquery a minimum. 
-Pay attention to processing Leaf's null: when the leaf appears, the leaf is ignored, and the direct return counts as a leaf
-Another way to count: use Integer.MAX_VALUE instead of null leaf, this can avoid wrong counting. (Can't directly recursive)
-This will take all nodes anyway, so dfs should be more suitable.




---

** 104. [Symmetric Tree.java] (https://github.com/awangdev/LintCode/blob/master/Java/Symmetric%20Tree.java) ** Level: Easy Tags: [BFS, DFS, Tree]
      

Check if tree is symmetric

Note the example and definition of Symmetric Binary Tree: mirror-like symmetry. It is not that the left and right sub-trees are equal.

#### DFS
-Recursively check symmetrically corresponding Node.  
-The children of each node and the children of the node opposite to the other side of the mirror are exactly mirror reflection positions.

#### Stack
-stack1: Left-hand sub-tree is added first, then right child; 
-stack2: Right-hand sub-tree is added with right child first, then left child.   
-During the process, if symmetric, all the nodes in the stack will correspond one by one.



---

** 105. [Tweaked Identical Binary Tree.java] (https://github.com/awangdev/LintCode/blob/master/Java/Tweaked%20Identical%20Binary%20Tree.java) ** Level: Easy Tags: [DFS , Tree]
      

Check if the binary tree is identified. 

Features: If the subtree has rotation, as long as the tree node values ​​are equal, it can be considered as an identifier.

#### DFS
-Based on DFS, compare left and right, left and right, left and right



---

** 106. [Merge Two Binary Trees.java] (https://github.com/awangdev/LintCode/blob/master/Java/Merge%20Two%20Binary%20Trees.java) ** Level: Easy Tags: [DFS , Tree]
      

#### DFS
-Basic binary tree traversal. Pay attention to the judgment of null child



---

** 107. [Subtree.java] (https://github.com/awangdev/LintCode/blob/master/Java/Subtree.java) ** Level: Easy Tags: [DFS, Tree]
      

Give a binary tree s, and a binary tree t, check if t is a subtree of s.

#### DFS
-It's very similar to the identification of binary tree
-Compare same tree is required only when current s.val = t.val.
-In other cases, continue to recursively isSubtree
-Note: Even if T1 == T2 is found, it is likely that the numbers are the same (here is not a binary search tree !!), and children are different
-So continue to recursively isSubtree (T1.left, T2) ... etc.



---

** 108. [Lowest Common Ancestor II.java] (https://github.com/awangdev/LintCode/blob/master/Java/Lowest%20Common%20Ancestor%20II.java) ** Level: Easy Tags: [Hash Table, Tree]
      

Give a Binary Tree root, and two nodes A, B. Features: The parent pointer is stored in the node. Find the lowest common ancestor


#### Hash Set
-This question has a strange place, each node also has a parent, so it can be bottom-up.
-save visited in hashset. The first duplicate is the lowest common ancestor of AB

#### Save in lists
-Bottom-up. Use parent to return to root
-Save all parents, then find the last common node in the two lists

#### Note
-Can't search target node directly from root to make two lists. Because it's not Binary Search Tree at all!




---

** 109. [Hash Function.java] (https://github.com/awangdev/LintCode/blob/master/Java/Hash%20Function.java) ** Level: Easy Tags: [Hash Table]
      

#### Hash Function
-Explain how Hash does it. 
-Hash function example:    
-hashcode ("abcd") = (ascii (a) * 33 ^ 3 + ascii (b) * 33 ^ 2 + ascii (c) * 33 ^ 1 + ascii (d) * 33 ^ 0)% HASH_SIZE 
-Parameters used: magic number 33, HASH_SIZE.

-The meaning of Hash is: give a string key, convert it to a number, so that the size becomes smaller.    
-Real implementations also need to deal with collision, may require design hash function, etc.


##### Reason for% HASH_SIZE at each step
-hashRst = hashRst * 33 + (int) (key [i]);       
-hashRst = hashRst% HASH_SIZE;       
-The reason is that hashRst will become too big, so it can't be counted and% ...



---

** 110. [Merge Two Sorted Lists.java] (https://github.com/awangdev/LintCode/blob/master/Java/Merge%20Two%20Sorted%20Lists.java) ** Level: Easy Tags: [Linked List]
      

As the title

#### Basics
-Put it small before. Every time than head size
-After the while, connect the endless list in one breath.   
-At the beginning, a node is built to run, and each time node.next = xxx is stored. Save a dummy. Used to return dummy.next.



---

** 111. [Missing Number.java] (https://github.com/awangdev/LintCode/blob/master/Java/Missing%20Number.java) ** Level: Easy Tags: [Array, Bit Manipulation, Math]
      

Give a string of unique numbers, the numbers are taken from [0 ~ n], unordered, find the first skipped number.

#### Swap 
-Much like First Missing Positive, only one line of code is different.
-Swap all numbers to their correct position
-The last for loop finds the misplaced index, which is the missing number.

#### Bit Manipulation
-XOR will only retain bits that are different 1 ^ 0 = 1, but 0 ^ 0, 1 ^ 1 == 0
-Use that feature, XOR all values ​​with index
-The remaining excess numbers are actually the index that cannot be eliminated by XOR, that is, the missing number value.
-Note: The title tells the number is [0 ~ n], but missing a number, then in [0 ~ n-1], the largest number (regardless of whether it is missing) must be n = nums.length.

#### HastSet
-Save all, looking for missing
-O (n) space, unsuitable

#### sorting
-sort, find 1st missing
-O (n log n) is too slow



---

** 112. [Remove Duplicates from Sorted Array.java] (https://github.com/awangdev/LintCode/blob/master/Java/Remove%20Duplicates%20from%20Sorted%20Array.java) ** Level: Easy Tags : [Array, Two Pointers]
      

Give a sorted array and remove the duplicates: that is, paste the non-repeating in order, the extra positions at the end of the array don't matter.

return unique item length.

#### Two Pointers
-sorted array, repeating elements are all together
-Two pointers can actually be a for loop pointer, another dynamic variable.
-track unique index
-skip duplicated items
-O (n)

#### Thinking Mode:
-Remove Duplicate from Array is different from remove from linked list.
-In LinkedList, it is better not to move node.val, and just remove node.
-For the array, it is difficult to remove the node directly, and we cannot use the new array, so we must:
-Put non-repeating elements one by one.
-This idea is similar to merge two sorted array (one of the following very long array can put arr1, arr2).
-Just find an element that will not mess up afterwards, will not move the index, and fill in the elements that meet the conditions. This guarantees in place.
-* Reverse thinking *: remove duplicate, actually find unique elements, and insert into original array



---

** 113. [Remove Duplicates from Sorted List.java] (https://github.com/awangdev/LintCode/blob/master/Java/Remove%20Duplicates%20from%20Sorted%20List.java) ** Level: Easy Tags : [Linked List]
      

Remove duplicate elements from the Linked list, leaving only unique elements.

#### Linked List
-sorted list, duplicate elements are all together
-Know how to build a Linked List.
-If there is a duplicate element at one point: node.val == node.next.val, remove it.
-Run with a dummy node
-Note:
-Node = node.next only if there is no duplication; 
-When there is a repetition, after the third element is brought up, it may still be the same as the current element, so it cannot be moved forward.
-ex: A-> A-> A
-check node and node.next in the while loop are better, so the ending position will be very clear



---

** 114. [Longest Word in Dictionary.java] (https://github.com/awangdev/LintCode/blob/master/Java/Longest%20Word%20in%20Dictionary.java) ** Level: Easy Tags: [Hash Table, Trie]
      

Give the string word [], find the longest Word, meet the conditions: This Word can be built from word [] letter by letter.

If multiple answers, respect smallest lexicographical order.

#### Sort, HashSet
-Sort first, you can see if the partial string already exists after sorting
-Use set.contains (substring (0, n-1)) to see if the substring in the previous step exists
-If found, because it has been sorted alphabetically, the one found must be the most suitable answer in this length.
-Then brutally find the next bigger one.
-Sort O (n log n), O (n) set space

#### Trie
-You can sort words Array first: 1. Long string first; 2. Equal length, sort by dictionary order
-Put all in Trie. Trie.insert ()
-For sorted words array, find Trie.startWith from the longest start.
-Once found, it is in line with the intent, return directly.
-Note: startWith must be isEnd for each node in order to meet the condition of 'spell out letter by letter'.
-Time: build Trie O (mn) + sort: O (nlogn) => O (nlogn)
-Space: O (mn)

#### 
-Sort by size-> compare contains () from the largest-> sort the result in lexicographically.
-But Collections.sort () is twice, and list.contains () is slower




---

** 115. [Path Sum.java] (https://github.com/awangdev/LintCode/blob/master/Java/Path%20Sum.java) ** Level: Easy Tags: [DFS, Tree]
      

Give an inputSum, then dfs, find if there is a path, and the resulting path sum is the same as inputSum.

#### DFS
-Determine the conditions for a good ending: is leaf && val == sum
-Minus node.val for each layer, then dfs.
-Write a note: The effect of root == null => false on parent nodes. It is found that it has no effect, so it can be simplified to use 1 functionDFS.




---

** 116. [Path Sum II.java] (https://github.com/awangdev/LintCode/blob/master/Java/Path%20Sum%20II.java) ** Level: Easy Tags: [Backtracking, DFS, Tree]
      

Give an inputSum, then dfs, find all paths, satisfy: path sum is the same as inputSum.

#### DFS, Backtracking
-Use remaining sum to check if input path sum condition is met
-Add to result list when satisfied
-Two kinds of backtracking:
-1. backtrack the current node, add it to the list, and then dfs. After dfs ends, delete the previously added elements. Very clean.
-2. Backtrack the next increased dfs level value. After dfs return, delete the last element in the list: but delete the remaining value of dfs.
-The first kind of backtrack is better mastered.

#### Previous Notes:
-A basic problem of Binary Tree: find all paths that meet the conditions
-Traverse to the end, compare sum vs. target
-Pay attention to divide. Write the traversal example



---

** 117. [Path Sum III.java] (https://github.com/awangdev/LintCode/blob/master/Java/Path%20Sum%20III.java) ** Level: Easy Tags: [DFS, Double Recursive , Tree]
      

Count all existing path sum == target sum. It can start at any point. But only parent-> child.

#### DFS
-Subtract the given input sum until the sum reaches a target value
-Because it can start from any point, when the sum reaches the standard, it needs to continue to recursive, so as to find all cases (with positive and negative numbers, sum may continue to increase / decrease)
-Classic helper dfs recursive + self recursive
-1. helper dfs recursive handles cases including root
-2. self recursive to lead the situation of skip root.

#### Features
-It is similar to `Binary Tree Longest Consecutive Sequence II` in recursive approach: 
-Use dfs for recursive computation including root
-Use this function yourself, do `recursive computation` that does not include root



---

** 118. [Rotate String.java] (https://github.com/awangdev/LintCode/blob/master/Java/Rotate%20String.java) ** Level: Easy Tags: [String]
      

Give two Strings to see if A rotates into B

#### LeetCode
-Basics
-StringBuffer.deleteCharAt (xx), StringBuffer.append (xx)
-O (n)


#### LintCode
-Different problem: give a char [], rotate offset times.
-* Three steps rotate *
-There is a pit: the offset may be long, so% length is needed to get the part that really needs rotate.
-Note: After rotating a full length, the string is unchanged



---

** 119. [Longest Common Prefix.java] (https://github.com/awangdev/LintCode/blob/master/Java/Longest%20Common%20Prefix.java) ** Level: Easy Tags: [String]
      

Find the longest public prefix in a string.

#### Sort, compare string
-Sort O (nlogn)
-first and last string should share common prefix
-This assumes that the title requires a common prefix for all strings, not some strings

#### Brutle
-Nested loop, each time compares all strings for equality
-Equal, append string. Not equal, return.
-O (mn)



---

** 120. [Reverse Words in a String III.java] (https://github.com/awangdev/LintCode/blob/master/Java/Reverse%20Words%20in%20a%20String%20III.java) ** Level : Easy Tags: [String]
      

Give a String, the Word inside is separated by single space, the purpose is to reverse all Word, but preserve Word and space order.

#### Reverse function
-Downgrade of Reverse Words in a String II, just remove the first overall reverse



---

** 121. [Merge Sorted Array II.java] (https://github.com/awangdev/LintCode/blob/master/Java/Merge%20Sorted%20Array%20II.java) ** Level: Easy Tags: [Array ]
      

As the title, merge two sorted array into new sorted array

-Length is fixed. Basic Implementation
-If an array is large enough, merge into this array, then merge from the end.



---

** 122. [Nth to Last Node in List.java] (https://github.com/awangdev/LintCode/blob/master/Java/Nth%20to%20Last%20Node%20in%20List.java) ** Level : Easy Tags: [Linked List]
      

#### Linked List
-Find nth node first
-Then head started running
-node to the end, and head ~ node is exactly n distance away. So head is the last nth



---

** 123. [Two Sum.java] (https://github.com/awangdev/LintCode/blob/master/Java/Two%20Sum.java) ** Level: Easy Tags: [Array, Hash Table]
      

#### HashMap <value, index>
-Relatively violent and concise: find a value, store an index
-If the result is matched in the HashMap, the index stored in the HashMap is returned. 
-O (n) space && time.

#### Sort array, two pointer
-Before and after ++, --Search. Sort takes O (nlogn).     
-1. The first two pointers look for value.       
-2. Note that you must use the extra space to reserve the original array and use it to find the index. (HashMap cannot be used here because the value is used as the key, but the value may be duplicated)      
-O (n) space, O (nlogn) time.    




---

** 124. [Max Area of ​​Island.java] (https://github.com/awangdev/LintCode/blob/master/Java/Max%20Area%20of%20Island.java) ** Level: Easy Tags: [Array , DFS]
      

#### DFS
-Although Easy, the basic idea of ​​DFS is used.
-1. dive deep
-2. mark VISITED
-3.sum it up
-Time: worst O (mn), traverse all possible nodes

-Pay more attention to starting dfs from the place where the value == 1 is met.
-For situations where there is no island, area should be 0, not Integer.MIN_VALUE. Ask the examiner's guy, don't write it down.



---

** 125. [Subarray Sum.java] (https://github.com/awangdev/LintCode/blob/master/Java/Subarray%20Sum.java) ** Level: Easy Tags: [Array, Hash Table, PreSum, Subarray]
      
time: O (n)
space: O (n)

To a string of numbers, to find a subarray therein [start, end] index, condition: subarary sum == 0.

#### Hash Table
-Simple version of `subarray sum equals k`: k = 0
-Find preSum, then keep checking `map.containsKey (preSum-k)`. 
-If `priorSum = preSum-k == 0`, it means that [priorSum.index + 1, curr index] is the paragraph we are looking for

#### Previous notes, same preSum + map solution
-Analyze that if sum [0 ~ a] = x, then sum [0 ~ b] = x, then sum [a + 1 ~ b] == 0
-Use hashMap to store the value of each sum [0 ~ i] and index i. If there are duplicates, find a set of sum 0 arrays.



---

** 126. [Range Sum Query-Immutable.java] (https://github.com/awangdev/LintCode/blob/master/Java/Range%20Sum%20Query%20-%20Immutable.java) ** Level: Easy Tags: [DP, PreSum]
      

Given a string of numbers, find sumRange.

#### PreSum
-Is the definition of pre sum
-preSum is also the simplest form of dp [].
-dp [i], preSum [i]: the sum of the first (i-1) elements.



---

** 127. [Longest Words.java] (https://github.com/awangdev/LintCode/blob/master/Java/Longest%20Words.java) ** Level: Easy Tags: [Hash Table, String]
      

Give a string of Strings, find the longest length, and return the longest Strings all

#### Hash Table
-<Integer, List <String >>
-Store the longest value, and finally map.get (max) 



---

** 128. [Unique Characters.java] (https://github.com/awangdev/LintCode/blob/master/Java/Unique%20Characters.java) ** Level: Easy Tags: [Array, String]
      

determine if characters are unique in string

#### HashSet
-space O (n), time O (n)

#### char []
-space O (n), time O (nlogn)

#### no additional data structure
-double for loop: O (n ^ 2)




---

** 129. [Binary Gap.java] (https://github.com/awangdev/LintCode/blob/master/Java/Binary%20Gap.java) ** Level: Easy Tags: [Bit Manipulation]
      
time: O (n), n = # of bits
space: O (1)

#### Bit Manipulation
-Understand the description of Binary Gap
-Simple `>>`, `& 1`, track start and end point just fine



---

** 130. [Maximize Distance to Closest Person.java] (https://github.com/awangdev/LintCode/blob/master/Java/Maximize%20Distance%20to%20Closest%20Person.java) ** Level: Easy Tags : [Array]
      
time: O (n)
space: O (1)

For a row of seats, sit alone: ​​find the farthest place (middle point) from the people on both sides, return the maximum distance from the person next to you

It's the same concept of Exam Room, to simplify the problem: just consider one person here.

####? Basic Implementation, track start / end
-start / end point, then compare size records dist
-Note 1: If there is no one in the first seat, special treatment, dist = [0 ~ end]
-Note 2:? If there is no one in the last seat, special treatment: dist = [n-1-start];
-The rest: `dist = Math.max (dist, (end-start) / 2)`
-Related topics: Almost the same concept `Binary Gap`, upgrade complex version` Exam Room`




---

** 131. [Paint Fence.java] (https://github.com/awangdev/LintCode/blob/master/Java/Paint%20Fence.java) ** Level: Easy Tags: [DP, Sequence DP]
      
time: O (n)
space: O (n)

#### DP
-Up to 2 fences with the same color
-Assuming that i is different from i-1, the result is (k-1) * dp [i-1]
-Assuming i is the same as i-1, then depending on the conditions, i-1 and i-2 must be different. Then all the results are (k-1) * dp [i-2]
-dp [i]: count # of ways to paint
-Principle of addition
-time, space: O (n)
-rolling array: space O (1)

#### Previous Notes
-This topic is very interesting. The analysis was too complicated at the beginning, and finally I followed the idea of ​​this buddy (http://yuanhsh.iteye.com/blog/2219891), but it was much simpler.
-The method of setting T (n) is the same as the Fibonacci number after simplification. The detailed analysis is as follows.
-After finishing, I still feel like a god. It was an Easy question, but I couldn't think of it.




---

** 132. [Best Time to Buy and Sell Stock.java] (https://github.com/awangdev/LintCode/blob/master/Java/Best%20Time%20to%20Buy%20and%20Sell%20Stock.java) ** Level: Easy Tags: [Array, DP, Sequence DP]
      

Give an array of stock prices, limit one round of trading (buy / buy), and ask how to find the maximum profit.

#### Understanding meaning is key
-The price is traded every day. Only buy and sell once in n days, then find the lowest price to buy and the highest price to sell.
-Record daily minimum value of Min. O (n)
-Buy and sell with Min every day, how much profit?

#### DP
-Find min value for first i items, new dp [n + 1].
-dp [i]: What is the minimum price for the previous i days: min cost of first i days
-Then use the price of the day to subtract dp [i] to calculate max profit.
-Time, Space: O (n)
-Further, use min to represent min [i], because only the current min is needed in the calculation.

#### Rolling array
-index i only depend on [i-2]
-Space O (n)

#### Brutle Failed
-Try to buy every day, then try to sell every day thereafter. Double for loop, O (n ^ 2). Timeout.
-Many of them are unnecessary calculations: [7, 1, 5, 3, 6, 4]. if we know buyin with 1 is cheapest, we don't need to buyin at 5, 3, 6, 4 later on; we'll only sell on higher prices.



---

** 133. [Best Time to Buy and Sell Stock II.java] (https://github.com/awangdev/LintCode/blob/master/Java/Best%20Time%20to%20Buy%20and%20Sell%20Stock%20II .java) ** Level: Easy Tags: [Array, DP, Greedy, Sequence DP, Status DP]
      
time: O (n)
space: O (1) greedy, O (n) dp

Difference from Stock I: You can buy and sell multiple times, and find the maximum profit of the sum.

#### Several other different ideas:
-Greedy, every time there are adjacent diffs that meet the profit criteria, they are sold, and finally all the diffs are added together. Calculating the delta is actually simple and rude, which is not bad.
-See below, find peek from the trough, sell.
-DP. (Old dp solution BuyOn [], SellOn [])
-DFS calculates all (timeout). Improvement on DFS-> DP-> calculate sellOn [i] and buyOn [i], and then return buyOn [i]. It is a bit hard to imagine, but the code is simple and O (n)

#### Greedy
-Draw, because you can buy and sell indefinitely, as long as there is a rise, there will be profit
-All the sales, the translations add up, which is actually overall best profit
-O (n)

#### Find the range with the largest increase, buy and sell:
-Find the trough and buy: when peek = start + 1, you take a step forward each time; if there is no upward trend, continue to the trough.
-Rise to the peak and sell: Once there is an upward trend, enter a while loop, go to the end, and add a profit.
-profit + = prices [peek-1]-prices [start]; quite special.
-When there is no uptrend, peek-1 is also start, so here is exactly profit + = 0.

#### DP, sequence dp + status
-Want to know the maximum profit of the previous i day, then use sequence DP: 
-dp [i]: represents the maximum profit for the previous i days
-Whether the day can be sold depends on whether it was bought yesterday, that is, the state of yesterday's purchase or sale: plus state, dp [i] [0], dp [i] [1]
-The status of `buying` dp [i] [0]` = 1. Buy today, dp [i-1] [1] sold yesterday-result [price] i; 2. Do not buy today, as yesterday Buy status dp [i-1] [0] and compare results.
-The status of `selling` dp [i] [1]` = 1. sold today, dp [i-1] [0] result bought yesterday + price [i]; 2. not sold today, compared with yesterday Comparison of sold status dp [i-1] [1].
-Note init: 
-dp [0] [0] = dp [0] [1] = 0; // 0 days, 
-dp [1] [0] = 0; // sell on 1st day, haven't bought, so just 0 profit.
-dp [1] [0] = -prices [0]; // buy on 1st day, with cost of prices [0]

##### Rolling Array
-[i] is associated with [i-1], roll




---

** 134. [Minimum Subarray.java] (https://github.com/awangdev/LintCode/blob/master/Java/Minimum%20Subarray.java) ** Level: Easy Tags: [Array, DP, Greedy, Sequence DP, Subarray]
      
time: O (m)
space: O (1)

Give a list of arrays, unsorted, can have negative / positive num. Find the minimum of the sum of the numbers in the subarray in the middle of the array

#### DP
-See min value, at least consider dp:
-Consider last num: min sum will be (preMinSum + curr, or curr)
-Use preMinSum to cache previouly calcualted min sum, also compare with + curr.
-Have a global min to track: because the preMinSum can be dis-continuous. 
-Can also be written as dp [i] but not necessary



---

** 135. [Subtree of Another Tree.java] (https://github.com/awangdev/LintCode/blob/master/Java/Subtree%20of%20Another%20Tree.java) ** Level: Easy Tags: [DFS , Divide and Conquer, Tree]
      

#### Tree 
-Traverse tree: left, right
-Concept of partial compare vs. whole compare



---

** 136. [Two Sum IV-Input is a BST.java] (https://github.com/awangdev/LintCode/blob/master/Java/Two%20Sum%20IV%20-%20Input%20is%20a% 20BST.java) ** Level: Easy Tags: [Tree]
      

HashSet to store visited items. Same old 2 sum trick.



---

** 137. [Read N Characters Given Read4.java] (https://github.com/awangdev/LintCode/blob/master/Java/Read%20N%20Characters%20Given%20Read4.java) ** Level: Easy Tags : [Enumeration, String]
      

Read4 title. Understanding title: There is an input object buff, which will be populated with data.

#### String in char [] format
-Understanding the topic: Actually it is track `How many bytes can be read by read4 () response`
-Another useful function `System.arraycopy (src, srcIndex, dest, destIndex, length)`



---

** 138. [Merge Sorted Array.java] (https://github.com/awangdev/LintCode/blob/master/Java/Merge%20Sorted%20Array.java) ** Level: Easy Tags: [Array, Two Pointers ]
      

Give two sorted arrays, merge. One of the arrays nums1 has extra positions

#### Basics
-A is long enough, then you can add new elements from the end of A.     
-Note that from the end, the large number comes first.  



---

** 139. [Valid Palindrome II.java] (https://github.com/awangdev/LintCode/blob/master/Java/Valid%20Palindrome%20II.java) ** Level: Easy Tags: [String]
      

#### Palindrome String
-delete an index = jump over the index
-Note that boolean chance can use a helper function



---

** 140. [Moving Average from Data Stream.java] (https://github.com/awangdev/LintCode/blob/master/Java/Moving%20Average%20from%20Data%20Stream.java) ** Level: Easy Tags : [Design, Queue, Sliding Window]
      

Give an interface, design a structure, and be able to calculate the moving window average.

#### Queue
-Understand the problem, pay attention to the handling of average and window.
-Simple queue.size () comparison



---

** 141. [Move Zeroes.java] (https://github.com/awangdev/LintCode/blob/master/Java/Move%20Zeroes.java) ** Level: Easy Tags: [Array, Two Pointers]
      

Move non-zero elements to front of array; preseve order.

#### Two Pointers
-Outside pointer that moves in certain condition. 
-Save appropirate elements



---

** 142. [Flood Fill.java] (https://github.com/awangdev/LintCode/blob/master/Java/Flood%20Fill.java) ** Level: Easy Tags: [DFS]
      

Same as MS Paint

#### DFS 
-track `boolean [] [] visited`, validate before dfs



---

** 143. [Diameter of Binary Tree.java] (https://github.com/awangdev/LintCode/blob/master/Java/Diameter%20of%20Binary%20Tree.java) ** Level: Easy Tags: [Tree ]
      

Find longest path (include or not include root)

Same idea as Binary Tree Maximum Path Sum: handle single path, or combined path (do not include curr root)

#### Singlepath, combined path
-`int [] {combinedPath, singlePath}`;
-pick single path + 1: `singlePath = Math.max (left [1], right [1]) + 1`;
-complete left / right child, or join curr root: `combinedPath = Math.max (Math.max (left [0], right [0]), left [1] + right [1] + 1)`;



---

** 144. [Backspace String Compare.java] (https://github.com/awangdev/LintCode/blob/master/Java/Backspace%20String%20Compare.java) ** Level: Easy Tags: [Stack, Two Pointers ]
      



---

** 145. [Roman to Integer.java] (https://github.com/awangdev/LintCode/blob/master/Java/Roman%20to%20Integer.java) ** Level: Easy Tags: [Math, String]
      

#### String 
-Familiar with Roman alphabet rules     
-1. 'IVXLCDM' numbers     
-2. To enumerate the case of combo, you need to subtract the extra part from the original sum: 'IV, IX' minus 2, 'XL, XC' minus 20, and 'CD, CM' minus 200. 
-Leading `I (1 * 2)`, `X (10 * 2)`, `C (100 * 2)` causes double counting 

https://en.wikipedia.org/wiki/Roman_numerals



---

** 146. [Intersection of Two Arrays.java] (https://github.com/awangdev/LintCode/blob/master/Java/Intersection%20of%20Two%20Arrays.java) ** Level: Easy Tags: [Binary Search, Hash Table, Sort, Two Pointers]
      

-Method 1: Use hashset to find unique && duplicate: O (m + n)
-Method 2: You can use binary search to find numbers. Note: binary search must require array sorted: nLog (m)



---

** 147. [Strobogrammatic Number.java] (https://github.com/awangdev/LintCode/blob/master/Java/Strobogrammatic%20Number.java) ** Level: Easy Tags: [Enumeration, Hash Table, Math]
      

Enumerate according to the topic, and then follow the basic implementation rules

#### Alter input

#### HashTable + Two Pointer



---

** 148. [Valid Parentheses.java] (https://github.com/awangdev/LintCode/blob/master/Java/Valid%20Parentheses.java) ** Level: Easy Tags: [Stack, String]
      

Peeling process. The trouble should end it   
The outer skin '{[' at the bottom of the stack   
The right skin should correspond to the left skin on the top of the stack. 



---

** 149. [First Unique Character in a String.java] (https://github.com/awangdev/LintCode/blob/master/Java/First%20Unique%20Character%20in%20a%20String.java) ** Level : Easy Tags: [Hash Table, String]
      

Method 1: According to the meaning of the title, find the first letter of first index == last index.

Method 2: Use a hashmap to store the index of the letter, and the index of some duplicate letters will be a list. Find a single index, combine into a list, sort, return list.get (0)



---

** 150. [Add Binary.java] (https://github.com/awangdev/LintCode/blob/master/Java/Add%20Binary.java) ** Level: Easy Tags: [Math, String, Two Pointers]
      

#### Two pointers
-Use two pointers i, j to track the 2 strings
-Add when i and j are applicable. While (i> = 0 || j> = 0)
-StringBuffer.insert (0, x);
-handle carry

#### wrong: convert to int
-Native method is not technical, replace binary with numbers, add them up, and then use binary
-If the input is large, it is likely that both int and long cannot be held. Not insurance.



---

** 151. [Isomorphic Strings.java] (https://github.com/awangdev/LintCode/blob/master/Java/Isomorphic%20Strings.java) ** Level: Easy Tags: [Hash Table]
      

#### HashMap
-two failture cases:
-same key, value not matching
-two key maps to same value

#### Previous note
1. Match. Is map.containsKey, map.containsValue, and char1 == char2. Perfect.
2. Either Key not exist, or Value not exit. False;
3. Both key and Value exist, but map.get (char1)! = Char2. Miss-match. False.
4. None of Key or Value exist in HashMap. Then add the match.



---

** 152. [Next Greater Element I.java] (https://github.com/awangdev/LintCode/blob/master/Java/Next%20Greater%20Element%20I.java) ** Level: Easy Tags: [Hash Table, Stack]
      

#### stack?



---




 
 
 
## Medium (247)
** 0. [Evaluate Division.java] (https://github.com/awangdev/LintCode/blob/master/Java/Evaluate%20Division.java) ** Level: Medium Tags: [BFS, DFS, Graph, Union Find]
      

#### DFS
-build map of `x # y-> val` to store values ​​[i] and 1 / values ​​[i]
-build map of `x-> list children`
-dfs to traverse the graph

#### BFS
-BFS should also work: build graph and valueMap
-for each starting item, add all next candidate to queue
-mark visited, loop until end item is found



---

** 1. [Fraction to Recurring Decimal.java] (https://github.com/awangdev/LintCode/blob/master/Java/Fraction%20to%20Recurring%20Decimal.java) ** Level: Medium Tags: [Hash Table, Math]
      

TODO: no need of hashMap, just use set to store the existing

It is not difficult to think of dealing with division: consider positive and negative, consider before and after the decimal point. Mainly after the decimal point, we must focus on consideration.
It's easy to overlook the benefits of integer.


---

** 2. [Gray Code.java] (https://github.com/awangdev/LintCode/blob/master/Java/Gray%20Code.java) ** Level: Medium Tags: [Backtracking]
      

TODO:
1. backtracking, using set to perform contains ()
2. BFS: use queue to keep the mutations

The title egg hurts and currently only accepts one result.

BackTracking + DFS:   
   Recursive helper flips each time oneself / left / right. After Flip, it should be restored as it is. Iterate through all.

Used (not carefully verified):   
The basic idea is to start from one point and go in one direction, flip a bit every time, and go back when you hit a wall.



---

** 3. [Majority Number II.java] (https://github.com/awangdev/LintCode/blob/master/Java/Majority%20Number%20II.java) ** Level: Medium Tags: [Enumeration, Greedy]
      

#### Array
-Divided in three: abc consideration
-If a: countA ++; or b: countB ++
-Or c: countA--, countB--
-Note: In the order of the if statement, valA && countA has priority over valB && countB
-The last two a and b with count> 0 are naturally greater than 1/3. One of them is greater than 1/3.
-Compare whichever countA and countB are large, then return which one.



---

** 4. [Majority Number III.java] (https://github.com/awangdev/LintCode/blob/master/Java/Majority%20Number%20III.java) ** Level: Medium Tags: [Hash Table, Linked List]
      

TODO: 
1. hash table solution not passing
2. Find O (n) solution

#### Hash Table
-Same as other Majority Numbers.
-If the number of occurrences is more than 1 / k, divide into k count occurrences. Use HashMap. Existing +1; if it does not exist in the map, it is divided into cases:    
-If map.size () == k, it means that the dates are full, and all existing ones should be -1 in the map
-If map.size () <k, indicating that the new candidate is to be added, then map.put (xxx, 1);
-Finally, find out the number of the highest leftance in the HashMap.
-But such worst case is O (nk)



---

** 5. [Minimum Height Trees.java] (https://github.com/awangdev/LintCode/blob/master/Java/Minimum%20Height%20Trees.java) ** Level: Medium Tags: [BFS, Graph]
      

#### Graph + BFS
-Build graph `map <node, list of node>`
-BFS to find the shortest path: when the neibhbor has the curr node as the only one neighbor, it is leaf.
-record shortest path in Map <Integer, List <Integer >> as result
-TODO: code it up.

#### Previous Solution
-removing leaf && edge



---

** 6. [Missing Ranges.java] (https://github.com/awangdev/LintCode/blob/master/Java/Missing%20Ranges.java) ** Level: Medium Tags: [Array]
      

#### Basic Implementation
-O (n)
-Two pointers, calculating the part between prev and curr each time.
-Then prev = curr, move forward one space
-TODO: check the edge case and make sure max / min of int are checked



---

** 7. [Next Permutation.java] (https://github.com/awangdev/LintCode/blob/master/Java/Next%20Permutation.java) ** Level: Medium Tags: [Array]
      

Need to consider: why reverse is need? Why we are looking for k?

Permutation's law:     
1. Change from small numbers because all recursive traversal starts from small numbers.    
2. Because of the rule of 1, find a large number of breakpoints from the end: Make sure that the permutation after swap is still the smallest when the prefix is ​​fixed.    

steps:    
Find the last rising point, k      
2. From back to front, find the first point larger than k, bigIndex      
3. swap k && bigIndex     
4. The last reversal (k + 1, end)      




---

** 8. [Palindrome Permutation II.java] (https://github.com/awangdev/LintCode/blob/master/Java/Palindrome%20Permutation%20II.java) ** Level: Medium Tags: [Backtracking, Permutation]
      

TODO: need to review permutation

Comprehensive question of permutation:    
1. Can validate input do Palindromic Permutation. This is (Palindrome Permutation I)   
2. By the way, save the first half of the permutation string and the single character (if any) in the middle.    
3. DFS does unique permutation: given input has duplicate characters.       



---

** 9. [Permutation Sequence.java] (https://github.com/awangdev/LintCode/blob/master/Java/Permutation%20Sequence.java) ** Level: Medium Tags: [Backtracking, Math]
      

TODO: what about regular DFS / backtracking to compute the kth? Dfs (rst, list, candiate list, k)

k is a number of permutation. And permutation is regular.

That is, you can determine the character of each digit according to the size of k (starting from the largest digit, because the default factorio changes from the largest digit).

So first find n !, then k / n! Can calculate the current digit character. Then reduce factorio and k, respectively.

In addition, use a boolean [] visited to ensure that each number appears only once.

This method is much more efficient than calculating each permutation.




---

** 10. [Product of Array Exclude Itself.java] (https://github.com/awangdev/LintCode/blob/master/Java/Product%20of%20Array%20Exclude%20Itself.java) ** Level: Medium Tags : [Array]
      




---

** 11. [Remove Duplicates from Unsorted List.java] (https://github.com/awangdev/LintCode/blob/master/Java/Remove%20Duplicates%20from%20Unsorted%20List.java) ** Level: Medium Tags : [Linked List]
      

Basic method: O (n) sapce, time
Iterate.
Encountered duplicate (maybe multiple), while until node.next is not duplicate.
Next, since it is not duplicate, add to set


If you don't use extra memory, do it in place:
Then sort linked list. Use merge sort.

Review merge sort:
1. find middle.
2.recursively: right = sort (mid.next); left = sort (head).
3. within sort (), at the end call merge (left, right)


---

** 12. [Rotate Image.java] (https://github.com/awangdev/LintCode/blob/master/Java/Rotate%20Image.java) ** Level: Medium Tags: [Array, Enumeration]
      

#### Find formulas
-Find a regular formula for the rotation angle: r = c; c = (w-r)
-Use temp variable, swap in place.



---

** 13. [Search in Rotated Sorted Array II.java] (https://github.com/awangdev/LintCode/blob/master/Java/Search%20in%20Rotated%20Sorted%20Array%20II.java) ** Level : Medium Tags: [Array, Binary Search]
      

After Allow duplicates:
Because the final binary search result is also O (n)
So remember this question: Since it is O (n), then a simple for loop is just fine.

Of course, talk to the interviewer about the reason. Don't come up with only for. . .


---

** 14. [Single Number II.java] (https://github.com/awangdev/LintCode/blob/master/Java/Single%20Number%20II.java) ** Level: Medium Tags: [Bit Manipulation]
      

In a string of numbers, all numbers are repeated three times, except for one number. Find this number, linear time, without extrace space (constant space)

TODO: bits



---

** 15. [Single Number III.java] (https://github.com/awangdev/LintCode/blob/master/Java/Single%20Number%20III.java) ** Level: Medium Tags: [Bit Manipulation]
      

TODO: wut?


---

** 16. [Space Replacement.java] (https://github.com/awangdev/LintCode/blob/master/Java/Space%20Replacement.java) ** Level: Medium Tags: [String]
      



---

** 17. [Stone Game.java] (https://github.com/awangdev/LintCode/blob/master/Java/Stone%20Game.java) ** Level: Medium Tags: [DP]
      

This DP is a bit weird. Need to consider.
NOT DONE YET


---

** 18. [The Smallest Difference.java] (https://github.com/awangdev/LintCode/blob/master/Java/The%20Smallest%20Difference.java) ** Level: Medium Tags: [Array, Sort, Two Pointers]
      



---

** 19. [Total Occurrence of Target.java] (https://github.com/awangdev/LintCode/blob/master/Java/Total%20Occurrence%20of%20Target.java) ** Level: Medium Tags: []
      
The idea is simple. It's a bit long to write.
Find total number of occurance. First find first occurance, then last occurance.



---

** 20. [Two Lists Sum.java] (https://github.com/awangdev/LintCode/blob/master/Java/Two%20Lists%20Sum.java) ** Level: Medium Tags: [Linked List]
      

Give two Linked lists, sum up and synthesize new lists



---

** 21. [Zigzag Iterator.java] (https://github.com/awangdev/LintCode/blob/master/Java/Zigzag%20Iterator.java) ** Level: Medium Tags: [BST]
      

This topic is relatively simple. When I do it, I first think about what to do with k. Then use a map to index and each listmark.
Every time next (), the corresponding list head is removed.
Then I ran in circles, swiping a list head each time. Not difficult. Just maintain a few variables clearly.


---

** 22. [Encode and Decode TinyURL.java] (https://github.com/awangdev/LintCode/blob/master/Java/Encode%20and%20Decode%20TinyURL.java) ** Level: Medium Tags: [Hash Table, Math]
      

In fact, I think of the entry point, which is a difficult and easy problem. The encode here is to find a way to save the URL, and then give a key.
So how to make this key, simply use a map, and then count. For more complicated, you can make a random letter / number to form the key.



---

** 23. [Wiggle Sort.java] (https://github.com/awangdev/LintCode/blob/master/Java/Wiggle%20Sort.java) ** Level: Medium Tags: [Array, Sort]
      

method 1:
Sort, nLog (n). Then change the straight uphill into cascading mountain peaks, you need to make a swap every few (every 2 digits in the title) to cause unevenness.
Note: There is no relationship between every other peak, so just worry about [i], [i-1] two positions every time.

Method 2:
O (n)
Look at the rule of curious numbers and even digits, and then run it again according to the rule given by the question, focusing on only two positions at a time: just swap the inappropriate [i], [i-1] positions.

Method 3:
Same as Law 2, but just a little more subtle:
Think too much the first time. In fact, a fall-through can solve the problem, because:
This fall-through cares about two elements at a time and can be done in one go, regardless of the previous elements.
A special point: flags control clever changes in the peaks and valleys. Another magical scene!
Such a spectacle, you must know it when you have seen it. When you haven't seen it, you are a little scratched.



---

** 24. [Queue Reconstruction by Height.java] (https://github.com/awangdev/LintCode/blob/master/Java/Queue%20Reconstruction%20by%20Height.java) ** Level: Medium Tags: [Greedy ]
      

There is nothing else but to write the example once, find the rules, and then greedy. 
You need to write the rules you found, such as: starting from h large, and putting k small first. Pay attention to the correctness when writing the comparator.
If you want to sort, and flexible insert: use arrayList. Make an object yourself.
Finally, do the 'matchCount' where the thinking is clear, find the most correct spot, and then greedy insert.

O (n) space, O (nLog (n)) time, because of sorting.

There may be room for simplification, and the code is a bit too long.
For example, try it without extra space?



---

** 25. [Two Sum II-Input array is sorted.java] (https://github.com/awangdev/LintCode/blob/master/Java/Two%20Sum%20II%20-%20Input%20array%20is% 20sorted.java) ** Level: Medium Tags: [Array, Binary Search, Two Pointers]
      

Ascending array, find 2SUM.

#### Two pointers
-Sorted array. Two pointer move start and end, check sum.
-Note that sum uses long.
-O (n) time

#### Binary Search, because it's already sorted
-Hold down a valueA, then find (target-valueB) in the remaining binary serach
-for loop O (n), binary search O (logn)
-overall time: O (nLogN), don't write



---

** 26. [2 Sum II.java] (https://github.com/awangdev/LintCode/blob/master/Java/2%20Sum%20II.java) ** Level: Medium Tags: [Array, Binary Search , Two Pointers]
      

Similar to 2sum II-input array is sorted. Both are sort array, then two pointers.

Question from LintCode. Note that you are looking for greater / bigger than target.

O (nLogn) is allowed due to given conditions:   
   sort
   two pointer

while two pointers move inside. Every time if num [left] + num [right]> target, then all num [left ++] plus num [right]> target.   
That is, num [right] does not move, and calculates how many groups can be added to move left, that is: right-left so many. Add all to count.     
Then right--. Change the right to compare it with the previous left part.



---

** 27. [Coin Change.java] (https://github.com/awangdev/LintCode/blob/master/Java/Coin%20Change.java) ** Level: Medium Tags: [Backpack DP, DP, Memoization]
      

Give a bunch of coins with different amounts, and total amount to spent. Find the minimum number of coins that can be combined into this amount. There is no limit to the number of each coin.

#### DP
-Find the right equation dp [x], how many coins are needed to accumulate amount x: #coin is value, and index is [0 ~ x].
-The relationship of the sub-question is: If a coin is used, then it should be #coins + 1 in the position of f [x-coinValue]

##### initialization
-To handle the boundary, at the beginning of 0index, use value0. 
-Integer.MAX_VALUE is used for comparison, initialize dp [x]
-Note that once Integer.MAX_VALUE + 1 will become negative. This will happen when coin = 0.

##### Optimization
-Method 1: Use Integer.MAX_VALUE directly
-Method 2: Use -1, a little more concise, compare dp [i] and dp [i-coin] + 1 each time, then save. It is not necessary to do multiple min comparisons.

#### Memoization
-dp [i] still says: min # of coints to make amount i
-initialize dp [i] = Integer.MAX_VALUE
-First select the last step (traversing coins), then dfs does the same
-Record dp [amount] If value has already been given, do not repeat the calculation and return directly.
-But there is no need to force memoization on this problem. The state and equation of ordinary DP are relatively easy to find.



---

** 28. [Maximum Product Subarray.java] (https://github.com/awangdev/LintCode/blob/master/Java/Maximum%20Product%20Subarray.java) ** Level: Medium Tags: [Array, DP, Subarray]
      

Find a series of continuous subsequences from a set of numbers (both positive and negative), and reach the maximum product product.

#### DP
-Find the best value, think of DP. Time / Space O (n)
-Two special places: 
-1. For positive and negative numbers, two DP arrays are required. 
-2. continuous prodct This condition determines when Math.min, Math.max, 
-It is compared with the current value of nums [x]. If the current value is more suitable, the previous continuous product will be discarded and restarted.
-This is destined to require a global variable to hold the result.

#### Space optimization, rolling array
-The index i in maxProduct && minProduct can only be related to i-1, so redundant operatoins can be omitted.
-Time: O (n), space: O (1)



---

** 29. [3 Sum Closest.java] (https://github.com/awangdev/LintCode/blob/master/Java/3%20Sum%20Closest.java) ** Level: Medium Tags: [Array, Two Pointers ]
      

A simple form of 3Sum, and does not find index, value, but just a sum.

double for loop. 2Sum can only use left / right 2 pointers. O (n ^ 2)

Note: use long when checking closest to avoid int being used



---

** 30. [Triangle Count.java] (https://github.com/awangdev/LintCode/blob/master/Java/Triangle%20Count.java) ** Level: Medium Tags: [Array]
      

In fact, it is the deformation of 3sum, or the deformation of 2sum. It is mainly done with 2 pointers.
Note that when selecting the index, set a [0 ~ i] one at a time, find the start, end, and i in the triangle.
Note smartly:
Among them, if a start / end / i match, then from this [start ~ end], anything larger than start is fine, so we count + = end-start.
On the other hand, other indexes of <end may not meet nums [start] + nums [end]> nums [i]



---

** 31. [3Sum.java] (https://github.com/awangdev/LintCode/blob/master/Java/3Sum.java) ** Level: Medium Tags: [Array, Two Pointers]
      


#### sort array, for loop + two pointer. O (n ^ 2)
-Handling duplicate wthin triplets: 
-If the outermost moving point i is repeated, it will be used until the last one at the end.
-If there are duplicates in the triplet, use the start point and move to the end.

Previous notes:
note:   
   1. Find value triplets, multiple results. Note that you are not looking for index.    
   2. For ascending order, the first layer of for loop is started from the last element, ensuring the order.    
   3. Remove the same numbers used by duplicate: check, all skipped. You don't need to calculate the same result with the same number.

step:   
   1. For loop pick a number A.    
   2. 2Sum results in a bunch of 2 numbers    
   3. Cross match Step A in step 1.   

Time O (n ^ 2), two nested loops

In addition, you can still use HashMap to do 2Sum. Slightly shorter. Still pay attention to handle duplicates.




---

** 32. [Unique Binary Search Tree.java] (https://github.com/awangdev/LintCode/blob/master/Java/Unique%20Binary%20Search%20Tree.java) ** Level: Medium Tags: [BST , DP, Tree]
      

Not quite clear.
The principle is summarized according to the left and right splits.Each split, there will be a certain amount of permutation on the left and right sides.Of course, the total number of cases is multiplied.
Then add each different split point:
f (n) = f (0) * f (n-1) + f (1) * f (n-2) + ... + f (n-2) * f (1) + f (n-1 ) * f (0)

Then convert the mathematical formula into the DP equation, which is a bit metaphysical! It's hard to think.



---

** 33. [Unique Paths II.java] (https://github.com/awangdev/LintCode/blob/master/Java/Unique%20Paths%20II.java) ** Level: Medium Tags: [Array, Coordinate DP , DP]
      

Like the grid of the unique path, the target goes to the bottom right corner, but there may be obstacles in the grid, which cannot be crossed. Find the count of the unique path.

#### Coordinate DP
-dp [i] [j]: # of paths to reach grid [i] [j]
-dp [i] [j] = dp [i-1] [j] + dp [i] [j-1];
-Consider the state needed at the end: how to compose and write the formula.
-In the formula, pay attention to the blocks that can be skipped, marked as 1. 'Unable to reach', which is 0 path in dp [i] [j].



---

** 34. [Bomb Enemy.java] (https://github.com/awangdev/LintCode/blob/master/Java/Bomb%20Enemy.java) ** Level: Medium Tags: [Coordinate DP, DP]
      

2D grid, each grid may be 'W' wall, 'E' enemy, or '0' empty.

A bomb can be blown in 4 directions. Find out how many enemies can be blown up on the grid.

#### Corrdinate DP
-Space, Time: O (MN)
-dp [i] [j] is the maximum amount of enemy on (i, j)
-dp [i] [j] needs to be added from 4 directions, that is, it has to go through 4 directions, so it is divided into UP / Down / Left / Right 4 int [] []
-Find max in the last step
-The method of considering directions is easy to think of, but the code for moving in four directions is tedious.
-Fry up: Think from top to bottom
-Fry Down: Think Bottom Up
-Skilled in writing 2D array index transformations.

There seems to be a more concise method, using a col count array: http://www.cnblogs.com/grandyang/p/5599289.html



---

** 35. [3Sum Smaller.java] (https://github.com/awangdev/LintCode/blob/master/Java/3Sum%20Smaller.java) ** Level: Medium Tags: [Array, Two Pointers]
      

The general O (n3) is definitely not working. Optimize on this basis.
When j, k is satisfied, (k-j) is all the cases where sum <target.
And once> target, because j can not go back, only k--, then the problem is locked. This can be done O (n2)



---

** 36. [Update Bits.java] (https://github.com/awangdev/LintCode/blob/master/Java/Update%20Bits.java) ** Level: Medium Tags: [Bit Manipulation]
      

Some tricks familiar with bits:
-~ 0 = -1 = 111111 ... 11111111 (32-bit)
-Create mask by shifting right >>>, and shifting left
-Reverse to get 0000 ... 11110000 format mask
-& 0000 = clean up; | ABC = assign ABC



---

** 37. [Maximum XOR of Two Numbers in an Array.java] (https://github.com/awangdev/LintCode/blob/master/Java/Maximum%20XOR%20of%20Two%20Numbers%20in%20an%20Array .java) ** Level: Medium Tags: [Bit Manipulation, Trie]
      

More difficult to think of. Using the XOR property A ^ B = C, then A = B ^ C.
1. Enumerate the possible A, 2. Then guess one by one.

1. Enumeration A: Because MAX must be the number with the largest leading-1, then the enumeration A starts from (1000000 ... 000), 
Take 1 or 0 for one more bit at a time
2. Because A is enumerated according to each bit, then B and C must also appear with the same digits.
Here, B and C have become the form of prefix and placed in the set. 
Similar to the idea of ​​2sum using hashmap, each time using the enumerated A ^ B = C to see if the result C is already in the set. 
If at, it is proved that the enumerated A may be derived by B ^ C, then a case is found.

Some tricks are also used: 
mask = (1 << i); // i-bit mask
mask = mask | (1 << i); // prefix mask



---

** 38. [Perfect Squares.java] (https://github.com/awangdev/LintCode/blob/master/Java/Perfect%20Squares.java) ** Level: Medium Tags: [BFS, DP, Math, Partition DP]
      

Given a number n, find out how many squares it can consist of at least. 

Square number such as: 1, 4, 9, 16 ... etc

#### Partition DP
-Encounter the most value, think of DP.
-Seeing split words, thinking of split DP. 
-Thinking, if j * j = 9, then j = 3 is the minimum step; but if it is 10, it will be divided into 1 + 9 = 1 + j * j 
-Consider the last number: if 12 is cut out of 1, how will the remaining 11 be considered? Cut out 4 and considered 8?
-Partion method: When considering dp [i-x], x is not 1, but x = j * j.
-Becomes dp = Min {dp [i-j ^ 2] + 1}

#### time complexity
-At first glance it is O (n * sqrt (n)). Actually. But how to derive it?
-Consider the upper limit: turn small numbers into large derivation upper limits; consider the lower limit: integrate numbers into small ones to find the lower limit.
-Consider sqrt (1) + sqrt (2) + .... sqrt (n): find the upper bound and lower bound of this.
-Finally found that it is A * n * sqrt (n) <= actual time complexity <= B * n * sqrt (n)
-Then O (n * sqrt (n))

#### BFS
-minus all possible (i * i) and calculate the remain
-if the remain is new, add to queue (use a hashset to mark calculated item)
-find shortest path / lowest level number

#### Previous Notes
-No clue at first. I checked the hint
-1. The first step came to mind. From a mathematical point of view, it may start from the largest perfect square number.
-2. Then the idea comes to dp. Assuming the maxSqrNum is used in the last step, then the remaining dp [i-maxSqrNum ^ 2] +1 is not good?
-3. I did, and found a problem. ．．Select maxSqrNum in the last step? For example, 12 is an example.
-Then when prompted, think of BFS. Shun. Try everything from 1 to maxSqrNum. Find the smallest one.
-Look at the example where I split 12. That's very visually BFS.
-During the interview, if you are uncertain at this stage, talk to the interviewer and you may be prompted by BFS.



---

** 39. [Backpack VI.java] (https://github.com/awangdev/LintCode/blob/master/Java/Backpack%20VI.java) ** Level: Medium Tags: [Backpack DP, DP]
      

Give an array of nums, all positive numbers, no repeated numbers; find: # of method to spell out m.

The numbers in nums can be reused. Different orders can be counted as different spellings.

#### Backpack DP
-dp [i] means: # of ways to fill weight i
-1 dimension: dp [w]: There are many ways to fill weigth w. There are as many possibilities as before, just as many as:
-dp [w] = sum {dp [w-nums [i]]}, i = 0 ~ n

##### Analysis
-When fighting for a backpack, there can be duplicate items, so it doesn't make sense to think about 'which unique item was put last'.
-The backpack problem is always inseparable from weight.
-It's very similar to coin chagne: consider the value / weigth of the last thing put, regardless of which one.






---

** 40. [Binary Search Tree Iterator.java] (https://github.com/awangdev/LintCode/blob/master/Java/Binary%20Search%20Tree%20Iterator.java) ** Level: Medium Tags: [BST , Design, Stack, Tree]
      

Draw, BST in order traversal. Record the minimum value with stack and put it on top. O (h) space.
Every time you consume a TreeNode, you look at the rightNode (in fact, the next smallest candidate), and stack all the left children of the rightNode in a one-stop stack.

Previous Notes:
Use O (h) space:

Understand the law of binary search tree inorder traversal:
   First find left.left.left .... left in the end, here is added to the stack.
   Then consider parent, then right.

For example this question:
   The top in the stack, which is the node in the bottom left corner of the tree, is considered first, and it is named rst.
   In fact, after this rst is taken out, it is also the bottom left parent at the same time, considering the bottom parent.
   Finally, consider the lowest level parent.right, which is rst.right.

note:
   next () actually has a while loop, which is probably O (h). The title requires average O (1), so it is also okay.


Use O (1) space: there is no stack, and the update current is always the minimum value.

Find the next smallest value, if there is a right child in current:   
   Similar to iteration when using stack, then find the left-most child of current.right again, which is the minimum value.
   
If current has no right child:    
    Then look for the upper right parent of current node, search in BinarySearchTree from root.

note:
   Be sure to find the parent that meets parent.left == current.
   Conversely, if current is the right child of the parent, the parent will be reprocessed in the next round.
   But there is a mistake: the parent in the binary search tree is less than the right child, that is, it must have been visited in the previous step, so it will endlessly loop.




---

** 41. [Flatten Nested List Iterator.java] (https://github.com/awangdev/LintCode/blob/master/Java/Flatten%20Nested%20List%20Iterator.java) ** Level: Medium Tags: [Design , Stack]
      

Method 1: Use queue to type all the items you need
Method 2: Use stack to store the required items first, and add them back to the stack every time you open a subsequence.



---

** 42. [Best Time to Buy and Sell Stock with Cooldown.java] (https://github.com/awangdev/LintCode/blob/master/Java/Best%20Time%20to%20Buy%20and%20Sell%20Stock% 20with% 20Cooldown.java) ** Level: Medium Tags: [DP]
      

Sequence DP
Much like StockIII. Analyze the state of HaveStock && NoStock, and then look at the last step.



---

** 43. [Find Peak Element.java] (https://github.com/awangdev/LintCode/blob/master/Java/Find%20Peak%20Element.java) ** Level: Medium Tags: [Array, Binary Search ]
      

binary search. 
Goal: find peak, where both sides are descending
When the leftmost and rightmost are Integer.MIN_VALUE, it can also constitute the condition that the middle number mid is peak.

Note:
There is no need to specifically check (mid-1) <0 or (mid + 1)> = n.
prove:
1. Leftmost end: when start = 0, end = 2 => mid = 1, mid-1 = 0;
2. Rightmost end: when end = n-1, start = n-3; mid = (start + end) / 2 = n-2; 
Then mid + 1 = n-2 + 1 = n-1 <n is taken for granted



---

** 44. [Longest Common Subsequence.java] (https://github.com/awangdev/LintCode/blob/master/Java/Longest%20Common%20Subsequence.java) ** Level: Medium Tags: [DP, Double Sequence DP, Sequence DP]
      

Give two strings, A, B. Find the LCS in these two strings: the longest common character length (it does not need to be a continuous substring)

#### Double Sequence DP
-Set the length of dp to (n + 1), because dp [i] is used to represent the state of the previous i (ith), so when the length is required, i + 1 can be in the i position and hold i.
-Double sequence: The relationship between two sequences, both from the end of the character, analyze 2 cases:
-1. The last character of A is not in the common sequence or the last character of B is not in the common sequence.
-2. The last characters of A / B are in the common sequence. Overall count + 1.



---

** 45. [Letter Combinations of a Phone Number.java] (https://github.com/awangdev/LintCode/blob/master/Java/Letter%20Combinations%20of%20a%20Phone%20Number.java) ** Level : Medium Tags: [Backtracking, String]
      

Method 1: Iterative with BFS using queue.

Method 2: Recursively adding chars per digit



---

** 46. [Pow (x, n) .java] (https://github.com/awangdev/LintCode/blob/master/Java/Pow (x,% 20n) .java) ** Level: Medium Tags: [Binary Search, Math]
      

O (n) if you do it silly, consider O (logN) if you want to do better.
Reduce double counting, everything in half.

note:
-odd even number of n / 2
-positive and negative of n
-Case of n == 0, case of x == 0, case of x == 1.


---

** 47. [Construct Binary Tree from Preorder and Inorder Traversal.java] (https://github.com/awangdev/LintCode/blob/master/Java/Construct%20Binary%20Tree%20from%20Preorder%20and%20Inorder%20Traversal .java) ** Level: Medium Tags: [Array, DFS, Divide and Conquer, Hash Table, Tree]
      

As the title

#### DFS
-Same idea as Construct from Inorder && Postorder.
-Write out the letter examples of Preorder and Inorder, and find that the beginning of Preorder is always the root of this level. Write helpers accordingly, pay attention to the index.
-Similar to Convert Sorted Array to Binary Tree, find the corresponding index, and then:
-node.left = dfs (...), node.right = dfs (...)
-Divide and Conquer
-optimize on finding `mid node`: given value, find mid of inorder:
-Instead of searching linearly, just store inorder sequence in `map <value-> index>`, O (1)
-IMPORATANT: the mid from inorder sequence will become the main baseline to tell range: 
-`range of subTree = (mid-inStart)`
-sapce: O (n), time: O (n) access



---

** 48. [Add Two Numbers.java] (https://github.com/awangdev/LintCode/blob/master/Java/Add%20Two%20Numbers.java) ** Level: Medium Tags: [Linked List, Math ]
      

LinkedList has been reversed, just do it.
Traverse the two l1, l2 to handle the carry-on, generate a new node each time, and finally check the carry-on.

It is exactly the same as Add Binary's understanding.

note:
Linked List has no natural size.
Use DummyNode (-1) .next to hold the result.




---

** 49. [Add Two Numbers II.java] (https://github.com/awangdev/LintCode/blob/master/Java/Add%20Two%20Numbers%20II.java) ** Level: Medium Tags: [Linked List]
      

Singly-linked list requires reverse, use stack.
The final result should be restored to the sequence direction like the input list, which can be done just by pop () one by one.

The addition is the same:
   1.sum = carry
   2.carry = sum / 10
   3.sum = sum% 10;



---

** 50. [Balanced Binary Tree.java] (https://github.com/awangdev/LintCode/blob/master/Java/Balanced%20Binary%20Tree.java) ** Level: Medium Tags: [DFS, Tree]
      

Give a binary tree to see if it is height-balanced

#### DFS
-DFS using depth marker: Save every depth. Then if there are any conditions that do not meet the requirements, save it as -1.
-Once there are <0 or the difference is greater than 1, all return Integer.MIN_VALUE. Integer.MIN_VALUE is extreme, to ensure the correctness of the result.
-The final comparison returns whether the result is <0. If it is <0, then false.
-Traverse entire tree, O (n)


#### DFS, maxDepth function
-Same concept as in 1, but cost more traversal efforts.



---

** 51. [Populating Next Right Pointers in Each Node.java] (https://github.com/awangdev/LintCode/blob/master/Java/Populating%20Next%20Right%20Pointers%20in%20Each%20Node.java) ** Level: Medium Tags: [DFS, Divide and Conquer, Tree]
      

Give a special binary tree, treeNode has a next pointer inside.

Write a function that connects all nodes to the level node. The rightmost node.next = NULL

#### DFS + Divide and Conquer
-The title requires DFS. I figured out how to consider several situations at the DFS level. It is easy to write. NOT BFS, because requires O (1) space
-For a root, there are only a few points to avoid: root.left, root.right, root.next. 
-Find a way to connect the dots in these three directions:
-1. `node.left.next = node.right`
-2. If `node.next! = Null`, link` node.right.next = node.next.left`;
-Then in dfs (root.left), dfs (root.right)
-Time: visit && connect all nodes, O (n)

#### BFS
-It is not the same as the title, and it uses queue space, which is proportional to Input. It's too big.
-BFS over Tree. Use Queue and queue.size (), old rules.   
-For each queue of the process, pay attention to adding the next pointer. 



---

** 52. [Validate Binary Search Tree.java] (https://github.com/awangdev/LintCode/blob/master/Java/Validate%20Binary%20Search%20Tree.java) ** Level: Medium Tags: [BST , DFS, Divide and Conquer, Tree]
      

If so, verify that it is BST.

#### DFS
-View each parent-child relationship: leftchild <root <rightChild; 
-BST has two extremes: left-most-leaf is the smallest element, and right-most-leaf is largest
-imagine we know the two extreme border: Integer.MIN_VALUE, Integer.MAX_VALUE; pass node around and compare node vs. node.parent.
-Method: Pass root.val as max or min, and check children
- 

##### Note: 
-min / max long type when needed. 
-If the title really gives node.val = Integer.MAX_VALUE, we need to be able to compare it with long.



---

** 53. [Convert Sorted List to Binary Search Tree.java] (https://github.com/awangdev/LintCode/blob/master/Java/Convert%20Sorted%20List%20to%20Binary%20Search%20Tree.java) ** Level: Medium Tags: [BST, DFS, Divide and Conquer, Linked List]
      

As the title, convert a sorted singly linked list into a height balanced BST

#### DFS
-Divide and Conquer   
-Find the mid node
-Then split the two halves, and make dfs to make two subtrees: node.left, node.right
-Use the length to locate the mid, every time you find the middle point to be the root, then the first half and the second half are dfs with length.
-Find the mid with fast pointer. Better: no need to traverse entire linked list

#### Details
-slowPointer = node;
-fastPointer = node.next;
-Then put root = mid.next     
-Then start sortedListToBST (mid.next.next); // Last half    
-mid.next = null; // Very important, you have to break the sequence    
-sortedListToBST (head); // first half from the beginning     
-Finally root.left, root.right merge.   



---

** 54. [Flatten Binary Tree to Linked List.java] (https://github.com/awangdev/LintCode/blob/master/Java/Flatten%20Binary%20Tree%20to%20Linked%20List.java) ** Level : Medium Tags: [Binary Tree, DFS]
      

Give a binary tree, and make the tree a linked list, in-place.

#### DFS
-After analyzing the intent, follow the intent: Flatten the tree, no extra space.
-1. reserve right child: `reservedRightNode`
-2. Connect `root.right = root.left`, DFS flatten (root.right) 
-3. Receiving flowers, coneect end of list-> reservedRightNode
-4. flatten the rest. Root.right ...

##### Note
-The order must be clear, you can't write it wrong, you can see it by writing a few examples
-For those nodes that move, clean up node.left = null



---

** 55. [Minimum Size Subarray Sum.java] (https://github.com/awangdev/LintCode/blob/master/Java/Minimum%20Size%20Subarray%20Sum.java) ** Level: Medium Tags: [Array , Binary Search, Subarray, Two Pointers]
      
time: O (n)
space: O (1)

Given a string of positive integers, find the shortest subarray sum, where the sum> = s

#### Two pointer
-All are positive integers, so preSum must be growing.
-Then actually use two pointer: `start = 0, end = 0` to keep moving forward. Strategy: 
-1. end ++ until a solution where sum> = s is reached
-2. Then move start; record each solution, Math.min (min, end-start);
-3. Then move end and look down
-Note: Although it looks like a nested loop at first glance, after analysis, I found that it is actually a loop that moves according to the end pointer. start moves one space at a time. Overall, it's still O (n)

#### Binary Search
-O (nlogn) NOT DONE.

#### Double For loop
-O (n ^ 2), inefficient



---

** 56. [Longest Substring Without Repeating Characters.java] (https://github.com/awangdev/LintCode/blob/master/Java/Longest%20Substring%20Without%20Repeating%20Characters.java) ** Level: Medium Tags : [Hash Table, String, Two Pointers]
      

method 1:
Two Pointers
Double pointer: Iterate from start, but the first step is to advance the end while loop; until the end cannot be pushed, then start ++
Ingenious point: Because end is a peripheral variable, on the start loop, end will not reset; [star ~ end] does not need to be calculated in the middle.
Eventually O (n);

Previous verison of two pointers:
Use two pointers, head and i.
Note: head is likely to be returned to an earlier place, such as abbbbbba. When it encounters the second a, head turns into head = 0 + 1 = 1.      
Of course this is wrong, so make sure that the head keeps growing and does not backtrack.

Method 2:
   HashMap <Char, Integer>: <character, last occurance index>
   Once there are duplicates, rest map.
   When there is no repetition, continue to map.put (), and then find the max value

Problem: After each reset map, it starts from the oldest index, and the worst case is O (n ^ 2):
'abcdef .... xyza'




---

** 57. [Remove Nth Node From End of List.java] (https://github.com/awangdev/LintCode/blob/master/Java/Remove%20Nth%20Node%20From%20End%20of%20List.java) ** Level: Medium Tags: [Linked List, Two Pointers]
      

O (n), one pace, no extra space
Find the window, pan, and finally skip a node between pre and head.



---

** 58. [Linked List Cycle II.java] (https://github.com/awangdev/LintCode/blob/master/Java/Linked%20List%20Cycle%20II.java) ** Level: Medium Tags: [Linked List, Math, Two Pointers]
      

LinkedList has cycle, find the starting point of cycle (the first repeated element).

#### Slow, fast Pointer
-Speed ​​pointer, O (1) space.
-1. After confirming the cycle 2. Mathematical problem: Find the beginning.
-When head == slow.next, head is the cycle starting point.
-In other words, when slow moves to that traceback point, the point of slow.next is exactly the point of head ...

#### Proof
-1. Suppose the slow pointer moves t steps, and the fast pointer doubles, which is 2t.
-2. We assume that the length of the cycle is Y, and the length before entering the cycle is X.
-3. Suppose that the slow pointer goes m cycles, and the fast pointer goes n cycles, and the two pointers meet.
-4. Finally met at point K in the Y cycle, that is, both hands took K steps in the last lap.
-Then:
-t = X + mY + K
-2t = X + nY + K
-? Integration formula: X + K = (n-2m) Y
-Here m and n are just integer number of laps, that is to say X and K are added together, it is the end cycle. X and K are complementary
-Conclusion: When the slow / fast pointers meet at point K, and then take step X, the starting point of the cycle is reached, which is the starting point required by the question.

#### Hash Table, O (n) space




---

** 59. [Kth Smallest Element in a Sorted Matrix.java] (https://github.com/awangdev/LintCode/blob/master/Java/Kth%20Smallest%20Element%20in%20a%20Sorted%20Matrix.java) ** Level: Medium Tags: [Binary Search, Heap]
      
time: O (n + klogn)
space: O (n)

Give a sorted matrix, find kth smallest number (not distinct)

Related: `Kth Largest Element in an Array`

#### PriorityQueue
-Similar to Merge K sorted Array / List: Use PriorityQueue.
-Because the element of Array cannot find next directly, use a class node to store value, x, y positions.
-Initial O (n) time, also find k O (k), sort O (logn) => O (n + klogn)
-Variant: Kth Largest in N Arrays

#### Binary Search
-we know where the boundary is start / end are the min / max value. 
-locate the kth smallest item (x, y) by cutt off partition in binary fasion: 
-find mid-value, and count # of items <mid-value based on the ascending matrix
-O (nlogn)




---

** 60. [Find Minimum in Rotated Sorted Array.java] (https://github.com/awangdev/LintCode/blob/master/Java/Find%20Minimum%20in%20Rotated%20Sorted%20Array.java) ** Level : Medium Tags: [Array, Binary Search]
      

After drawing, after the minimum value is rotated, it becomes the lowest valley in the middle of the array.
Also, the minimum value of the left slope is greater than the maximum value of the right slope. 
Use this to judge binary search.

O (nlogn)



---

** 61. [Connecting Graph.java] (https://github.com/awangdev/LintCode/blob/master/Java/Connecting%20Graph.java) ** Level: Medium Tags: [Union Find]
      

Haven't run this program, it is a simple implementation of UnionFind.
Document describes the calculation principles / ideas of each link.



---

** 62. [Connecting Graph II.java] (https://github.com/awangdev/LintCode/blob/master/Java/Connecting%20Graph%20II.java) ** Level: Medium Tags: [Union Find]
      

Lint can't run yet, all according to the intent and answer document.



---

** 63. [Connecting Graph III.java] (https://github.com/awangdev/LintCode/blob/master/Java/Connecting%20Graph%20III.java) ** Level: Medium Tags: [Union Find]
      

It is still a variant of UnionFind, this time it is calculated how many unions are left. In fact, it is very simple, maintain a global variable count:
At the beginning count = n, because all elements are in bulk; each time union, count--.



---

** 64. [Number of Islands.java] (https://github.com/awangdev/LintCode/blob/master/Java/Number%20of%20Islands.java) ** Level: Medium Tags: [BFS, DFS, Matrix DFS, Union Find]
      

Give a 2Dmatrix, which is 1 and 0, find #of island.

#### DFS
-More or less like a graph problem: visit all nodes connected with the starting node.
-top level has a double for loop, look at each point.
-Whenever it encounters 1, count + 1, then the DFS helper function marks everything related to this island as '0'
-This ensures that every visited island is cleaned
-O (mn) time, visit all nodes

#### Union Find
-You can use union-find, just like Number of island II.
-But this is not a Return list, but just # of islands
-Union Find is independent from the problem: it models the union status of integers.
-Remember the template and several variations of UnionFind (Connecting Graph I, II, III), and the final code is easier to write.



---

** 65. [Surrounded Regions.java] (https://github.com/awangdev/LintCode/blob/master/Java/Surrounded%20Regions.java) ** Level: Medium Tags: [BFS, DFS, Matrix DFS, Union Find]
      

Give a 2D board with 'X' and 'O'. Paint all areas surrounded by X with 'X'. 

Starting from the edges of the four sides, spreading like a zombie virus, mark all the nodes on the sides, then change the 'O' to X, and finally reply marks-> 'O'

#### Union Find
-This time, the concept of rank is used in UnionFind, which needs review. Rank [] is the size of the union where each node is tracked.
-The purpose is: always merge into the big union
-note: Convert 2D coordinate (x, y) to 1D: index = x * n + y

#### DFS: mark all invalid 'O'
-Reversed thinking: find surrounded nodes, how about filter out border nodes && their connections?
-Need to traverse all the border nodes, consider dfs, visit all.
-loop over border: find any 'O', and dfs to find all connected nodes, mark them as 'M'
-time: O (mn) loop over all nodes to replace remaining 'O' with 'X'

#### DFS: mark all valid 'O'
-More like a graph problem: traverse all 'O' spots, and mark as visited int [] [] with area count [1-> some number]
-Run dfs as top-> bottom: mark area count and dsf into next level
-End condition: if any 'O' reaches border, mark the global map <count, false>
-keep dfs untill all connected nodes are visited.
-At the end, O (mn) loop over the matrix and mark 'X' for all the true area from map.
-Practice: write code to verify

### BFS
-TODO



---

** 66. [Implement Trie (Prefix Tree) .java] (https://github.com/awangdev/LintCode/blob/master/Java/Implement%20Trie%20 (Prefix% 20Tree) .java) ** Level: Medium Tags: [Design, Trie]
      

Implement Tire, also known as Prefix Tree. Do three functions: insert, search, startWith

#### Trie
-HashMap builds Trie. Trie three methods:
-1. Inset: add word   
-2. Search: find word    
-3. StartWith: find prefix    

##### Features
-Only two children are binary tree. Then multiple children are Trie
-So how do I find a child without a left / right pointer?   
-Use HashMap, take child's label as Key, and value is child node. HashMap moves   

##### other
-The char in the node is optional here. Just use the map to store the children distributed downwards in each TrieNode.  
-There is another problem, such as related to other types of search. If you want to return whole string at the end, you can store an up-to-this-point String in node.

##### Previous Note
-If you encounter a one-word query, consider it.
-Pay attention when building TrieNode: how to find children? If it's a map, it's actually pretty good.
-Moreover, the char or string in each node is sometimes not very useful.
-Can be empty. However, for some topics, such as what String to return at the end, a true String can be stored at the end string.





---

** 67. [Add and Search Word-Data structure design.java] (https://github.com/awangdev/LintCode/blob/master/Java/Add%20and%20Search%20Word%20-%20Data%20structure% 20design.java) ** Level: Medium Tags: [Backtracking, Design, Trie]
      

Trie structure, the deformation of the prefix tree: '.' Can replace any character, then iterate all children of this node.

There are char, isEnd, HashMap <Character, TrieNode> inside the node   
Build trie = Insert word: Add without node, move with node.   
Search word: Report an error without node. Return true to the end   

This problem is because '.' Can replace any possible character. None of them is a new path, so recursive is better.    
(iterative is about to be queuing, please be troublesome)



---

** 68. [Word Search.java] (https://github.com/awangdev/LintCode/blob/master/Java/Word%20Search.java) ** Level: Medium Tags: [Array, Backtracking, DFS]
      

#### DFS, Backtracking:
-Find the first letter, then recursively DFS to string the word to the end:
-For each letter, go in four directions, one of them can be true.
-Note: Each time you reach a letter, mark '#'. After 4 path recurse returns, mark it back.

#### Note: other ways of marking visited:
-Use a boolean visited [] []
-Use hash map, key = x @ y




---

** 69. [Decode String.java] (https://github.com/awangdev/LintCode/blob/master/Java/Decode%20String.java) ** Level: Medium Tags: [DFS, Divide and Conquer, Stack ]
      

Give an expression string. It contains numbers, letters, parentheses. The number represents the content of the parentheses repeated several times.

The parentheses can be String or expression.

Purpose: Expand expression into a normal String.


#### Stack, Iteratively
-Process inner item first: last come, first serve, use stack.
-Record number globally and only use it when '[' is met.
-Stack stores the contents of [], detect brackets at the beginning and end: process inner string at the end
-There are many details that need attention to get it right:
-Stack <Object> can also be used, pay attention to the cast everywhere. Need to be stored is Object: String, Integer
-Several type checks: instanceof String, Character.isDigit (x), Integer.valueOf (int num)
-When it comes out: `sb.insert (0, stack.pop ())`


#### DFS
-Bottom-> up: find deepest inner string first and expand from inside of `[]`
-Similar to some features to consider when stacking. Special points: ** Check the end of `[]` **
-Because in DFS, the substring in parentheses will be retained to enter the next level, so we need to keep track of substring at the base level.
-Use int paren to track the opening and closing of parentheses, and find closure ']' when paren == 0 again
-Other times, continue to append to substring




---

** 70. [Maximum Binary Tree.java] (https://github.com/awangdev/LintCode/blob/master/Java/Maximum%20Binary%20Tree.java) ** Level: Medium Tags: [Stack, Tree]
      

Give a string of numbers and make a maximum binary tree: the top root is the largest; the left child is also a max tree, and the right child must also be a max tree.

#### Monotonous Stack
-Decreasing stack using bottom-> top: the bottom root is maintained as the largest element.
-In the process, once currNode.val> stack.peek () is encountered, it means that this currNode needs to be placed at the bottom of the stack.
-In other words, when this condition is met, process, pop () all currNode.val> stack.peek (), and finally add currNode.

-The requirements of the maxTree problem itself are: the big one is in the middle, and the left and right subTrees must also be maxTree:
-Monotonous Stack helps keep / track of max value here, but the logic of left / right tree is unique to MaxTree.
-The assignment of the left / right node is based on the requirements of the title: after the middle maximum is separated, the left is the left subTree, and the right is the right subTree.

#### Previous notes
-Should memorize MaxTree. By analogy, you will do Min-Tree, Expression Tree
-In Stack, the maximum value is below. Using this property, there are several steps:

##### Step1
-Pop out all the less than curr nodes, while loop, keep it going.    
-The last node that popped out is smaller than Curr: it is also the largest popped out of the stack that is smaller than the curr, which is the closest to the curr size. (Because the maximum value of this stack is below)    
-Put this largest node smaller than curr in curr.left.    

##### Step2   
-Then, the next stack must be greater than curr:   
-That becomes the left parent of curr. Set stack.peek (). Right = curr.

##### Step3   
-End: The bottom of the stack must be the largest one, which is the head of the max tree.





---

** 71. [Swap Nodes in Pairs.java] (https://github.com/awangdev/LintCode/blob/master/Java/Swap%20Nodes%20in%20Pairs.java) ** Level: Medium Tags: [Linked List]
      

#### enumurate 
The basic principle, write it out, and then wire:
pre-> A-> B-> C-> ...
A virtual preNode is required as the starting node, otherwise the subsequent nodes cannot be changed to the beginning.

#### Note
Use dummy = pre as the previous box of the head.
Use `pre.next == null && pre.next.next` to check if it is NULL.
pre.next.next guarantees at least one swap.



---

** 72. [Wood Cut.java] (https://github.com/awangdev/LintCode/blob/master/Java/Wood%20Cut.java) ** Level: Medium Tags: [Binary Search]
      

The idea of ​​dichotomy: the judgment is a validate () function, not a simple '=='

No sorting is needed! Why? Because we are not dicing on the given array, we are dicing on [0, max] based on the maximum value.

Overall time: O (nLogM), where M = largest wood length



---

** 73. [Find the Duplicate Number.java] (https://github.com/awangdev/LintCode/blob/master/Java/Find%20the%20Duplicate%20Number.java) ** Level: Medium Tags: [Array , Binary Search, Two Pointers]
      

-Be careful not to think about formulas: think mid is index
-Here mid is actually a value of binary search on value [1, n].
-Use validate () function again

Time: O (nLogN)



---

** 74. [Game of Life.java] (https://github.com/awangdev/LintCode/blob/master/Java/Game%20of%20Life.java) ** Level: Medium Tags: [Array]
      

#### basic
-Simple implementation, just write the count function clearly.
-time: O (mn), extra space: O (mn)
-Note that the board [i] [j] copy

#### follow up
unlimited border? It may be necessary to split the board. Use a large frame to split, and each time you wrap a line, repeat the calculation 2 times.

#### improvement: do it in place!
-time: O (mn), extra space: O (1)
-bit manipulation: use the second bit to store the previous value.
-Because we only consider 0 and 1, we can do it this way. But it is not scalable.
-If you need to store multiple states, you may need to move more bits, or use a state map
-Note the details of bit manipulation: << 1, >> 1, and mast usage: |, & 




---

** 75. [Number of Airplane in the sky.java] (https://github.com/awangdev/LintCode/blob/master/Java/Number%20of%20Airplane%20in%20the%20sky.java) ** Level : Medium Tags: [Array, Interval, PriorityQueue, Sort, Sweep Line]
      

#### Sweep Line
-Split Interval into points on the number line 
-Take off mark 1   
-Landing mark -1     
-Sort by PriorityQueue, loop through queue, and calculate the possible max (takeoff + landing) value.

#### Note
-Take off and land at the same time, which is 1-1 = 0. So there is a second while loop in the while loop,    
-When coordinates x are coincident, add and subtract all x points here, and then compare max.     
-This avoids wrong counts or counts



---

** 76. [Meeting Rooms II.java] (https://github.com/awangdev/LintCode/blob/master/Java/Meeting%20Rooms%20II.java) ** Level: Medium Tags: [Greedy, Heap, PriorityQueue, Sort, Sweep Line]
      

Give a string of numbers to represent the start / end time of the meeting. Find out how many meetings happen at the same time (how many rooms are needed)

#### PriorityQueue
-PriorityQueue + a Class to resolve. O (nlogn)
-Same question as Number of Airpline in the sky

#### Method 2: Tried it with a sorted Array + HashMap
It's ok, but HashMap should be careful when handle edge, because the map key of start and end will be repeated at the same time.



---

** 77. [Unique Path.java] (https://github.com/awangdev/LintCode/blob/master/Java/Unique%20Path.java) ** Level: Medium Tags: [Array, Coordinate DP, DP]
      

2D array, count how many ways to go to the bottom right corner.

##### DP
-Count DP. Note that the first two positions of the equation are added together: the first two cases have no overlap, and there is no shortage of cases.
-Note the initialization, return to 1.
-The reason for initialize is that it is also a reminder: -1index will appear in the equation
-Of course, row i = 0, or col j = 0, there is only 1 way to access
-time O (mn), space O (mn)

##### Scrolling array
-[i] is only related to [i-1]. Use curr / prev to build a rolling array.
-space O (n) optimize space




---

** 78. [Maximal Square.java] (https://github.com/awangdev/LintCode/blob/master/Java/Maximal%20Square.java) ** Level: Medium Tags: [Coordinate DP, DP]
      

You can only go to the right and below, and find the square with the largest area. That is, find the square that has become the longest.

#### DP
-Square, each side needs to be the same length.
-Taking the lower right corner as the point of consideration, the conditions must be met: the points of left / up / diagonal are all 1
-And, if all three points are derived in three directions, the longest square edge is the shortest edge among them (limited by the shortest edge)
-dp [i] [j]: max square length when reached at (i, j), from the 3 possible directions
-dp [i] [j] = Math.min (Math.min (dp [i-1] [j], dp [i] [j-1]), dp [i-1] [j-1]) + 1;
-Space, time O (mn)

##### init
Each point may have a side length of 1, if matrix [i] [j] == '1'

##### Scrolling array
The relationship between [i] and [i-1], think of rolling arrays to optimize space, O (n) sapce.



---

** 79. [Coins in a Line.java] (https://github.com/awangdev/LintCode/blob/master/Java/Coins%20in%20a%20Line.java) ** Level: Medium Tags: [DP , Game Theory, Greedy]
      

Take the chess piece game, each person can take 1 or 2 and take away the loss of the last child. Q: Based on the given chess piece loss, can I determine the winning or losing of the first mover?

Game Theory: If I want to win, the situation I get back must be 'possible to lose'.

#### DP, Game Theory
-To win, it must be guaranteed that when the opponent gets the board, in all cases where he can go, it is 'possible to lose', that is enough.
-Design dp [i]: indicates whether I can win when i face the situation of coins, depending on whether I can lose one or two, can the opponent lose?
-dp [i] =! dp [i-1] ||! dp [i-2]
-Time: O (n), space O (n)
- 博弈问题, 常从'我的第一步'角度分析, 因为此时局面最简单.

#### Rolling Array
空间优化O(1). Rolling array, %2



---

**80. [Coins in a Line II.java](https://github.com/awangdev/LintCode/blob/master/Java/Coins%20in%20a%20Line%20II.java)**      Level: Medium      Tags: [Array, DP, Game Theory, Memoization, MiniMax]
      

给一串coins, 用values[]表示; 每个coin有自己的value. 先手/后手博弈,
每次只能 按照从左到右的顺序, 拿1个或者2个棋子, 最后看谁拿的总值最大.

MiniMax的思考方法很神奇, 最后写出来的表达式很简单

#### DP, Game Theory 自考过程比较长
- 跟Coins in a line I 不一样: 每个coin的value不同.
- 用到MiniMax的思想, 这里其实是MaxiMin. Reference: http://www.cnblogs.com/grandyang/p/5864323.html
- Goal: 使得player拿到的coins value 最大化.
- 设定dp[i]: 从index i 到 index n的最大值. 所以dp[0]就是我们先手在[0 ~ n]的最大取值 
- 于此同时, 你的对手playerB也想最大化, 而你的选择又不得不被对手的选择所牵制.
- 用MaxiMin的思想, 我们假设一个当下的状态, 假想对手playerB会做什么反应(从对手角度, 如何让我输)
- 在劣势中(对手让我输的目标下)找到最大的coins value sum


##### 推算表达式
- Reference里面详细介绍了表达式如何推到出来, 简而言之:
- 如果我选了i, 那么对手就只能选(i+1), (i+2) 两个位置, 而我在对方掌控时的局面就是min(dp[i+2], dp[i+3])
- 如果我选了i和(i+1), 那么对手就只能选(i+2), (i+3) 两个位置, 而我在对方掌控时的局面就是min(dp[i+3], dp[i+4])
- 大家都是可选1个或者2个coins
- 目标是maximize上面两个最坏情况中的最好结果

##### 简化表达式
- 更加简化一点: 如果我是先手, dp[i]代表我的最大值.
- 取决于我拿了[i], 还是[i] + [i+1], 对手可能是dp[i + 1], 或者是dp[i+2]
- 其实dp[i] = Math.max(sum - dp[i + 1], sum - dp[i + 2]);
- 这里的sum[i] = [i ~ n] 的sum, 减去dp[i+1], 剩下就是dp[i]的值没错了

##### Initialization
- 这个做法是从最后往前推的, 注意initialize dp末尾的值.
- dp = new int[n + 1]; dp[n] = 0; // [n ~ n]啥也不选的时候, 为0.
- sum = new int[n + 1]; sum[n] = 0; // 啥也不选的时候, 自然等于0
- 然后记得initialize (n-1), (n-2)

##### 时间/空间
Time O(n)
Space O(n): dp[], sum[]



---

**81. [Binary Tree Postorder Traversal.java](https://github.com/awangdev/LintCode/blob/master/Java/Binary%20Tree%20Postorder%20Traversal.java)**      Level: Medium      Tags: [Stack, Tree, Two Stacks]
      

如题, POST-ORDER traversal.

LeetCode给了hard, 应该是觉得stack的做法比较难想到.

#### Recursive
trivial, 先加left recursively, 再加right recursively, 然后组成头部.

#### Stack
- 双stack的思想, 需要在图纸上画一画
- 原本需要的顺序是: 先leftChild, rightChild, currNode.
- 营造一个stack, reversely process: 先currNode, 再rightChild, 再leftChild
- 这样出来的结果是reverse的, 那么翻转一下就可以了.
- v1做的时候用了stack1, stack2, 因为根据这个双stack的思想而来
- v2简化, 可以放在一个stack里面, 每次record result 的时候: rst.add(0, item);

##### 利用stack的特点
- 每次加element进stack的时候, 想要在 bottom/后process的, 先加
- 想要下一轮立刻process的, 最后push进stack.

##### 注意
这些binary tree traversal的题目.常常有多个做法:recursive or iterative



---

**82. [Compare Version Numbers.java](https://github.com/awangdev/LintCode/blob/master/Java/Compare%20Version%20Numbers.java)**      Level: Medium      Tags: [String]
      

给两串version number,  由数字和'.' 组成. 比较先后顺序. 

If version1 > version2 return 1, if version1 < version2 return -1, otherwise return 0.

#### divide and conquer 
- 用 str.split("\\.") 分割string
- Convert成integer, 逐个击破

#### 注意
- '1.0' 和 '0' 是相等的
- 如果可以假设version integer都是valid, 直接Integer.parseInt()就可以了
- 不然的话, 可以compare string



---

**83. [Count Complete Tree Nodes.java](https://github.com/awangdev/LintCode/blob/master/Java/Count%20Complete%20Tree%20Nodes.java)**      Level: Medium      Tags: [Binary Search, Tree]
      

Complete Tree就是说, 最后一个level可能是缺node的(不是说最右下角缺node, 别忘了!)

#### DFS + Optimization
- 每次看最左left depth和最右leaf depth 是不是一样, 如果一样, 直接 2 ^ h - 1就好
- 不一样的话, 再DFS

##### Trick
- 直接DFS会timeout, O(n), 其实可以optimize
- to pass the test with O(h^2), 位运算: Math.pow(2, h) = 2 << (h - 1). 神奇!
- 2 << 1就是把所有bits往左移动一位, 也就是 * 2 

#### Iteratively
- See details in comments inline. 要对tree非常理解
- binary tree one child tree nodes # = 2 ^ h - 1; 所以一个child tree + root = 2 ^ h



---

**84. [Course Schedule.java](https://github.com/awangdev/LintCode/blob/master/Java/Course%20Schedule.java)**      Level: Medium      Tags: [BFS, Backtracking, DFS, Graph, Topological Sort]
      

- 一堆课用int[2] pair 来表示. [1, 0] 表示要上课1的话, 必须先把课0上了. 
- 每一个数字都是一个ndoe, 题目问是否能把所有的课排了
- input是 numOfCourses, 还有这个prerequisites [[]]

#### Topological Sort
- 给一个graph of nodes
- 至关重要: 用`List[] edges; edges[i] = new ArrayList<>();` 来表示graph: 就是每个node, to all its neighbors
- 目标是根据edge 的 direction, 把这个graph 里面的 node sort 一个list
- 如果有cycle, 这个item就不会被放在最后的list 里面. 
- 比如: 如果两个课互相是dependency, 就变成了cyclic dependency, 这样不好.


#### BFS
- Kahn algorithem:
- 先build一个graph map: <node, list of nodes >; or `List[] edges; edges[i] = new ArrayList<>();`
- count in-degree: inDegree就是每个node上面, **有多少个走进来的edge**?
- **IMPORTANT**: always initialize inDegree map/array with 0
- 那些没有 in-coming-edge的, indegree 其实就 等于 0, 那么他们就应该在final result list里面
- 对这些 indegree == 0 的 nodes BFS, add to queue.
- visit queue 上每个 node: count++, also add this curr node to sorted list
- Check all neighbors/edges of curr node: 如果visit过了, 这个node上的 indegree--
- 如果 indegree == 0, add this node to queue.

##### Indegree 原理
- Note: 如果有cycle, 这个node上面会多一些inDegree, 也就无法清0, 它也无法进入 queue && sorted list. 
- Remember: **indegree是周围的node到我这里的次数count**
- 如果周围所有node的连线, 都意义切除后, 我的indegree还不等于0, 那么肯定有某些node间接地有重复连线, 也就是有cycle
- Topological problem: almost always care about cycle case (if detecting cycle is not goal)

#### DFS
- 这道题没有要求作出final list, 相对简单, 只要visit每个nodes, 最后确认没有cycle就好了
- 用 visited int[] 来确认是否有cycle. 1 代表 paretNode visited, -1 代表在DFS上一行的标记
- 如果遇到-1, 说明这个node在上一级或者以上的同一个dfs path里面已经走过, 那么证明有cycle, return false.
- 走完一个node的所有neighbor, 都没有fail, 那么backtracking, set visited[i] = 1
- 真的topo sort会在DFS的底端, 把record放进一个stack, 最后reverse, 就是真的sort order.

#### Notes:
- 还有 List[] arrayOfList = new ArrayList[]; 这样的操作啊, 代替了map<integer, integerList>
- List[]的list, 其实是default  List<Object>

#### Previous notes
有点绕，但是做过一次就明白一点。    
是topological sort的题目。一般都是给有dependency的东西排序。    

最终都会到一个sink node， 再不会有向后的dependency, 在那个点截止。    
我就已这样子的点为map的key, 然后value是以这个node为prerequisite的 list of courses.    

画个图的话，prerequisite都是指向那个sink node， 然后我们在组成map的时候，都是从sink node 发散回来到dependent nodes.    

在DFS里面，我们是反向的， 然后，最先完全visited的那个node, 肯定是最左边的node了，它被mark的seq也是最高的。    

而我们的sink node，当它所有的支线都visit完了，seq肯定都已经减到最小了，也就是0，它就是第一个被visit的。   


最终结果：
每个有pre-requisit的node都trace上去（自底向上），并且都没有发现cycle.也就说明schedule可以用了。



---

**85. [Course Schedule II.java](https://github.com/awangdev/LintCode/blob/master/Java/Course%20Schedule%20II.java)**      Level: Medium      Tags: [BFS, DFS, Graph, Topological Sort]
      

- 一堆课用int[2] pair 来表示. [1, 0] 表示要上课1的话, 必须先把课0上了. 
- 每一个数字都是一个ndoe, 题目求这个最后排好的课的list
- 如果排不好, 就给个空就好
- input是 numOfCourses, 还有这个prerequisites [[]]
- 做法跟Course Schedule I 非常像, 可以参考.

#### Topological Sort, Indegree, BFS
- 用`List[] edges; edges[i] = new ArrayList<>();` 来表示graph: 就是每个node, to all its neighbors
- 每个没有 inDegree==0 node, 都是可以加进 final list里面的. 比如一开始找到的那些 inDegree = 0的 node
- 注意, 如果 prerequisites = [], 那么就是说这些课都independent, 开个int[0 ~ n-1]的数组并赋值就好.
- 如果有cycle, 严格意义上就做不了topological sort, 也无法涵盖所有nodes,  那么return [ ]

#### DFS
- 根据 Course Schedule 里面的DFS 修改
- 维持visited int[]全局变量
- 维持sortedList int[] 全局变量, 注意加进去的时候是 add(0, node) 加在开头这样
- 每次到一个node的children全部DFS走完之后, 就可以把他加进final list里面
- 如果有cycle, 也就是dfs return false的时候, 这个题目判定排课失败, return new int[] { }



---

**86. [Contains Duplicate III.java](https://github.com/awangdev/LintCode/blob/master/Java/Contains%20Duplicate%20III.java)**      Level: Medium      Tags: [BST]
      

给一个unsorted array, 问, 是否有两个element, value相差最大为t,  而两个element的index 相差最大为k.

Note: 虽然题目名字是Contains Duplicate, 但其实要找的两个element不是duplicate, 而是Math.abs(value1 - value2) <= t.

#### TreeSet
- TreeSet还是一个set, 我们用来装已经visit过得item
- 如果window大小超过K, 那么把nums[i - k - 1] 去掉, 并且加上新的element
- 这里有个公式推算: (Math.abs(A-B) <= t) =>>>>> (-t <= A - B <= t) =>>>>>> A >= B - t, A <= B + t
- 也就是说, 如果对于 B = nums[i], 来说, 能找到一个target A, 满足上面的公式, 那么就可以 return true.
- Time O(nLogk), treeSet的大小不会超过k,  而 treeSet.ceiling(), treeSet.add(), treeSet.remove() 都是 O(logK)
- Space O(k)

#### Note
- 与Contains Duplicate II 类似概念. TreeSet有BST 因此可以直接用, 而不用自己构建BST
- 简化题目里面的重要条件 Math.abs(A-B) <= t 而推断出 A >= B - t, A <= B + t
- 并且需要需要用 TreeSet.ceiling(x): return number greater or equal to x. 这个用法要记住吧, 没别的捷径.



---

**87. [Jump Game.java](https://github.com/awangdev/LintCode/blob/master/Java/Jump%20Game.java)**      Level: Medium      Tags: [Array, DP, Greedy]
      

给出步数，看能不能jump to end.

#### Greedy - start from index = 0
- Keep track of farest can go
- 一旦 farest >= nums.length - 1, 也就是到了头, 就可以停止, return true.
- 一旦 farest <= i, 也就是说, 在i点上, 已经走过了步数, 不能再往前跳, 于是 return false
- This can be done using DP. However, greedy algorithm is fast in this particular problem.

#### Greedy - start from index = n - 1
- greedy: start from end, and mark last index
- loop from i = [n - 2 -> 0], where i + nums[i] should always >= last index
- check if last == 0 when returning. It means: can we jump from index=0 to the end?
- Time: O(n), beat 100%

#### DP
- DP[i]: 在i点记录，i点之前的步数是否可以走到i点？ True of false.
- 其实j in [0~i)中间只需要一个能到达i 就好了
- Function: DP[i] = DP[j] && (A[j] >= i - j), for all j in [0 ~ i)
- Return: DP[dp.length - 1];
- Time: O(n^2)




---

**88. [Coin Change 2.java](https://github.com/awangdev/LintCode/blob/master/Java/Coin%20Change%202.java)**      Level: Medium      Tags: [Backpack DP, DP]
      

给串数字, target amount, 求总共多少种方式可以reach the amount.

#### DP
- O(MN): M, total target amount; N: size of coins
- 类似于: 网格dp, unique path 里面的2种走法: 从上到下, 从左到右
- 状态: dp[i]: sum of ways that coins can add up to i.
- Function: dp[j] += dp[j - coins[i]];
- Init: dp[0] = 1 for ease of calculation; other dp[i] = 0 by default
- note: 避免重复count, 所以 j = coins[i] as start
- 注意 coins 需要放在for loop 外面, 主导换coin的流程, 每个coin可以用无数次, 所以在每一个sum value上都尝试用一次每个coin

#### knapsack problem: backpack problem



---

**89. [Decode Ways.java](https://github.com/awangdev/LintCode/blob/master/Java/Decode%20Ways.java)**      Level: Medium      Tags: [DP, Partition DP, String]
      
time: O(n)
space: O(n)

给出一串数字, 要翻译(decode)成英文字母. [1 ~ 26] 对应相对的英文字母. 求有多少种方法可以decode.

#### Partition DP
- 加法原理: 根据题意, 有 range = 1 的 [1, 9], range = 2 的 [10~26] 来作为partition.
- 确定末尾的2种状态: single letter or combos. 然后计算出单个letter的情况, 和双数的情况
- 定义`dp[i] = 前i个digits最多有多少种decode的方法`. new dp[n + 1].
- 加法原理: 把不同的情况, single-digit, double-digit 的情况加起来
- dp[i] += dp[i - x], where x = 1, 2
- note: calculate number from characters, need to - '0' to get the correct integer mapping.
- 注意: check value != '0', 因为'0' 不在条件之中(A-Z)
- Space, Time O(n)

#### 引申
- 这里只有两种partition的情况 range=1, range =2.  如果有更多partition的种类, 就可能多一层for loop做循环




---

**90. [Minimum Path Sum.java](https://github.com/awangdev/LintCode/blob/master/Java/Minimum%20Path%20Sum.java)**      Level: Medium      Tags: [Array, Coordinate DP, DP]
      

#### DP
- Time, Space O(MN)
- 往右下角走, 计算最短的 path sum. 典型的坐标型.
- 注意: init 第一行的时候, 要accumulate dp[0][j - 1] + grid[i][j], 而不是单纯assign grid[i][j]

#### Rolling Array
- Time O(MN), Space O(1)
- 需要在同一个for loop里面完成initialization, 和使用dp[i][j]
- 原因: dp[i % 2][j] 在被计算出来的时候, 是几乎马上在下一轮是要被用的; 被覆盖前不备用,就白算
- 如果按照第一种方法, 在开始initialize dp, 看起来固然简单, 但是不方便空间优化



---

**91. [Counting Bits.java](https://github.com/awangdev/LintCode/blob/master/Java/Counting%20Bits.java)**      Level: Medium      Tags: [Bit Manipulation, Bitwise DP, DP]
      

给一个数组, 算里面有多少bit 1. 

#### Bitwise DP
- 对于每一个数字, 其实很简单就能算出来: 每次 >>1, 然后 & 1 就可以count 1s. Time: 一个数字可以 >>1 O(logN) 次
- 现在要对[0 ~ num] 都计算, 也就是N个数字, 时间复杂度: O(nLogN).
- 用DP来优化, 查找过的number的1s count, 存下来在 dp[number]里面.
- 计算你顺序从 0 -> num, count过的数字就可以重复利用.
- Bit题目 用num的数值本身表示DP的状态.
- 这里, dp[i] 并不是和 dp[i-1]有逻辑关系; 而是dp[i] 和dp[i>>1], 从binary representation看出有直接关系.



---

**92. [Continuous Subarray Sum.java](https://github.com/awangdev/LintCode/blob/master/Java/Continuous%20Subarray%20Sum.java)**      Level: Medium      Tags: [Coordinate DP, DP, Math, Subarray]
      

给一个非负数的数列和数字k(可正负, 可为0). 找到连续子序列(长度超过2), 使得这个subarray的sum 是 k的倍数. 问: 是否可能?

#### DP
- O(n^2)
- 需要记录在0 ~ i点(包括nums[i], 以nums[i]结尾)的sum, 坐标型动态规划.
- dp[i] = dp[i - 1] + nums[i];
- 最后移动, 作比较

#### 直接算结果
- 从sum = 每次[i ~ j]的所有情况
- 验证



---

**93. [House Robber II.java](https://github.com/awangdev/LintCode/blob/master/Java/House%20Robber%20II.java)**      Level: Medium      Tags: [DP, Sequence DP, Status DP]
      

和House Robber I 类似, 搜刮房子, 相邻不能动. 特点是: 现在nums排成了圈, 首尾相连.

#### Sequence DP
- dp[i][status]: 在 status=[0,1] 情况下, 前i个 房子拿到的 max rob gain. status=0, 1st house robbed; status=1, 1st house skipped
- 根据dp[i-1]是否被rob来讨论dp[i]: dp[i] = Math.max(dp[i-1], dp[i - 2] + nums[i - 1]);
- 特别的是，末尾的last house 和 first house相连. 这里就需要分别讨论两种情况: 第一个房子被搜刮, 或者第一个房子没被搜刮
- be careful with edge case nums = [0], only with 1 element.
- Time,space: O(n)

#### 两个状态
- 是否搜刮了第一个房子, 分出两个branch, 可以看做两种状态.
- 可以考虑用两个DP array; 也可以加一dp维度, 补充这个状态.
- 连个维度表示的是2种状态(1st house being robbed or not); 这两种状态是平行世界的两种状态, 互不相关.

#### Rolling array
- 与House Robber I一样, 可以用%2 来操作rolling array, space reduced to O(1)



---

**94. [House Robber III.java](https://github.com/awangdev/LintCode/blob/master/Java/House%20Robber%20III.java)**      Level: Medium      Tags: [DFS, DP, Status DP, Tree]
      

Houses被arrange成了binary tree, 规则还是一样, 连续相连的房子不能同时抄.

求Binary Tree neighbor max 能抄多少.

#### DFS
- 判断当下的node是否被采用，用一个boolean来表示. 
- 如果curr node被采用，那么下面的child一定不能被采用.
- 如果curr node不被采用，那么下面的children有可能被采用，但也可能略过，所以这里用Math.max() 比较一下两种可能有的dfs结果。
- dfs重复计算:每个root都有4种dive in的可能性, 假设level高度是h, 那么时间O(4^(h)), where h = logN, 也就是O(n^2)

#### DP, DFS
- 并不是单纯的DP, 是在发现DFS很费劲后, 想能不能代替一些重复计算?
- 基本思想是dfs解法一致: 取root找最大值, 或者不取root找最大值
- 在root上DFS, 不在dfs进入前分叉; 每一个level按照状态来存相应的值: dp[0] root not picked, dp[1] root picked.
- Optimization: DP里面, 一口气找leftDP[]会dfs到最底层, 然后自下向上做计算
- 这个过程里面, 因为没有在外面给dfs()分叉, 计算就不会重叠, 再也不用回去visit most-left-leaf了, 算过一遍就完事.
- 然而, 普通没有dp的dfs, 在算完visited的情况下的dfs, 还要重新dfs一遍!visited的情况.
- Space O(h), time O(n), 或者说是O(2^h), where h = log(n)

#### DP 特点
- 不为状态而分叉dfs
- 把不同状态model成dp
- 每一个dfs都return一个based on status的 dp array.
- 等于一次性dfs计算到底, 然后back track, 计算顶部的每一层.
- DP 并不一定要是以n为base的. 也可以是局部的去memorize状态->value.



---

**95. [Permutation in String.java](https://github.com/awangdev/LintCode/blob/master/Java/Permutation%20in%20String.java)**      Level: Medium      Tags: [Two Pointers]
      

#### Two Pointer
- 如果做s1的permudation, 时间复杂度是O(n!) 肯定不可以
- 这里用HashTable的做法 (因为26字母, 所以用int[26]简化) 来记录window内的 character count
- 如果window内的character count 相等, 那么就是permudation
- 更进一步优化: 找两个map相互对应, 不如用一个 int[26]: s1对遇到的character做加法, s2对遇到的character做减法
- two pointer 运用在 n1, n2 的把控; 以及 s2.charAt(i - n1) 这一步



---

**96. [Permutations II.java](https://github.com/awangdev/LintCode/blob/master/Java/Permutations%20II.java)**      Level: Medium      Tags: [Backtracking]
      

给一串数组, 找出所有permutation数组. 注意: 给出的nums里面有重复数字, 而permutation的结果需要无重复.

#### Backtracking
- 排序, 
- Mark visited. 通过permutation规律查看是否排出了重复结果
- 并且要检查上一层recursive时有没有略过重复element
- time O(n!)

##### 背景1
- 在recursive call里面有for loop, 每次从i=0开始, 试着在当下list上加上nums里面的每一个。    
- 从i=0开始，所以会依次recursive每一个nums：
- 因此，例如i=2,肯定比i=3先被访问。也就是:取i=2的那个list permutation肯定先排出来。   

##### 背景2
- 重复的例子：给出Input[x, y1, y2], 假设y的值是一样的。那么，{x,y1,y2}和{x,y2,y1}是相同结果。

##### Note
- 综上，y1肯定比y2先被访问,{x,y1,y2}先出。 紧随其后，在另一个recursive循环里，{x,y2...}y2被先访问，跳过了y1。    
- 重点:规律在此，如果跳过y1，也就是visited[y1] == false, 而num[y2] == num[y1]，那么这就是一个重复的结果，没必要做，越过。
- 结果:那么，我们需要input像{x,y1,y2}这样数值放一起，那么必须排序。

#### Non-recursive, manuall swap
- Idea from: https://www.sigmainfy.com/blog/leetcode-permutations-i-and-ii.html
- 用到 sublist sort
- 用 swap function, 在原数组上调节出来新的permutation
- 注意: 每次拿到新的candidate, 都要把没有permutate的数位sort, 然后再开始swap.
- 这是为了确保, [j]和[j-1]在重复时候, 不用重新记录.

#### Queue
- 给一个visited queue
- 和queue在所有的地方一同populate. 
- 然后visited里面存得时visited indexes。 (Not efficient code. check again)



---

**97. [Shuffle an Array.java](https://github.com/awangdev/LintCode/blob/master/Java/Shuffle%20an%20Array.java)**      Level: Medium      Tags: [Permutation]
      

像shuffle music 一样, 做一套shuffle array的functions: 

shuffle() 给出random的permutation

reset() 给出最初的nums

#### Permutation
- Permutation 实际上就是在list/array/... 上面给元素换位置
- 硬换位置, 每次换的位置不同, 用random来找到要换的index
- 维持同一个random seed
- O(n)

##### Note
- compute all permutations 太慢, 不可行.



---

**98. [Group Anagrams.java](https://github.com/awangdev/LintCode/blob/master/Java/Group%20Anagrams.java)**      Level: Medium      Tags: [Hash Table, String]
      

给一串string, return list of list, 把anagram 放在一起.

#### Hash Table, key 是 character frequency
- 存anagram
- 用 character frequency 来做unique key
- 用固定长度的char[26] arr 存每个字母的frequency; 然后再 new string(arr).   
- 因为每个位子上的frequency的变化，就能构建一个unique的string
- O(nk), k = max word length


#### Hash Table, key 是 sorted string
- 和check anagram 想法一样：转化并sort char array，用来作为key。
- 把所有anagram 存在一起。注意结尾Collections.sort().
- O(NKlog(K)), N = string[] length, k = longest word length    




---

**99. [Backpack.java](https://github.com/awangdev/LintCode/blob/master/Java/Backpack.java)**      Level: Medium      Tags: [Backpack DP, DP]
      

给i本书, 每本书有自己的重量 int[] A, 背包有自己的大小M, 看最多能放多少重量的书?

#### Backpack DP 1
- 简单直白的思考 dp[i][m]: 前i本书, 背包大小为M的时候, 最多能装多种的书?
- **注意**: 背包问题, 重量weight一定要是一维.
- dp[i][j] = Math.max(dp[i][j], dp[i - 1][j - A[i - 1]] + A[i - 1]);
- 每一步都track 最大值
- 最后return dp[n][m]
- 时间空间  O(mn)
- Rolling array, 空间O(m)

#### Backpack DP 2
- true/false求解, 稍微曲线救国: 重点是, 最后, 按照weight从大到小遍历, 第一个遇到true的, index就是最大值.  
- 考虑: 用i个item (可跳过地取), 是否能装到weight w?
- 需要从'可能性'的角度考虑, 不要搞成单一的最大值问题.
- 1. 背包可装的物品大小和总承重有关.
- 2. 不要去找dp[i]前i个物品的最大总重, 找的不是这个. 
    dp[i]及时找到可放的最大sum, 但是i+1可能有更好的值, 把dp[i+1]变得更大更合适.

##### 做法
- boolean[][] dp[i][j]表示: 有前i个item, 用他们可否组成size为j的背包? true/false.
- (反过来考虑了，不是想是否超过size j, 而是考虑是否能拼出exact size == j)
- **注意**: 虽然dp里面一直存在i的位置, 实际上考虑的是在i位置的时候, 看前i-1个item.

##### 多项式规律
- 1. picked A[i-1]: 就是A[i-1]被用过, weight j 应该减去A[i-1]. 那么dp[i][j]就取决于dp[i-1][j-A[i-1]]的结果.
- 2. did not pick A[i-1]: 那就是说, 没用过A[i-1], 那么dp[i][j]就取决于上一行d[i-1][j]
- dp[i][j] = dp[i - 1][j] || dp[i - 1][j - A[i - 1]]

##### 结尾
- 跑一遍dp 最下面一个row. 从末尾开始找, 最末尾的一个j (能让dp[i][j] == true)的, 就是最多能装的大小 :)   
- 时间，空间都是：O(mn)




---

**100. [Backpack II.java](https://github.com/awangdev/LintCode/blob/master/Java/Backpack%20II.java)**      Level: Medium      Tags: [Backpack DP, DP]
      

给i本书, 每本书有自己的重量 int[] A, 每本书有value int[] V

背包有自己的大小M, 看最多能放多少value的书?

#### Backpack DP
- 做了Backpack I, 这个就如出一辙, 只不过: dp存的不是max weight, 而是 value的最大值.
- 想法还是，选了A[i - 1] 或者没选A[i - 1]时候不同的value值.
- 时间空间O(mn)
- Rolling Array, 空间O(m)

#### Previous DP Solution
- 如果无法达到的w, 应该mark as impossible. 一种简单做法是mark as -1 in dp. 
- 如果有负数value, 就不能这样, 而是要开一个can[i][w]数组, 也就是backpack I 的原型.
- 这样做似乎要多一些代码, 好像并不是非常需要




---

**101. [Backpack V.java](https://github.com/awangdev/LintCode/blob/master/Java/Backpack%20V.java)**      Level: Medium      Tags: [Backpack DP, DP]
      

#### Backpack DP
- 与背包1不同: 这里不是check可能性(OR)或者最多能装的size是多少; 而是计算有多少种正好fill的可能性.
- dp[i][w]: 用前i本书, 正好fill到 w weight的可能性.
- 对于末尾, 还是两种情况:
- 1. i-1位置没有加bag
- 2. i-1位置加了bag
- 两种情况可以fill满w的情况加起来, 就是我们要的结果.
- 如常: dp[n + 1][w + 1]
- 重点: dp[0][0] 表示0本书装满weight=0的包, 这里我们必须 dp[0][0] = 1, 给后面的 dp function 做base
- Space, time: O(MN)
- Rolling array, 空间优化, 滚动数组. Space: O(M)

#### 降维打击, 终极优化
- 分析row(i-1)的规律, 发现所有row(i)的值, 都跟row(i-1)的左边element相关, 而右边element是没用的.
- 所以可以被override.
- Space: O(M), 真*一维啊!
- Time: O(MN)



---

**102. [Evaluate Reverse Polish Notation.java](https://github.com/awangdev/LintCode/blob/master/Java/Evaluate%20Reverse%20Polish%20Notation.java)**      Level: Medium      Tags: [Stack]
      

给一个 RPN string list, 根据这个list, 计算结果.

#### Stack
- stack 里面 存数字
- 每次遇到operator, 都拿前2个数字计算
- 计算结果存回到stack里面, 方便下一轮使用.
- Time,Space O(n)




---

**103. [Insertion Sort List.java](https://github.com/awangdev/LintCode/blob/master/Java/Insertion%20Sort%20List.java)**      Level: Medium      Tags: [Linked List, Sort]
      

input一串数字, 需要出sorted output. 每次insert一个数字时, 都要放到正确的sorted的位置

每次insertion的时候, 都从input里面减掉这个数字

#### Linked List
- 把list里面每个元素都拿出来，scan and insert一遍
- Time O(n^2), worst case, 每次放入n个数字里面的element, 刚好都是最大的
- 所以每次要traverse n nodes, 然后走n次

##### 思考方法
- 如果已经有个sorted list, insert一个element进去。怎么做？
- while 里面每个元素都小于 curr, keep going
- 一旦curr在某个点小了，加进去当下这个空隙。



---

**104. [Interleaving Positive and Negative Numbers.java](https://github.com/awangdev/LintCode/blob/master/Java/Interleaving%20Positive%20and%20Negative%20Numbers.java)**      Level: Medium      Tags: [Two Pointers]
      

给一串数组 有正负数. 重新排列, 让数组里面 正数 和 负数 相隔开. 原来的order无所谓

#### Two pointer
- 需要知道正负的位置, 所以排序 O(nlogN)
- 考虑: 正数多还是负数多的问题, 举栗子就看出来端倪了
- 然后Two Pointer, swap 
- Time O(nlogn), space O(n)

#### extra space
- 用extra O(n) space, 把正负分成两个list
- 然后分别按照index填回去
- time O(n). space O(n)
- 但是就么有用到Two pointer了



---

**105. [Largest Number.java](https://github.com/awangdev/LintCode/blob/master/Java/Largest%20Number.java)**      Level: Medium      Tags: [Sort]
      

给一串数字, 非负数, 把所有数字串联起来, 组成最大数字.

因为结果很大, 所以用string表示 

#### Sort, Comparator
- 考虑 more significant spot 应该拿到更大的值
- 如果sort number,  comparator 会比较难写: 每个digit的weight不同, 要分别讨论个位数和多位数.
- goal: 让较大的组合数排在前面, 让较小的组合数排在后面
- 不如: 组合两种情况, 用String比较一下大小 (也可以用 integer来比较组合数, 但是为保险不超Integer.MAX_VALUE, 这里比较String)
- String.compareTo() 是按照 lexicographically, 字典顺序排列的
- 利用compareTo, 来倒序排列 string, 刚好就得到我们要的结果.
- O(nlogn), 排序



---

**106. [Longest Common Substring.java](https://github.com/awangdev/LintCode/blob/master/Java/Longest%20Common%20Substring.java)**      Level: Medium      Tags: [DP, Double Sequence DP, Sequence DP, String]
      

#### Double Sequence DP
- 两个string, 找最值: longest common string length
- 序列型, 并且是双序列, 找两个序列 (两维的某种性质)
- dp[i][j]: 对于 A 的前i个字母, 对于 B 的前j个字母, 找最长公共substring的长度
- dp = new int[m + 1][n + 1]
- dp[i][j] = dp[i - 1][j - 1] + 1; only if A.charAt(i - 1) == B.charAt(j - 1)
- 注意track max, 最后return
- space O(n^2), time(n^2)

##### Rolling array
- 空间优化, [i] 只有和 [i - 1] 相关, 空间优化成 O(n)

#### String
- 找所有A的substring, 然后B.contains()
- track max substring length
- O(n^2) time



---

**107. [Longest Increasing Continuous subsequence II.java](https://github.com/awangdev/LintCode/blob/master/Java/Longest%20Increasing%20Continuous%20subsequence%20II.java)**      Level: Medium      Tags: [Array, Coordinate DP, DP, Memoization]
      

#### Coordinate DP
- due to access permission, not test
- dp[i][j]: longest continuous subsequence length at coordinate (i, j)
- dp[i][j] should come from (i-1,j) and (i, j-1).
- dp[0][0] = 1
- condition: from up/left, must be increasing
- return dp[m-1][n-1]

#### Memoization
- O(mn) space for dp and flag.
- O(mn) runtime because each spot will be marked once visited. 
- 这个题目的简单版本一个array的例子：从简单题目开始想DP会简单一点。每个位置，都是从其他位置（上下左右）来的dpValue +　１.　如果啥也没有的时候，init state 其实都是1， 就一个数字，不增不减嘛。




---

**108. [Maximum Subarray II.java](https://github.com/awangdev/LintCode/blob/master/Java/Maximum%20Subarray%20II.java)**      Level: Medium      Tags: [Array, DP, Greedy, PreSum, Sequence DP, Subarray]
      

给一串数组, 找数组中间 两个不交互的 subarray 数字之和的最大值

#### DP
- 考虑两个方向的dp[i]: 包括i在内的subarray max sum. 
- dp[i] 的特点是: 如果上一个 dp[i - 1] + nums[i - 1] 小于 nums[i-1], 那么就舍弃之前, 从头再来:
- dp[i] = Math.max(dp[i - 1] + nums.get(i - 1), nums.get(i - 1));
- 缺点: 无法track全局max, 需要记录max.
- 因为我们现在要考虑从左边/右边来的所有max, 所以要记录maxLeft[] 和 maxRight[] 
- maxLeft[i]: 前i个元素的最大sum是多少 (不断递增); maxRight反之, 从右边向左边
- 最后比较maxLeft[i] + maxRight[i] 最大值
- Space, Time O(n)
- Rolling array, reduce some space, but can not reduce maxLeft/maxRight

#### preSum, minPreSum
- preSum是[0, i] 每个数字一次加起来的值
- 如果维持一个minPreSum, 就是记录[0, i]sum的最小值(因为有可能有负数)
- preSum - minPreSum 就是在 [0, i]里, subarray的最大sum值
- 把这个最大subarray sum 记录在array, left[] 里面
- right[] 是一样的道理
- enumerate一下元素的排列顺位, 最后 max = Math.max(max, left[i] + right[i + 1])



---

**109. [Reverse Linked List II .java](https://github.com/awangdev/LintCode/blob/master/Java/Reverse%20Linked%20List%20II%20.java)**      Level: Medium      Tags: [Linked List]
      

reverse 一个 linked list 中  [m ~ n] 的一部分.

#### Reverse linked list
- 在基本的reverse linked list 上面 多了一层: 找到front node,  接下来的 [m ~ n] node 需要被reverse
- 只需要reverse中间的部分.
- Reverse的时候: 用一个dummyNode, 这道题里面, 其实就用 nodeFront, 那么 dummy.next 就是整个reversed list.

##### 注意
- 一定要Mark开头的那个mth node, 最后用它接上 剩下node tail. 不然后面的node会断掉

#### Previous notes
- 遍历到M前，
- 存一下那个点，
- 从M开始， for loop， reverse [m~n]。 然后把三段链接在一起。




---

**110. [Lowest Common Ancestor of a Binary Tree.java](https://github.com/awangdev/LintCode/blob/master/Java/Lowest%20Common%20Ancestor%20of%20a%20Binary%20Tree.java)**      Level: Medium      Tags: [DFS, Tree]
      

给一个Binary Tree root, 以及两个node p, q. 找 p 和 q 的 lowest common ancestor

#### DFS
- 因为是 binary tree, 所以直接盲目搜索搜索path不efficient, use extra space and waste time
- 巧用DFS来找每一个node的common ancestor. 
- Need the assumption: 1. unique nodes across tree; 2. must have a solution
- 当root == null或者 p q 任何一个在findLCA底部被找到了(root== A || root == B)，那么就return 这个root.     
- 三种情况:
- 1. A,B都找到，那么这个level的node就是其中一层的ancestor: 其实，最先recursively return到的那个，就是最底的LCA parent.   
- 2. A 或者 B 找到，那就还没有公共parent, return 非null得那个。   
- 3. A B 都null, 那就找错了没有呗, return null
- Worst case, visit all nodes to find p q at last level, last two leaves: time/space O(n)



---

**111. [Lowest Common Ancestor of a Binary Search Tree.java](https://github.com/awangdev/LintCode/blob/master/Java/Lowest%20Common%20Ancestor%20of%20a%20Binary%20Search%20Tree.java)**      Level: Medium      Tags: [BST, DFS, Tree]
      

给 binary search tree root, q node, p node. 找到p q 的lowest common ancestor

#### Find path with BST
- 利用 BST 的性质，可以直接搜到target node，而做成两个长度不一定相等的list
- 然后很简单找到LCA 
- O(n) space, O(logn) time

#### DFS
- Brutly寻找p和q的common ancestor, 然后recursively drive left/right
- 非常巧妙, 但是也比较局限; 稍微变条件, 就很难recursive.
- 几种情况:
- 1. one of p, q 在leaf, 那么此时的root其实就是lowest common ancestor
- 2. 如果p, q 在root的左右两边, 这就是分叉口, 那么root就是lowest common ancestor
- 3. 如果p,q 在root的同一边 (左,右), 那么继续dfs
- O(1) extra space, O(logn) time



---

**112. [Remove Duplicates from Sorted Array II.java](https://github.com/awangdev/LintCode/blob/master/Java/Remove%20Duplicates%20from%20Sorted%20Array%20II.java)**      Level: Medium      Tags: [Array, Two Pointers]
      

给一个sorted array, 把重复的去掉: 也就是把不重复的按照顺序贴上来, array末尾多余的位置无所谓.

最多可重复出元素的数量不超过2个. return unique item 的长度.

#### Two Pointers
- sorted array, 重复元素都在一起
- 跟 `Remove Duplicates from Sorted Array` 几乎一模一样, 只不过unique index现在可以 validate 2 位
- 其余一模一样, use index to track unique item; skip if duplicated for more than 2 times
- O(n) time, O(1) space
- 这里也可以真的用2个pointers 写while loop, 但是没有必要, 只是单纯地走一个for loop其实就足够.



---

**113. [Remove Duplicates from Sorted List II.java](https://github.com/awangdev/LintCode/blob/master/Java/Remove%20Duplicates%20from%20Sorted%20List%20II.java)**      Level: Medium      Tags: [Linked List]
      

从Linked list 里面摘掉重复元素: 只要重复过, 全部都删掉; 重复出现过得元素一个不留.

#### Linked List
- sorted list, 重复元素都在一起
- 运用 dummyHead: 如果要去掉所有重复元素, 就要有个dummyHead作为局外人在开头牵线
- 只要发现一个 node.val == node.next.val, 就记下这个duplicated val, move forward, 过掉所有重复过的元素
- 思想:
- 用第二个 inner while loop, 把所有的重复元素都处理干净, 然后再move forward
- 优点: outter while loop 不需要考虑太多case, 在inner loop 都把主要的business logic 解决了.

##### 注意DummyHead 的使用
- 当我们有了DummyHead 作为Linked List 的局外线头, 其实可以选择每次遇到duplicate, 就把更加后面的元素 强行assign 给 dummyHead.next 
- 下面还尝试过一种做法: 但是需要考虑的edge case 太多了: 不断移动node, 知道不重复, assign prev.next = node. 
- 这样的做法比较直白, 但是需要考虑很多edge case, 而且并没有很好利用到 dummy head, 注意规避.

##### Previous Note
- 斩草除根。
- 多个node，check node.next ?= node.next.next




---

**114. [QuickSort.java](https://github.com/awangdev/LintCode/blob/master/Java/QuickSort.java)**      Level: Medium      Tags: [Quick Sort, Sort]
      

implement quick sort.

#### Quick Sort
- 首先partition. 返还一个partition的那个中间点的位置: 这个时候, 所有小于nums[partitionIndex] 都应该在 partitionIndex左边
- 然后劈开两半
- 前后各自 quick sort, recursively
- 注意：在partition里面, 比较的时候nums[start] < pivot, nums[end]>pivot, 如果写成了 <= 会 stack overflow.
- Time O(nlogn), Space: O(1)



---

**115. [MergeSort.java](https://github.com/awangdev/LintCode/blob/master/Java/MergeSort.java)**      Level: Medium      Tags: [Merge Sort, Sort]
      

#### Merge Sort
- Divide and conquer, recursively
- 先从中间分段, merge sort 左边 (dfs), merge sort 右边
- 最后merge起来
- merge的时候因为是做int[], 所以没办法必须要O(n) space
- Time O(nlogn), Space O(n)



---

**116. [Binary Tree Level Order Traversal.java](https://github.com/awangdev/LintCode/blob/master/Java/Binary%20Tree%20Level%20Order%20Traversal.java)**      Level: Medium      Tags: [BFS, DFS, Tree]
      

如题.

#### BFS
- 最普通,Non-recursive: BFS, queue, 用个queue.size()来end for loop:换行。   
- 或者用两个queue. 当常规queue empty，把backup queue贴上去

#### DFS
- 每个level都应该有个ArrayList. 那么用一个int level来查看：是否每一层都有了相应的ArrayList。   
- 如果没有，就加上一层。    
- 之后每次都通过DFS在相应的level上面加数字。




---

**117. [Binary Tree Level Order Traversal II.java](https://github.com/awangdev/LintCode/blob/master/Java/Binary%20Tree%20Level%20Order%20Traversal%20II.java)**      Level: Medium      Tags: [BFS, Tree]
      

如题, 但是output要倒序.

#### BFS
- 跟Binary Tree Level Order Traversal一样,只不过存result一直存在存在0位.


#### DFS
- 根据level来append每个list
- rst里面add(0,...)每次都add在list开头



---

**118. [Binary Tree Longest Consecutive Sequence II.java](https://github.com/awangdev/LintCode/blob/master/Java/Binary%20Tree%20Longest%20Consecutive%20Sequence%20II.java)**      Level: Medium      Tags: [DFS, Divide and Conquer, Double Recursive, Tree]
      

找到binary tree 里的最长 consecutive sequence. Sequence可以递增递减, Sequence顺序可以回溯parent.

#### DFS, Divide and Conquer
- Similar to Binary Tree Longest Consecutive Sequence I
- 只不过可以递增递减, 还有连接上parent的方向.
- 对于任何一个节点, 都可能: 
- 1. 自己跟两个child链接, 成为一个sequence
- 2. 左边孩子, 右边孩子各自是一个consecutive sequence, 但是不跟root相连
- main function 一开始就divide成这三份, 然后dfs
- dfs take diff == 1, diff == -1, 来做递增递减的校对.
- dfs rules:
- 1. if node == null, leaf depth = 0
- 2. if not consecutive, reset the depth = 0 (same for both left child, and right child)
- 3. compare the leftDepth && rightDepth to find the maximum
- 4. diff is the same in the same dfs loop to maintain consistant increase/decrease

##### 注意
- dfs的结果很可能是0, 如果没有任何结果, 那么上一层的caller depth = dfs() + 1 = 1
- 那么回归到root, dfs的结果很可能就是1.
- 可能会问: 那么在tree里面的partial sequence (不连接到root)的被忽略了?
- 这里 `longestConsecutive(root.left)` 就很重要了
- 这一步特地忽略掉了root, 然后走下去一层: 因为是recursive, 所以还会继续divde && conquer
- 最后, 任何一层的孩子都会被照顾到.

##### Double Recursive functions
- 用两种recursive的方式handle skip root node的情况
- Recursive using dfs(), basically build child + parent
- Recursive using main function, but with value of child node: skipping root



---

**119. [Combinations.java](https://github.com/awangdev/LintCode/blob/master/Java/Combinations.java)**      Level: Medium      Tags: [Backtracking, Combination, DFS]
      

Given two integers n and k, return all possible combinations of k numbers out of 1 ... n.

#### DFS, Backtracking
- for loop, recursive (dfs).
- 每个item用一次, 下一个level dfs(index + 1)
- Combination DFS. 画个图想想. 每次从1~n里面pick一个数字i
- 因为下一层不能重新回去 [0~i]选，所以下一层recursive要从i+1开始选。



---

**120. [Combination Sum IV.java](https://github.com/awangdev/LintCode/blob/master/Java/Combination%20Sum%20IV.java)**      Level: Medium      Tags: [Array, Backpack DP, DP]
      

给一串数字candidates (no duplicates), 和一个target. 

找到所有unique的 组合(combination) int[], 要求每个combination的和 = target.

注意: 同一个candidate integer, 可以用任意多次.

#### Backpack DP
- 计数问题, 可以想到DP. 其实就是Backpack VI.
- 从x个数字里面找candidate(可以重复用同一个数字), 来sum up to target. 找: # of ways to form the sequence.
- Backpack VI: 给一个数组nums, 全正数, 无重复数字; 找: # of 拼出m的方法
- dp[i]: # of ways to build up to target i
- consider last step: 如果上一步取的是 candidate A, 那么就该加到dp[i]:
- dp[i] += dp[i - A]
- 要找overall dp[i], 就做一个for loop: dp[i] = sum{dp[i - num]}, where for (num: nums)
- Time: O(mn). m = size of nums, n = target
- If we optimize dp for loop, 需要Sort nums. O(mlogm). will efficient 如果m是constant或者relatively small. Overall: O(n)

#### DFS, backtracking
- 尽管思考方式是对的, 但是 times out
- 可以重复使用数字的时候, 比如用1 来拼出 999, 这里用1就可以走999 dfs level, 不efficient



---

**121. [Binary Tree Right Side View.java](https://github.com/awangdev/LintCode/blob/master/Java/Binary%20Tree%20Right%20Side%20View.java)**      Level: Medium      Tags: [BFS, DFS, Tree]
      

给一个binary tree, 从右边看过来, return all visible nodes

#### BFS
- 最右:即level traversal每一行的最末尾.   
- BFS, queue 来存每一行的内容, save end node into list

#### DFS
- Use Map<Level, Integer> 来存每一个level的结果
- dfs function 里, 如果 input depth 不存在, 就add to map.
- dfs function 里面先: dfs(node.right), 然后 dfs(node.left)
- 由于always depth search on right side, 所以map会被right branch populate; 然后才是 leftChild.right




---

**122. [Binary Tree Maximum Path Sum II.java](https://github.com/awangdev/LintCode/blob/master/Java/Binary%20Tree%20Maximum%20Path%20Sum%20II.java)**      Level: Medium      Tags: [DFS, Tree]
      

找到从max path sum from root. 条件: 至少有一个node.

#### DFS
- 比Binary Tree Maximum Path Sum I 简单许多. 因为条件给的更多：at least 1 node + have to start from root
- root一定用到
- 3种情况: curr node, curr+left, curr+right
- 因为一定包括root, 说以从 `dfs(root, sum=0)` 开始, 每个level先加root, sum += root.val



---

**123. [Rotate List.java](https://github.com/awangdev/LintCode/blob/master/Java/Rotate%20List.java)**      Level: Medium      Tags: [Linked List, Two Pointers]
      

给一个single linked list, 右移k steps. k non-negative.

#### Linked List basics
- 记得用dummy.next来存head.
- 特殊: 这里k可能大于list总长. 写一写linked node 移动的步数, 然后 k = k % n.
- 找到newTail, newHead, 然后利用dummy, 换位子



---

**124. [Binary Tree Longest Consecutive Sequence.java](https://github.com/awangdev/LintCode/blob/master/Java/Binary%20Tree%20Longest%20Consecutive%20Sequence.java)**      Level: Medium      Tags: [DFS, Divide and Conquer, Tree]
      

找到binary tree 里的最长 consecutive sequence.

#### DFS
- Divide and Conquer. dfs
- 分开 看左边/右边
- 如果左边满足连续递增的规则, dfs (depth + 1), 如果不满足规则, dfs(depth = 1)
- 右边也是一样
- 对结果跟max作比较, return



---

**125. [Number of Connected Components in an Undirected Graph.java](https://github.com/awangdev/LintCode/blob/master/Java/Number%20of%20Connected%20Components%20in%20an%20Undirected%20Graph.java)**      Level: Medium      Tags: [BFS, DFS, Graph, Union Find]
      

给一个数字n代表n nodes, marked from 1 ~ n, 和一串undirected edge int[][]. 

count这个graph里面有多少个独立的component.

#### Union Find
- 跟Graph Valid Tree 几乎一模一样
- 建造简单的parent[] union find
- 每个edge都union.
- **注意** union 的时候, 只需要union if rootA != rootB

#### DFS
- build graph as adjacent list: Map<Integer, List<Integer>>
- dfs for all nodes of the graph, and mark visited node
- count every dfs trip and that will be the total unions



---

**126. [Next Closest Time.java](https://github.com/awangdev/LintCode/blob/master/Java/Next%20Closest%20Time.java)**      Level: Medium      Tags: [Basic Implementation, Enumeration, String]
      

给一个时间string"12:09", 用里面的4个integer组合成其他时间string, 目标找最小的next time.

如果组合出的time string 在input time之前, 默认 + 24 hours.

#### String
- enumerate all candidates and filter to keep the correct ones
- String.compareTo(string) -> gives lexicographical comparision



---

**127. [Partition Array.java](https://github.com/awangdev/LintCode/blob/master/Java/Partition%20Array.java)**      Level: Medium      Tags: [Array, Quick Sort, Sort, Two Pointers]
      

给一串数字, 和 int k. 根据k的值partition array, 找到第一个i, nums[i] >= k.

#### Two Pointer
- Quick sort的基础. 
- Partition Array根据pivot把array分成两半。
- 从array两边开始缩进。while loop到遍历完。非常直白的implement。
- 注意low/high,或者叫start/end不要越边界
- O(n)
- 注意: 这里第二个inner while `while(low <= high && nums[high] >= pivot) {..}` 采用了 `nums[high] >= pivot`
- 原因是题目要找第一个nums[i] >= k, 也就是说, 即便是nums[i]==k也应该swap到前面去
- 这个跟quick sort 原题有一点点不一样.




---

**128. [Word Ladder.java](https://github.com/awangdev/LintCode/blob/master/Java/Word%20Ladder.java)**      Level: Medium      Tags: [BFS]
      

给一串string[], 需要找shortest distance to change from wordA -> wordB. (限制条件细节见原题)

#### BFS
- 通常, 给一个graph(这道题可以把beginWord看成一个graph的起始node), 找shortest path用BFS
- 在start string基础上，string的每个字母都遍历所有26个字母
- visited 过的 从wordList里去掉
- time: word length m, there can be n candidates => O(mn)
- 但是总是exceed time limit on LeetCode. However, it passes LintCode:
- 原因是 LeetCode给的是list,  list.contains(), list.remove()  都是 O(logn) time!!!
- convert to set first.

#### Trie
- timeout, overkill



---

**129. [Unique Word Abbreviation.java](https://github.com/awangdev/LintCode/blob/master/Java/Unique%20Word%20Abbreviation.java)**      Level: Medium      Tags: [Design, Hash Table]
      


给一个string[] dict, 和一个word. 

每个word都可以缩写成固定的abbreviation `<first letter><number><last letter>`(详细看原题)

检查input word是否满足unique

#### HashMap<string, Set>
- 简单算出abbreviatioin
- 检查abbr是否存在; 如果存在, 是不是input word本身.



---

**130. [Unique Binary Search Tree II.java](https://github.com/awangdev/LintCode/blob/master/Java/Unique%20Binary%20Search%20Tree%20II.java)**      Level: Medium      Tags: [BST, DP, Divide and Conquer, Tree]
      

给一个数字n, 找到以(1...n)为node的所有unique BST.

#### BST
- 根据BST规则, divide and conquer
- 取一个value, 然后分两半(start, value - 1), (value + 1, end) 分别dfs
- 然后左右两边的结果cross match

#### DP? Memoization?



---

**131. [Ugly Number.java](https://github.com/awangdev/LintCode/blob/master/Java/Ugly%20Number.java)**      Level: Medium      Tags: [Math]
      

LeetCode: 判断数字是否是ugly number. (definition: factor only have 2, 3, 5)

#### Math
- 看是否可以整除. 
- 看整除最终结果是否== 1

LintCode: 找kth ugly number, 应该与 Ugly Number II是一样的

- 方法1: PriorityQueue排序。用ArrayList check 新的ugly Number是否出现过。
- 方法1-1：(解释不通，不可取)用PriorityQueue排序。神奇的3，5，7走位：按照题目答案的出发，定了3，5，7以什么规律出现。但是题目并没有特殊表明。
- 方法2: DP . Not Done yet.




---

**132. [Top K Frequent Words.java](https://github.com/awangdev/LintCode/blob/master/Java/Top%20K%20Frequent%20Words.java)**      Level: Medium      Tags: [Hash Table, Heap, MaxHeap, MinHeap, PriorityQueue, Trie]
      
time: O(nlogk)
space: O(n)

给一串String. 找到top k frequent words.

#### PriorityQueue - Min Heap
- O(n) space of map, O(nlogk) to build queue.
- limit minHeap queue size to k: add to queue if found suitable item; always reduce queue if size > k

#### PriorityQueue - Max Heap
- 用HashMap存frequency, 用ArrayList存lists of words
- create一个Node class, 然后用PriorityQueue.   
- PriorityQueue里面用到了 String.compareTo(another String).巧妙。
- time: PQ uses O(nlogn), overall O(nlogn)
- slower, because the maxHeap needs to add all candidates

#### Trie && MinHeap屌炸天   
- 可以做一下
- http://www.geeksforgeeks.org/find-the-k-most-frequent-words-from-a-file/

#### HashMap + collections.sort()
- 用HashMap存frequency, 用ArrayList存lists of words。最后返回从尾部向前数的k个。   
- 注意排序时Collection.sort()的cost是O(nLogk)
- not efficient




---

**133. [Segment Tree Build.java](https://github.com/awangdev/LintCode/blob/master/Java/Segment%20Tree%20Build.java)**      Level: Medium      Tags: [Binary Tree, Divide and Conquer, Lint, Segment Tree]
      

给一个区间[startIndex, endIndex], 建造segment tree structure, return root node.

#### Segment Tree definition
- Recursively build the binary tree
- 左孩子：（A.left, (A.left+A.rigth)/2）   
- 右孩子：（(A.left+A.rigth)/2＋1， A.right）   



---

**134. [Segment Tree Build II.java](https://github.com/awangdev/LintCode/blob/master/Java/Segment%20Tree%20Build%20II.java)**      Level: Medium      Tags: [Binary Tree, Divide and Conquer, Lint, Segment Tree]
      

给一个array, 建造segment tree structure, 

每个treeNode 里面存这个range里的 max value, return root node.

#### Segemnt Tree
- 给的是Array. 注意找区间内的max, assign给区间. 其余和普通的segment tree build一样   
- 注意, segment tree是根据array index range 排位: 根据index in [0, array.length - 1]割开区间, break到底
- 最终start==end做结尾
- 这道题要trackmax, 那么在leaf node assign max=A[start] or A[end]
- 往上,parent一层的max:就是比较左右孩子,其实都是在两个sub-tree里面比较sub-tree的max。   

- Devide and Conquer
- 先分，找到left/right，比较max,在create current node,再append到当前node上面。
- 实际上是depth-first, 自底向上建立起的。



---

**135. [Segment Tree Query.java](https://github.com/awangdev/LintCode/blob/master/Java/Segment%20Tree%20Query.java)**      Level: Medium      Tags: [Binary Tree, DFS, Divide and Conquer, Lint, Segment Tree]
      

给了segment Tree, node里面有Max value, 找[start,end]里面的max

#### Segment Tree, Divide and Conquer
- 根据[start,end]跟 mid of (root.start, root.end) 做比较:
- 简单的2个case: [start,end]全在mid左, 或者[start, end]全在mid右
- 稍微复杂的3rd case: [start, end]包含了mid, 那么就break into 2 queries
- [start, node.left.end], [node.right.start, end]



---

**136. [Segment Tree Modify.java](https://github.com/awangdev/LintCode/blob/master/Java/Segment%20Tree%20Modify.java)**      Level: Medium      Tags: [Binary Tree, DFS, Divide and Conquer, Lint, Segment Tree]
      

给一个segmentTree, node里面存max. 写一个modify function: modify(node, index, value).

#### Segment Tree, Divide and Conquer
- Recursively 在segment tree里面找index, update it with value.   
- 每个iteration，很可能（要么左手，要么右手）max就变了。所以每次都left.max and right.max compare一下
- 最后轮回到头顶，头顶一下包括头顶，就全部都是max了



---

**137. [Segment Tree Query II.java](https://github.com/awangdev/LintCode/blob/master/Java/Segment%20Tree%20Query%20II.java)**      Level: Medium      Tags: [Binary Tree, DFS, Divide and Conquer, Lint, Segment Tree]
      

#### Segment Tree
- 和 Segment Tree Query I 以及其他Segment Tree类似: 这个SegmentTreeNode return count of elements in range
- 这个题目考了validate input source：input 的start,end可能超出root[start,end]。   
- 那么第一步就要先clear一下: 1. 完全不在range就return 0. 2. 有range重合就规整到root的range.




---

**138. [ColorGrid.java](https://github.com/awangdev/LintCode/blob/master/Java/ColorGrid.java)**      Level: Medium      Tags: [Design, Hash Table]
      

#### basic implementation
- 用HashMap， 理解题目规律，因为重复的计算可以被覆盖，所以是个优化题。没有什么太大的悬念和意义.
- 消灭重合点:       
- 如果process当下col, 其实要减去过去所有加过的row的交接点。。。     
- 再分析，就是每次碰到row 取一个单点, sumRow += xxx。       
- 然后process当下col时候， sum += colValue * N - sumRow. 就等于把交叉所有row（曾经Process过的row）的点减去了。很方便。
- 最后read in 是O(P),  process也是O(P).




---

**139. [Container With Most Water.java](https://github.com/awangdev/LintCode/blob/master/Java/Container%20With%20Most%20Water.java)**      Level: Medium      Tags: [Array, Two Pointers]
      

#### Two Pointers
- 木桶理论。盛水的最高取决于最低的那面墙。
- 左右两墙，往中间跑动。
- 另:若一面墙已经小于另外一面，就要移动，换掉矮墙（可能下一面更高，或更低)
- 但决不能换掉当下的高墙，因为低墙已经limit的盛水的上限，若高墙移动，导致两墙之间距离减少，就注定水量更少了。（弄啥来，不能缺心眼啊）



---

**140. [Copy List with Random Pointer.java](https://github.com/awangdev/LintCode/blob/master/Java/Copy%20List%20with%20Random%20Pointer.java)**      Level: Medium      Tags: [Hash Table, Linked List]
      
time: O(n)
space: O(1)

deep copy linked list. linked list 上有random pointer to other nodes.

#### HashMap, Linked List
- Basic Implementation of copy linked list:
- use node and dummy to hold new list, 遍历head.next .... null.    
- Map 在这里用来: 1. avoid creating same node; 2. return the item if existing
- map 的 key全部是old object, 新的key全部是 newly created object
- 每一步都check map里面有没有head. 没有? 加上
- 每一步都check map里面有没有head.random. 没有? 加上



---

**141. [Encode and Decode Strings.java](https://github.com/awangdev/LintCode/blob/master/Java/Encode%20and%20Decode%20Strings.java)**      Level: Medium      Tags: [String]
      

如题.

#### String
- 'word.length()#word' 这样encode, 可以避免遇到#
- 基于我们自己定的规律, 在decode的里面不需要过多地去check error input, assume所有input都是规范的.    
- decode就是找"#",然后用"#"前的数字截取后面的string.




---

**142. [Fast Power.java](https://github.com/awangdev/LintCode/blob/master/Java/Fast%20Power.java)**      Level: Medium      Tags: [DFS, Divide and Conquer]
      

如题: Calculate the a^n % b where a, b and n are all 32bit integers.

#### Divide and Conquer
- a^n可以被拆解成(a*a*a*a....*a)， 是乘机形式，而%是可以把每一项都mod一下的。所以就拆开来take mod.
- 这里用个二分的方法，recursively二分下去，直到n/2为0或者1，然后分别对待. 
- 注意1: 二分后要conquer，乘积可能大于Integer.MAX_VALUE, 所以用个long.
- 注意2: 要处理n%2==1的情况，二分时候自动省掉了一份 a，要乘一下。




---

**143. [Find the Connected Component in the Undirected Graph.java](https://github.com/awangdev/LintCode/blob/master/Java/Find%20the%20Connected%20Component%20in%20the%20Undirected%20Graph.java)**      Level: Medium      Tags: [BFS, DFS]
      

给一个undirected graph, return 所有的component. (这道题找不到了)  

#### BFS
- BFS遍历，把每个node的neighbor都加进来. 
- 一定注意要把visit过的node Mark一下。因为curr node也会是别人的neighbor，会无限循环。      
- Component的定义：所有Component内的node必须被串联起来via path (反正这里是undirected, 只要链接上就好)     
- 这道题：其实component在input里面都已经给好了，所有能一口气visit到的，全部加进queue里面，他们就是一个component里面的了。     
- 而我们这里不需要判断他们是不是Component

#### DFS
- DFS 应该也可以 visit all nodes, mark visited.



---

**144. [HashWithCustomizedClass(LinkedList).java](https://github.com/awangdev/LintCode/blob/master/Java/HashWithCustomizedClass(LinkedList).java)**      Level: Medium      Tags: [Hash Table]
      

练习HashMap with customized class. functions: get(), put(), getRandom() 

#### Hash Table
- store map as array: `Entry<K,V>[] table;`
- store entry as linked list: `public Entry(K key, V value, Entry<K,V> next)`
- compute hashKey: `Math.abs(key.hashCode()) % this.capacity`
- Handle collision:
- 1. Check if duplicate (matching key), if so, replace and return
- 2. Check through the linked list, find find duplicate (matching key), replace and return.
- 3. If no duplicate, add the entry to the tail
- Find item: compute hashKey -> find linked list -> iterate over list to find a matching key.



---

**145. [Interval Minimum Number.java](https://github.com/awangdev/LintCode/blob/master/Java/Interval%20Minimum%20Number.java)**      Level: Medium      Tags: [Binary Search, Divide and Conquer, Lint, Segment Tree]
      

给一串数字 int[], 然后一个query Interval[], 每个interval是 [start, end], 找query 区间里的最小值.

#### Segment Tree
- SegtmentTree, methods: Build, Query. 这题是在SegmentTreeNode里面存min.
- 类似的有存:max, sum, min



---

**146. [Interval Sum.java](https://github.com/awangdev/LintCode/blob/master/Java/Interval%20Sum.java)**      Level: Medium      Tags: [Binary Search, Lint, Segment Tree]
      

给一串数字 int[], 然后一个query Interval[], 每个interval是 [start, end], 找query 区间里的sum.

#### Segment Tree + Binary Search
- 其实是segment tree 每个node上面加个sum
- 记得Segment Tree methods: Build, Query
- Note: 存在SegmentTreeNode里面的是sum.  其他题目可能是min,max,count ... or something else.



---

**147. [Kth Smallest Element in a BST.java](https://github.com/awangdev/LintCode/blob/master/Java/Kth%20Smallest%20Element%20in%20a%20BST.java)**      Level: Medium      Tags: [BST, DFS, Stack, Tree]
      

#### Iterative + stack: inorder traversal
- 很容想到Inorder-binary-search-tree Traversal
- Iterative 稍微难想点：先把最左边的add， pop() stack， 加上右边（如果存在）； 下一个轮回，如果又左孩子，又是一顿加。

#### Recursive + DFS
- 然后稍微优化一下，确保rst.size() == k 时候，就可以return了
- check leaf => dfs left => add root => dfs right



---

**148. [Majority Element II.java](https://github.com/awangdev/LintCode/blob/master/Java/Majority%20Element%20II.java)**      Level: Medium      Tags: [Array]
      

#### Sort + count
- O(nlogN)

#### Two counters
- O(n), count and track valueA, valueB
- count overall apperance at the end for the two items
- save to result
- 注意: 按照if statement的顺序, valA&&countA 比valB&&countB有优先性



---

**149. [Partition List.java](https://github.com/awangdev/LintCode/blob/master/Java/Partition%20List.java)**      Level: Medium      Tags: [Linked List, Two Pointers]
      

#### Linked List
- linked list 不能像partitioin array一样从两边遍历
- 把小于value的加在前半段, 把 >= value的加在后半段
- 做法很普通: 建造两个list, midTail pointer, post pointer
- 把满足条件（<x, >=x）的数字分别放到两个list里面
- 记得用dummyNode track head.
- 最终midTail.next = post链接起来。



---

**150. [Peeking Iterator.java](https://github.com/awangdev/LintCode/blob/master/Java/Peeking%20Iterator.java)**      Level: Medium      Tags: [Design]
      

#### Use concept pre cache
- 找一个cache来存next()的值, 也就是: next value的值提前存在cache里面
- 因此peek()的时候, 就可以直接return cache, 而不用做 itt.next()
- 然后每次真的next()的时候, 里取下一个itt.next()维护这个cache

#### Previous notes
- 再一次理解错题意. peek() 就是头顶，但是不一定是最大值啊。
- 总是把PEEK想成了最大值，然后用2 STACK做了最大值的cache，练的一手好双stack，可惜错了。




---

**151. [Rehashing.java](https://github.com/awangdev/LintCode/blob/master/Java/Rehashing.java)**      Level: Medium      Tags: [Hash Table]
      

给一个Hash Table, 是用 linked list 做的. 问题是: capacity太小, collision太多的情况下, 需要double capacity 然后rehash.

#### Hash Table
- 明白hashCode() function的意义: 拿到hashKey的时候, 用hashKey%capacity 来做hash code
- hashcode就是hash map里面的index
- 明白collision handling 的方式, 和如何double capacity而rehashing
- 都是基本操作, 概念实现



---

**152. [Reorder List.java](https://github.com/awangdev/LintCode/blob/master/Java/Reorder%20List.java)**      Level: Medium      Tags: [Linked List]
      

给一个Linked list, reorder: 从head/tail 两个方向 向中间进发, re-order like: one node at a time,

#### Linked List 功能大集合
- reverse list, find mid of list, merge two list
- 先find mid, 然后把 mid.next reverse了, 最后merge 两段.
- 注意, 用完mid.next之后, 一定要 mid.next = null, 不然merge会出问题



---

**153. [Restore IP Addresses.java](https://github.com/awangdev/LintCode/blob/master/Java/Restore%20IP%20Addresses.java)**      Level: Medium      Tags: [Backtracking, DFS, String]
      

给一串数字, 检查是否是valid IP, 如果合理, 给出所有valid 的IP组合方式.

#### Backtracking
- 递归的终点:list.zie() == 3, 解决最后一段
- 递归在一个index上面, pass s.toCharArray()
- validate string要注意leading '0'
- 注意: 递归的时候可以用一个start/level/index来跑路
- 但是尽量不要去改变Input source， 会变得非常confusing.
- note: code有点messy, 因为要考虑IP的valid情况
- 那个'remainValid', 其实是一个对于remain substring的判断优化, 不成立的就不dfs了



---

**154. [Reverse Words in a String.java](https://github.com/awangdev/LintCode/blob/master/Java/Reverse%20Words%20in%20a%20String.java)**      Level: Medium      Tags: [String]
      

#### Break by space, then flip 
- 结尾不能有空格
- trim() output
- 如果Input是 ""的话，split以后就啥也没有了
- 另个题目Reverse Words in String (char[]) 可以in-place, 条件是char[]里面是没有首尾空格.
- Time, Space: O(n)

#### Other methods
- flip entire string, then flip each individual string (代码有点多, 这道题犯不着)



---

**155. [Reverse Words in a String II.java](https://github.com/awangdev/LintCode/blob/master/Java/Reverse%20Words%20in%20a%20String%20II.java)**      Level: Medium      Tags: [String]
      

#### In-place reverse
- reverse用两回. 全局reverse。局部:遇到空格reverse
- 注意ending index: `i == str.length - 1`, 结尾点即使没有' '也要给reverse一下最后一个词




---

**156. [Search a 2D Matrix.java](https://github.com/awangdev/LintCode/blob/master/Java/Search%20a%202D%20Matrix.java)**      Level: Medium      Tags: [Array, Binary Search]
      

给2D matrix, 每行sorted, 每行的首位都大于上一行的末尾. goal: find target from matrix

#### 2D matrix 转1D array
- 一行一行是从小到大, sorted, 连续的, 可以看做1D sorted array
- Binary Search



---

**157. [Search a 2D Matrix II.java](https://github.com/awangdev/LintCode/blob/master/Java/Search%20a%202D%20Matrix%20II.java)**      Level: Medium      Tags: [Binary Search, Divide and Conquer]
      

给matrix, 每一行sorted, 每一列从上往下sorted, 找target是否存在

#### Binary Search
- 根据给定的性质, 其实点选的极端一点: x = 最下面的row, y = 当下一行里面最小的left position. 
- (x,y)在左下角
- 在此情况下, 只能往一个方向运行: 如果小于target, y++; 如果大于target, 那么只能x--
- 每次操作, 都是删掉一行, 或者一列, 再也不需要回头看
- `while (x >= 0 && y < col) {}` 确保不会跑脱
- 同样的方式: 可以从右上角(0, col - 1) 开始, 代码稍微改一改

#### Divide and Conquer?
- TODO



---

**158. [Search for a Range.java](https://github.com/awangdev/LintCode/blob/master/Java/Search%20for%20a%20Range.java)**      Level: Medium      Tags: [Array, Binary Search]
      

给sorted array, 有重复数字, 找跟target重合所在的range.

#### Binary Search
- 2个while loop
- 找first/last occurance
- TODO: Can the code be simplified?




---

**159. [Search Range in Binary Search Tree .java](https://github.com/awangdev/LintCode/blob/master/Java/Search%20Range%20in%20Binary%20Search%20Tree%20.java)**      Level: Medium      Tags: [BST, Binary Tree]
      

给一个BST, integer range (k1, k2), 找range 里面所有的integer.

#### BST
- 等于dfs遍历了所有k1<= x <= k2的x node。
- dfs left, process root, then dfs right
- 这里, 把 left/right/match的情况全部cover了，然后把k1,k2的边框限制好，中间就全部遍历了。



---

**160. [Sort List.java](https://github.com/awangdev/LintCode/blob/master/Java/Sort%20List.java)**      Level: Medium      Tags: [Divide and Conquer, Linked List, Merge Sort, Sort]
      

#### Merge sort
- 1. find middle. 快慢指针
- 2. Sort: 切开两半，先sort前半, 如果先sort了mid.next~end, sort后，中间点mid.next == null，再sort前半段
- 3. Merge:  假设given list A, B 已经是sorted, 然后按照大小，混合。
- 要recursively call sortList() on partial list.

#### Quick sort
- 想做可以看讲义：http://www.jiuzhang.com/solutions/sort-list/
- 但是quick sort不建议用在list上面。
- 排列list, merge sort可能更可行和合理。原因分析在下面， 以及： http://www.geeksforgeeks.org/why-quick-sort-preferred-for-arrays-and-merge-sort-for-linked-lists/



---

**161. [Summary Ranges.java](https://github.com/awangdev/LintCode/blob/master/Java/Summary%20Ranges.java)**      Level: Medium      Tags: [Array]
      

给一串sorted list, 中间有缺数字, return 所有数字的range string (example 看题目)

#### Basic implementation
- 用一个list as the buffer to store candidates
- when: 1. end of nums; 2. not continuous integer => convert list to result



---

**162. [Topological Sorting.java](https://github.com/awangdev/LintCode/blob/master/Java/Topological%20Sorting.java)**      Level: Medium      Tags: [BFS, DFS, Topological Sort]
      

#### Topological Sort BFS
- indegree tracking: Track all neighbors/childrens. 把所有的children都存在 inDegree<label, indegree count>里面
- Process with a queue: 先把所有的root加一遍(indegree == 0)，可能多个root。并且全部加到queue里面。
- BFS with Queue:
- Only when map.get(label) == 0, add into queue && rst. (indegree剪完了, 就是root啦)
- inDegree在这里就 count down indegree, 确保在后面出现的node, 一定最后process.


#### Basics about graph
- 几个graph的condition：   
- 1. 可能有多个root
- 2. directed node, 可以direct backwards.

TODO:
- build`Map<DirectedGraphNode, Integer> inDegree = new HashMap<>();` and include the root itself
- that is more traditional indegree building



---

**163. [Spiral Matrix.java](https://github.com/awangdev/LintCode/blob/master/Java/Spiral%20Matrix.java)**      Level: Medium      Tags: [Array, Enumeration]
      

从(0,0)坐标, 走完spiral matrix, 把结果存在list里.

#### DX, DY
- Basic implementation, array, enumeration
- 写一下position前进的方向: RIGHT->DOWN->LEFT->UP
- 用一个direction status 确定方向
- 写一个compute direction function 改变方向 `(direction + 1) % 4`
- `boolean[][] visited` 来track走过的地方



---

**164. [Construct Binary Tree from Inorder and Postorder Traversal.java](https://github.com/awangdev/LintCode/blob/master/Java/Construct%20Binary%20Tree%20from%20Inorder%20and%20Postorder%20Traversal.java)**      Level: Medium      Tags: [Array, DFS, Divide and Conquer, Tree]
      

#### DFS, Divide and Conquer
- 写个Inorder和Postorder的例子。利用他们分left/right subtree的规律解题。
- Postorder array 的末尾， 就是当下层的root.   
- 在Inorder array 里面找到这个root,就刚好把左右两边分割成left/right tree。
- 这题比较tricky地用了一个helper做recursive。 特别要注意处理index的变化, precisely考虑开头结尾
- runtime: O(n), visit && build all nodes

#### Improvement
- `findMid(arr)` can be replaced with a map<value, index>, no need execute O(n) search at runtime



---

**165. [Generate Parentheses.java](https://github.com/awangdev/LintCode/blob/master/Java/Generate%20Parentheses.java)**      Level: Medium      Tags: [Backtracking, DFS, Sequence DFS, String]
      

#### DFS
- start with empty string, need to go top->bottom
- 取或者不取`(`, `)`
- rule: open parentheses >= close parentheses
- Note: 在DFS时 pass a reference (StringBuffer) and maintain, instead of passing object (String) and re-create every time
- time: O(2^n), pick/not pick, the decision repat for all nodes at every level
- T(n) = 2 * T(n - 1) + O(1)

#### bottom->up DFS
- figure out n=1, n=2 => build n=3, and n=4
- dfs(n-1) return a list of candidates
- add a pair of `()` to the candidates: either in front, at end, or contain the candidates



---

**166. [Strobogrammatic Number II.java](https://github.com/awangdev/LintCode/blob/master/Java/Strobogrammatic%20Number%20II.java)**      Level: Medium      Tags: [DFS, Enumeration, Math, Sequence DFS]
      

TODO: 
1. use list, iterative? keep candidates and populating
2. clean up the dfs code, a bit messy
3. edge case of "0001000" is invalid, right?

#### DFS
- A bit like BFS solution: find inner list, and then combine with outter left/right sides.
- find all solutions, DFS will be easier to write than iterative/BFS
- when n = 1, there can be list of candidates at bottom of the tree, so bottom->up is better
- bottom->up, dfs till leaf level, and return candidates.
- each level, pair with all the candidates
- 其实就是剥皮，一层一层，是一个central-depth-first的，钻到底时候，return n=1,或者n=2的case，然后开始backtracking。
- 难的case先不handle.到底之后来一次overall scan.
- every level have 5 choices of digital pairs to add on sides. Need to do for n-2 times. 
- Time complexity: O(5^n)



---

**167. [Flip Game II.java](https://github.com/awangdev/LintCode/blob/master/Java/Flip%20Game%20II.java)**      Level: Medium      Tags: [Backtracking, DFS, DP]
      

String 只包含 + , - 两个符号. 两个人轮流把consecutive连续的`++`, 翻转成 `--`.

如果其中一个人再无法翻转了, 另一个人就赢. 求: 给出string, 先手是否能赢.

#### Backtracking
- curr player 每走一步, 就生成一种新的局面, dfs on this
- 等到dfs结束, 不论成功与否, 都要backtracking
- curr level: 把"++" 改成 "--"; backtrack的时候, 改回 '--'
- 换成boolean[] 比 string/stringBuilder要快很多, 因为不需要重新生成string.
- ++ 可以走 (n - 1)个位置: 
- T(N) = (N - 2) * T(N - 2) = (N - 4) * (N - 2) * T(N - 4) ... = O(N!)

##### iterate based on "++"
- 做一个String s的 replica: string or stringBuilder
- 每次dfs后, 然后更替里面的字符 "+" => "-"
- 目的只是Mark已经用过的index
- 真正的dfs 还是在 original input string s 身上展开
- 每次都重新生成substring, 并不是很efficient

##### Game theory
- 保证p1能胜利，就必须保持所有p2的move都不能赢
- 或者说, 在知道棋的所有情况时, 只要p2有一种路子会输, p1就一定能走对路能赢.
- 同时，p1只要在可走的Move里面，有一个move可以赢就足够了。
- p1: player1, p2: player2

#### O(N^2) 的 DP
- 需要Game Theory的功底, Nim game. https://www.jiuzhang.com/qa/941/
- http://www.1point3acres.com/bbs/thread-137953-1-1.html
- TODO: https://leetcode.com/problems/flip-game-ii/discuss/73954/Theory-matters-from-Backtracking(128ms)-to-DP-(0ms)



---

**168. [Palindrome Partitioning.java](https://github.com/awangdev/LintCode/blob/master/Java/Palindrome%20Partitioning.java)**      Level: Medium      Tags: [Backtracking, DFS]
      

给个string s, partition(分段)后, 要确保每个partition都是palindrome. 

求所有partition palindrome组合. `list<list<string>>`

#### DFS
- 可以top->bottom: 遍历str, validate substring(start, i); if valid, add as candidate, and dfs; backtrack by remove candidate.
- 也可以bottom->up: 遍历str, validate substring(start, i); if valid, dfs(remaining str), return list of suffix; cross match with curr candidate.

#### DFS Top->Bottom
- 在遍历str的时候，考虑从每个curr spot 到 str 结尾，是能有多少种palindorme?
- 那就从curr spot当个字符开始算，开始backtracking.
- 如果所选不是palindrome， 那move on.
- 若所选的确是palindrome,　加到path里面，DFS去下个level，等遍历到了结尾，这就产生了一种分割成palindrome的串。
- 每次DFS结尾，要把这一层加的所选palindrome删掉，backtracking嘛

#### Optimization
- 可以再每一个dfs level 算 isPalindrome(S), 但是可以先把 boolean[][] isPalin 算出来, 每次O(1) 来用
- 注意: isPalin[i][j] 是 inclusive的, 所以用的时候要认准坐标
- Calculate isPalin[i][j]: pick mid point [0 ~ n]
- expand and validate palindrome at these indexes: `[mid, mid+1]` or `[mid-1][mid+1]`

#### Complexity
- Overall Space O(n^2): 存 isPlain[][]
- Time O(2^n), 每一层都在做 pick/not pick index i 的选择, 所以worst case 2^n. 
- 因为我们的isPalin[][]优化了palindrome的判断O(1), 所以overall Time: O(2^n)



---

**169. [Submatrix Sum.java](https://github.com/awangdev/LintCode/blob/master/Java/Submatrix%20Sum.java)**      Level: Medium      Tags: [Array, Hash Table, PreSum]
      

给一个int[][] matrix, 找一个sub matrix, where the sum == 0.

#### PreSum的思想
- 算出一个右下角点(i,j)到(0,0)的大小: 上一块 + 左一块 + curr node - overlap area
- preSum[i][j]: sum from (0,0) to (i-1,j-1)
- same approach as `subarray sum`: use hashmap to store diff->index; if diff re-appears, that means sum of 0 has occurred
- sequence of calculation: 1. iterate over start row. 2. iterate over end row. 3. iterate over col number (this is where hashmap is stored based on)
- the iteration over col is like a screening: find previous sum and determine result
- Note: 其实并没有真的去找 `== 0` 的解答,而是根据特性来判断 `剩下的/后来加上的一定是0`



---

**170. [Longest Palindromic Substring.java](https://github.com/awangdev/LintCode/blob/master/Java/Longest%20Palindromic%20Substring.java)**      Level: Medium      Tags: [DP, String]
      

给一个string, 找到最长的palindrome substring.

Related: Longest Palindromic Subsequence, Palindrome Partioning II

O(n^2) is not too hard to think of. How about O(n)?

#### String, Palindrome definition
- 从中间劈开, 遍历i: 从n个不同的点劈开: 每次劈开都看是否可以从劈开出作为palindromic的中点延伸
- palindrome两种情况: odd, even palindrome
- Worst case: 整个string都是相同字符，time complexity变成： 1 + 2 +３　＋　．．．　＋n = O(n^2)

#### DP: isPalin[][]
- 穷举double for loop. O(n^2)
- boolean isPalin[i][j], 每次确认有palindrome就记录下来true / false
- 穷举的for loop计算顺序: end point j, and stat point i = [0, j]
- 在计算 isPalin[i][j]的时候, isPalin[i+1][j-1]应该已经计算过了.
- double for loop: O(n^2). slower, because it guarantees O(n^2) due to the for loop

#### O(n) 
- TODO
- https://www.felix021.com/blog/read.php?2040



---

**171. [Longest Palindromic Subsequence.java](https://github.com/awangdev/LintCode/blob/master/Java/Longest%20Palindromic%20Subsequence.java)**      Level: Medium      Tags: [DFS, DP, Interval DP, Memoization]
      

给一个string s, 找最长的sub-sequence which is also palindrome.

注意！subsequence并不是substring, 是可以skip letter / non-continuous character sequence
    
#### Interval DP
- 用[i][j]表示区间的首尾
- 考虑3个情况: 砍头, 砍尾, 砍头并砍尾 (考虑首尾关系)
- Iteration一定是以i ~ j 之间的len来看的. 
- len = j - i + 1; 那么反推, 如果len已知, j = len + i -1;
- 注意考虑len == 1, len == 2是的特殊情况.
- time/space: O(n^2)

#### Memoization
- 同样的方式model dp[i][j]: range [i, j] 之间的  max palindromic length
- 三种情况: 
- 1. 首尾match 继而 dfs[i+1, j-1]
- 2. 首尾不match,dfs[i+1,j] 
- 3. 首尾不match,dfs[i,j-1] 
- 注意: init dp[i][j]=-1, dfs的时候查dp[i][j] 是否算过
- more about dfs: bottom-up, first dive deep into dfs(i+1,j-1) till the base cases.
- time/space: O(n^2)
- prepare dp[n][n]: O(n^2); dfs: visit all combinations of [i,j]: O(n^2)




---

**172. [Gas Station.java](https://github.com/awangdev/LintCode/blob/master/Java/Gas%20Station.java)**      Level: Medium      Tags: [Greedy]
      

给一串gas station array, 每个index里面有一定数量gas.

给一串cost array, 每个index有一个值, 是reach下一个gas station的油耗.

array的结尾地方, 再下一个点是开头, 形成一个circle route.

找一个index, 作为starting point: 让车子从这个点, 拿上油, 开出去, 还能开回到这个starting point

#### Greedy
- 不论从哪一个点开始, 都可以记录总油耗, `total = {gas[i] - cost[i]}`. 最后如果total < 0, 无论从哪开始, 必然都不能走回来
- 可以记录每一步的油耗积累, `remain += gas[i] - cost[i]`
- 一旦 remain < 0, 说明之前的starting point 不合适, 也就是说, 初始点肯定在后面的index. 重设: start = i + 1
- single for loop. Time: O(n)

#### NOT DP
- 看似有点像 House Robber II, 但是问题要求的是: 一个起始点的index
- 而不是求: 最后点可否走完/最值/计数



---

**173. [Triangles.java](https://github.com/awangdev/LintCode/blob/master/Java/Triangles.java)**      Level: Medium      Tags: [Array, Coordinate DP, DFS, DP, Memoization]
      

给一个list<list<Integer>> triangle, 细节原题. 找 min path sum from root.

#### DFS + Memoization
- 其实跟给一个2D matrix没有什么区别, 可以做dfs, memoization.
- initialize memo: pathSum[i][j] = MAX_VALUE; 计算过的path省略
- Bottom-top: 先dfs到最深的path, 然后逐步网上返回
- `OR 原理: min(pathA, pathB) + currNode`
- 浪费一点空间, pathSum[n][n]. space: O(n^2), where n = triangle height
- 时间:O(n^2). Visit all nodes once: 1 + 2 + 3 + .... n = n^2

#### DP
- 跟dfs的原理很像, `OR 原理: min(pathA, pathB) + currNode`
- init dp[n-1][j] = node values
- build from bottom -> top: dp[i][j] = Math.min(dp[i + 1][j], dp[i + 1][j + 1]) + triangle.get(i).get(j);
- 跟传统的coordinate dp有所不同, inner for loop 是需要计算 j <= i, 原因是triangle的性质.
- 空间: dp[n][n]. space: O(n^2)
- 时间:O(n^2). Visit all nodes once: 1 + 2 + 3 + .... n = n^2

#### DP + O(n) space 
- Based on the DP solution: the calculation always depend on `next row` for col at `j` and `j + 1`
- 既然只depend on next row, 可以用rolling array来处理: reduce to O(n) space.
- Further: 可以降维, 把第一维彻底去掉, 变成 dp[n]
- 同样是double for loop, 但是只在乎column changes: `dp[j] = Math.min(dp[j], dp[j + 1]) + triangle.get(i).get(j);`  



---

**174. [Merge Intervals.java](https://github.com/awangdev/LintCode/blob/master/Java/Merge%20Intervals.java)**      Level: Medium      Tags: [Array, PriorityQueue, Sort, Sweep Line]
      

给一串int[Interval] (unsorted), 把所以Interval merge起来.

#### Sweep Line with Priority Queue
- O(nlogn) time (PriorityQueue), O(n) space     
- 扫描线+Count无敌手。注意start end把interval给合起来。   
- count==0的时候，就是每次start end双数抵消的时候，就应该是一个interval的开头/结尾。写个例子就知道了。   
- 记得怎么写comparator. New way: new PriorityQueue<>(Comparator.comparing(p -> p.val));
- 在 LeetCode里面，Sweep Line比方法2要快很多.

#### Sort Interval 
- Sort by interval.start之后，试着跑一遍，按照merge的需求，把需要merge的地方续好，然后减掉多余的interval就好。
- sort by Interval.start: `intervals.sort(Comparator.comparing(interval -> interval.start)); // O(nlogn)`
- Related example: Insert Interval
- 用两个相连的Interval: curr, next
- 如果 curr.end覆盖了 next.start: 需要merge. 那么比较一下 curr.end vs. next.end    
- 一旦merge, 需要remove被覆盖的 next interval: `list.remove(i+1)`
- 若没有重合，就继续iteration
- time O(nlogn), space O(1)

#### Sort Intervals and append end logically
- Sort intervals: O(nlogn), extra space O(n) when creating rst list
- 找到结尾 interval, 满足条件就可以save
- 如果不到return的条件, 就继续延伸 interval.end



---

**175. [H-Index.java](https://github.com/awangdev/LintCode/blob/master/Java/H-Index.java)**      Level: Medium      Tags: [Bucket Sort, Hash Table, Sort]
      

找到h-index, 给的citation int[] 并不是sorted. h-index 的definition 具体看题目.

#### Sort, find h from end
- 例子写出来，发现可以sort以后按照定义搜索一遍。 nlogn.
- 搜索一遍时候可以优化，用binary search. 但是没意义，因为array.sort已经用了nlogn
- 题目给的规则, 从小到大排序后: 剩下的 paper `n-h`, 全部要 <= h 个 citation.
- time O(nlogn), search O(n)

##### 正向思考
- 从i = 0 开始找第一个 `citations[i] >= h`, 就是第一个符合 h-index 规则的paper, return h

##### 反向思考
- 如果从 h = n, 每次h--; 那么 `x = n - h` 就是从 `[0 ~ n)` 开始找第一个 `dictations[x] >= h`, 就是结果
- 同时, `dictations[x-1]` 就是最后一个(dictation最多的)其余的paper.

#### Bucket count / Bucket Sort
- O(n)
- Bucket sort的思想(更像是counting sort?): 过一遍 input, 把dictation value 作为 index, 分布在bucket[index]上++
- bucket[x] 是 count when # of citation == x. 
- 如果 x 大于 n的时候, 就超出了index范围, 但是刚好这个问题可以包容, 把这样的情况记位在bucket[n]就可以
- 巧妙: `sum += bucket[h]` where `h = [n ~ 0]` 利用了h-index的definition:
- #of papers (sum of bucket[n]...bucket[0]) has more than h cidations 
- 这里运用到了bucket sort的思想, 但是并不是sorting, 而h-index的定义运用的很巧妙.
- Read more about actual bucket sort: https://en.wikipedia.org/wiki/Bucket_sort



---

**176. [H-Index II.java](https://github.com/awangdev/LintCode/blob/master/Java/H-Index%20II.java)**      Level: Medium      Tags: [Binary Search]
      

找到h-index, 给的citation int[] 已经sorted. h-index 的definition 具体看题目.

#### Binary Search
- H-index的一个简单版, 已经sorted(从小到大), 找target value
- 按定义, 找最后一个 `dictations[mid] >= h`, where `h = n - mid`
- O(logn)



---

**177. [Sort Colors.java](https://github.com/awangdev/LintCode/blob/master/Java/Sort%20Colors.java)**      Level: Medium      Tags: [Array, Partition, Quick Sort, Sort, Two Pointers]
      

给一串数字 nums, 数字代表颜色[0,1,2]; 要求 sort nums, 数字最终按照大小排列. 

虽然叫sort color, 其实就是sort 这些 numbers, 只不过抽象了一下.

#### partition array, the base of quick sort
- partition the array by pivot k = {0, 1, 2}
- 每一次partition都return starting point of the current partition
- 然后根据下一个 color, 去还没有sort 干净的那个部分, 再sort一下就好
- time O(kn), where k = 0 => O(n)
- 这里只是partion, 并不需要recursively quick sort, 所以结果是简单的O(n)

#### One pass
- have two pointers, left/right
- start tracks red, end tracks blue. Swap red/blue to right position, and left++ or right--.
- leave white as is and it will be sorted automatically
- be very careful with index i: when swapping with index right, we do not know what is nums[right], so need to re-calculate index i .
- O(n)
- Note: this one pass solution does not work if there are more than 3 colors. Need to use the regular quick sorty.

#### Counting sort
- TODO: count occurance and reassign array



---

**178. [Sort Colors II.java](https://github.com/awangdev/LintCode/blob/master/Java/Sort%20Colors%20II.java)**      Level: Medium      Tags: [Partition, Quick Sort, Sort, Two Pointers]
      

Sort Color的普通版, sort all k colors in colors array.

Details 参见: https://github.com/awangdev/LintCode/blob/master/Java/Sort%20Color.java

#### Quick Sort
- O(nk)



---

**179. [Sort Letters by Case.java](https://github.com/awangdev/LintCode/blob/master/Java/Sort%20Letters%20by%20Case.java)**      Level: Medium      Tags: [Partition, Sort, String, Two Pointers]
      

给一串字符(ASCII 大写, 小写字母), 要求sort 小写字母, 在大写字母前面. 

字母间的前后顺序无所谓, 也不需要preserve original order .

跟sort color分成相似.

#### Partition + Two pointers
- 其实就是quick sort里面的partition function的简化版
- Two pointers, 找一个 pivot 'a' 来区分大写小写字母
- ASCII code 里面 大写字母在小写字母前面, 数字更小
- 然后 while, move start++, end--,
- 每一轮都swap

#### Two pointers
- 直接用两个 pointer left/right 标记开头结尾
- 每次遇到 `>= 'a'` 就是小写字母, swap(chars, i, left);
- 每次遇到 `< 'a'` 就是大写字母, swap(chars, i, right);
- 注意: 每次处理完left swap, 任由for loop i++, 因为确定 [0 left] 都是准确的
- 每次处理完 right swap, 我们不确定从 right index 换过来的是不是正确的, 所以 i--, 跟for loop 的 i++抵消.
- 写 while loop 的 solution看起来更容易理解.



---

**180. [Subarray Sum Closest.java](https://github.com/awangdev/LintCode/blob/master/Java/Subarray%20Sum%20Closest.java)**      Level: Medium      Tags: [PreSum, PriorityQueue, Sort, Subarray]
      
time: O(nlogn)
space: O(n)

给一串数字, 找subarray的首尾index, 条件: subarray最接近0.

#### PreSum + index in class
- Can be a 2D array, or a `class Point` to store preSum + index
- Sort preSum: smaller (有可能负数) 靠前, 大数字靠后
- 比较preSum种相连接的两个节点, 找差值min; 因为最接近的两个preSum节点的差值肯定是最小
- min所在的两个节点的index, 就是result candidate: 这两个index可能再原nums里面相差很远
- time O(nlogn), sort
- space: O(n)

#### 为何没有用 map<preSum, index> ?
- 因为map虽然能存 preSum + index, 但是无法有效排序
- 所以用一个class来存这两个信息, 然后合理排序



---

**181. [Task Scheduler.java](https://github.com/awangdev/LintCode/blob/master/Java/Task%20Scheduler.java)**      Level: Medium      Tags: [Array, Enumeration, Greedy, PriorityQueue, Queue]
      

#### Array, count frequency, enumerate
- Enumerate to understand: 1. we can module the tasks in module/section; 2. Only need sum the intervals/slots, not return actual layout
- Perfect condition, all letters appear identical # times: just line them up separate in order.
- Real case: task appears different times
- 1. Place maxCount task as header followed with n slots: define (maxCount-1) sections
- 2. For tasks with less # than maxCount# can fill the (maxCount-1) sections; what about the tail section?
- 3. Any task with same maxTask#, of if prior sections all filled, will fill the tail section
- To count overall slots/intervals, come up with this equation:
- 1. Fixed sections: `(maxCount - 1) * (n + 1)`
- 2. Plus all repeating maxCount tasks: calculate by couting identical maxCount of them
- 3. Exception: if the first (max - 1) sections are all filled completely, and we still have extra task (ex: when n is not large enough), then just return tasks.length
- time O(1), space O(1)

#### PriorityQueue
- 正面去做: 
- summerize 每个task出现的次数, 然后qp sort Task object, count 大的靠前
- 起始每个section: k slots = n + 1
- 目标是穷尽 k, 或者 穷尽 pq (poll k times, but will save it back to queue if Task # > 0)
- 如果qp 真的穷尽, break, return count
- 不然, count + remain of k
- extra space O(x), time O(n) + constant time O(xlogx), where x = 26



---

**182. [Exam Room.java](https://github.com/awangdev/LintCode/blob/master/Java/Exam%20Room.java)**      Level: Medium      Tags: [PriorityQueue, Sort]
      

#### PriorityQueue
- Use priority queue to sort by customized class interval{int dist; int x, y;}. 
- Sort by larger distance and then sort by start index
- seat(): pq.poll() to find interval of largest distance. Split and add new intervals back to queue.
- leave(x): one seat will be in 2 intervals: remove both from pq, and merge to a new interval.
- 主方程写出来其实很好写, 就是 split + add interval, 然后 find + delete interval 而已. 最难的是构建data structure
- seat(): O(logn), leave(): O(n)

##### Trick: 构建虚拟 boundary
- 如果是开头的seat, 或者是结尾的seat, 比较难handle: 一开始坐在seat=0的时候, 没有interval啊!
- Trick就是, 我们自己定义个虚拟的座位 `seat=-1`, `seat=N`
- 一开始有一个 interval[-1, N] 然后就建立了boundary.
- 从此以后, 每次split成小interval的时候:
- 遇到 `interval[-1, y]`, distance就是 `(y - 0)`
- 遇到 `interval[x, N]`, distance就是 `(N - 1 - x)`
- 当然正常的interval dist 就是 `(y - x) / 2`

##### distance 中间点
- Interval.dist 我们其实做的是 distance的中间点 `(y - x) / 2`
- 这里的dist是 `距离两边的距离` 而不是 x, y 之间的距离. 这里要特别注意.

#### TreeSet
- https://leetcode.com/problems/exam-room/discuss/139885/Java-Solution-based-on-treeset/153588

#### Map
- how?
- TODO, not sure.



---

**183. [Anagrams.java](https://github.com/awangdev/LintCode/blob/master/Java/Anagrams.java)**      Level: Medium      Tags: [Array, Hash Table]
      

把anagram找到并output

#### HashMap
- 存在int[26], Arrays.toString(arr) 就是 string key: character frequency map
- anagram都有一样的key, 存进hashmap<string, list of anagrams>
- output anagrams

#### HashMap + Sort
- HashMap 的做法. sort每个string, 存进HashMap, 重复的就是anagrams,最后输出。   
- toCharArray
- Arrays.sort
- Stirng.valueOf(char[])
- 时间n*L*O(logL),L是最长string的长度。

#### Previous Notes
- Arrays.toString(arr)的做法。arr是int[26], assuming only have 26 lowercase letters.    
- Count occurrance, 然后convert to String，作为map的key.
- Time complexity: nO(L)
- 另一种做法：http://www.jiuzhang.com/solutions/anagrams/   
- 1. take each string, count the occurrance of the 26 letters. save in int[]count.   
- 2. hash the int[] count and output a unique hash value; hash = hash * a + num; a = a * b.   
- 3. save to hashmap in the same way as we do. 
- 这一步把for s: strs 里面的时间复杂度降到了O(L). L = s.length().   
- Need to work on the getHash() function.
- 时间变成n*O(L). Better.




---

**184. [Path Sum IV.java](https://github.com/awangdev/LintCode/blob/master/Java/Path%20Sum%20IV.java)**      Level: Medium      Tags: [DFS, Hash Table, Tree]
      

给一串3-digit 的数组. 每个数字的表达一个TreeNode, 3 digit分别代表: depth.position.value

这串数字已经从小到大排列. 求: 所有可能的 root->leaf path 的所有可能的 path sum 总和. 

#### DFS, Hash Table
- 因为`前两个digit可以uniquely identify`一个node, 所以可以把前两个digit作为key, 定位node.
- 特点: 比如考虑root, 有 n 个leaf, 就会加 n 遍root, 因为有 n 个 unique path嘛.
- 实现: 每个node, 上来先把curr value加进sum; 只要有child, 到这个node位置的以上path sum 就要被重加一次.
- format: depth.position.value. (on same level, position may not be continuous)
- approach: map each number into: <depth.position, value>, and dfs. 
- Start from dfs(map, rootKey, sum):
- 1. add node value to sum
- 2. compute potential child.
- 3. check child existence, if exist, add sum to result (for both left/right child). Check existence using the map.
- 4. also, if child exist, dfs into next level
- Space, time O(n)



---

**185. [Number Of Corner Rectangles.java](https://github.com/awangdev/LintCode/blob/master/Java/Number%20Of%20Corner%20Rectangles.java)**      Level: Medium      Tags: [DP, Math]
      

具体看题目: count # of valid rectangles (four corner are 1) in a grid[][].

#### basic thinking + Math
- Fix two rows and count matching columns
- Calculate number rectangles with `combination` concept:
- total number of combinations of pick 2 points randomly: count * (count - 1) / 2

#### DP
- TODO. HOW?

#### Brutle
- O(m^2 * n^2), times out



---

**186. [Palindromic Substrings.java](https://github.com/awangdev/LintCode/blob/master/Java/Palindromic%20Substrings.java)**      Level: Medium      Tags: [DP, String]
      

根据题意, count # of palindromic substring. (不同index截取出来的substring算不同的情况)

#### isPalin[][]
- build boolean[][] to check isPalin[i][j] with DP concept
- check all candidates isPalin[][]
- O(n^2)

#### odd/even split check
https://leetcode.com/problems/palindromic-substrings/discuss/105689/Java-solution-8-lines-extendPalindrome



---

**187. [Multiply Strings.java](https://github.com/awangdev/LintCode/blob/master/Java/Multiply%20Strings.java)**      Level: Medium      Tags: [Math, String]
      

给两个integer String, 求乘积

#### String calculation, basic implementation
- let num1 = multipier, num2 = base. 
- mutiply and save into int[m + n], without carry. Loop over num1, each row num1[x] * num2
- move carry to the correct index and direclty save result
- calculate carry on rst[]: sb.insert(0, c) such that no need to reverse() later
- remove leading '0', but do not delete string "0"
- time,space O(mn)

#### Previous notes. 
- Bad solution: reversing makes it complicated, no need to reverse.
- 1. 数字‘123’， 在数组里面， index == 0 是 ‘1’。 但是我们平时习惯从最小位数开始乘积，就是末尾的'3'开始。
- 所以！翻转两个数字先！我去。这个是个大坑。
- 2. 乘积product，和移动Carrier都很普通。
- 3. ！！最后不能忘了再翻转。
- 4. 最后一个看坑。要是乘积是0，就返回‘0’。 但是这个其实可以在开头catch到没必要做到结尾catch。
- 用到几个StringBuffer的好东西: reverse(), sb.deleteCharAt(i)   
- 找数字，或者26个字母，都可以: s.charAt(i) - '0'; s.charAt(i) - 'a';



---

**188. [Subsets.java](https://github.com/awangdev/LintCode/blob/master/Java/Subsets.java)**      Level: Medium      Tags: [Array, BFS, Backtracking, Bit Manipulation, DFS]
      
time: O(2^n)
space: O(2^n)

给一串unique integers, 找到所有可能的subset. result里面不能有重复.

#### DFS
- dfs的两种路子: 1. pick&&skip dfs, 2. for loop dfs
- 1. pick&&skip dfs: 取或者不取 + backtracking. 当level/index到底，return 一个list. Bottom-up, reach底部, 才生产第一个solution.
- 2. for loop dfs: for loop + backtracking. 记得：做subset的时候, 每个dfs recursive call是一种独特可能，先加进rst.  top-bottom: 有一个solution, 就先加上.
- Time&&space: subset means independent choice of either pick&&not pick. You pick n times: `O(2^n)`, 3ms

#### Bit Manipulation
- n = nums.length, 那么在每一个index, 都是 pick / not pick: 0/1
- 考虑subset index 0/1的bit map: range 的就是 [0000...00 ~ 2^n-1]
- 每一个bitmap就能展现出一个subset的内容: all the 1 represents picked indexes
- 做法:
- 1. 找出Range
- 2. 遍历每一个bitmap candidate
- 3. 对每一个integer 的 bit representation 遍历, 如果是1, add to list
- time: O(2^n * 2^n) = O(4^n), still 3ms, fast.

#### Iterative, BFS
- Regular BFS, 注意考虑如果让one level to generate next level
- 1. 用queue来存每一次的candidate indexes
- 2. 每一次打开一层candiates, add them all to result
- 3. 并且用每一轮的candidates, populate next level, back into queue.
- should be same O(2^n), but actual run time 7ms, slower





---

**189. [Subsets II.java](https://github.com/awangdev/LintCode/blob/master/Java/Subsets%20II.java)**      Level: Medium      Tags: [Array, BFS, Backtracking, DFS]
      
time: O(2^n)
sapce: O(2^n)

给一串integers(may have duplicates), 找到所有可能的subset. result里面不能有重复.

#### DFS
- DFS, 找准需要pass along的几个数据结构. 先`sort input`, 然后DFS
- Using for loop approach: 每个dfs call是一种可能性，直接add into result.     
- 为了除去duplicated result, skip used item at current level: `if (i > depth && nums[i] == nums[i - 1]) continue;`
- sort O(nlogn), subset: O(2^n)
- space O(2^n), save results

#### BFS
- Regular BFS, 注意考虑如果让one level to generate next level
- skip duplicate: `if (i > endIndex && nums[i] == nums[i - 1]) continue;`
- 1. 用queue来存每一次的candidate indexes
- 2. 每一次打开一层candiates, add them all to result
- 3. 并且用每一轮的candidates, populate next level, back into queue.
- srot O(nlogn), subset: O(2^n)
- should be same O(2^n). slower than dfs

#### Previous notes:
- 在DFS种skip duplicate candidates, 基于sorted array的技巧：    
- 一旦for loop里面的i!=index，并且nums[i] == nums[i-1],
- 说明x=nums[i-1]已经在curr level 用过，不需要再用一次: [a,x1,x2]，x1==x2    
- i == index -> [a,x1]    
- i == index + 1 -> [a,x2]. 我们要skip这一种
- 如果需要[a,x1,x2]怎么办？ 其实这一种在index变化时，会在不同的两个dfs call 里面涉及到。

#### 注意
- 不能去用result.contains(), 这本身非常costly O(nlogn)
- 几遍是用 list.toString() 其实也是O(n) iteration, 其实也是增加了check的时间, 不建议




---

**190. [Combination Sum.java](https://github.com/awangdev/LintCode/blob/master/Java/Combination%20Sum.java)**      Level: Medium      Tags: [Array, Backtracking, Combination, DFS]
      
time: O(n!)
space: O(n!)

给一串数字candidates (no duplicates), 和一个target. 

找到所有unique的 组合(combination) int[], 要求每个combination的和 = target.

注意: 同一个candidate integer, 可以用任意多次.


#### DFS, Backtracking
- 考虑input: 没有duplicate, 不需要sort
- 考虑重复使用的规则: 可以重复使用, 那么for loop里面dfs的时候, 使用curr index i
- the result is trivial, save success list into result.

##### Time complexity for Combination (reuse-candidate)
- at each level dfs, we have the index as starting point: 
- if we are at `index=0, we can have n child dfs() options via for loop`; 
- if at `index=1, we will have (n-1) dfs options via for loop`. 
- Consider it as the `pick/not-pick` problem, where the difference is you can pick `x` times at each index rather than only 2 times. 
- Overall, we will multiply the # of possibilities: n * (n - 1) * (n - 2) ... * 1 = n! => `O(n!)`

##### Combination DFS 思想
- 在每个index上面都要面临: `pick/not pick的选择`, 用for loop over index + backtracking 实现 picks.
- 每次pick以后, 就生成一条新的routine, from this index
- 下一个level的dfs从这个index开始, 对后面(或者当下/if allow index reuse) 进行同样的 pick/not pick 的选择
- 注意1: 每个level dfs 里面, for loop 里会有 end condition: 就不必要dfs下去了.
- 注意2: Backtracking在success case && dfs case 后都要做, 因为backtrack 是为了之前上一层dfs.




---

**191. [Combination Sum II.java](https://github.com/awangdev/LintCode/blob/master/Java/Combination%20Sum%20II.java)**      Level: Medium      Tags: [Array, Backtracking, Combination, DFS]
      

给一串数字candidates (can have duplicates), 和一个target. 

找到所有unique的 组合(combination) int[], 要求每个combination的和 = target.

注意: 同一个candidate integer, 只可以用一次.

#### DFS, Backtracking
- when the input has duplicates, and want to skip redundant items? 
- 1. sort. 2. in for loop, skip same neighbor.
- 考虑input: 有duplicate, 必须sort
- 考虑重复使用的规则: 不可以重复使用
- 1. for loop里面dfs的时候, 使用curr index + 1
- 2. for loop里面, 同一个level, 同一个数字, 不能重复使用: `(i > index && candidates[i] == candidates[i - 1]) continue`
- 因为在同一个level里面重复的数字在下一个dfs level里面是会被考虑到的, 这里必须skip (这个就记住吧)
- the result is trivial, save success list into result.

##### Time complexity
- Which one?
- Time: every level has 1 less element to choose, worst case is: cannot find any solution over all combinations: O(m!)
- Time: Same as `subsetII`, pick/not=pick an item as we go, no reuse of item. Worst case: all unique items in the set. O(2^n)




---

**192. [Combination Sum III.java](https://github.com/awangdev/LintCode/blob/master/Java/Combination%20Sum%20III.java)**      Level: Medium      Tags: [Array, Backtracking, Combination, DFS]
      

给一个integer k, 和一个target n. 

从positive数字[1 ~ 9], 找到所有unique的 组合(combination) int[], size = k, 要求每个combination的和 = n.

(隐藏条件, 需要clarify): 同一个candidate integer [1 ~ 9], 只可以用一次.

#### DFS, Backtracking
- 跟Combination Sum I, II 没什么太大区别, 只不过, 一定要用k个数字, 也就是一个for loop里面的特别条件
- 考虑input: 没有重复数字 [1 ~ 9]
- 考虑candidate重复利用: 不可以重复利用, next level dfs 时候, curr index + 1
- the result is trivial, save success list into result.

##### Time Complexity
- Which one?
- worst case: tried all numbers and cannot find: O(m!), m = 9, all possible integers in [1~9]
- C(n,k), n choose k problem : `n! / (k! * (n-k)!)` => ends up being `O(min(n^k, n^(n-k)))`



---

**193. [Product of Array Except Self.java](https://github.com/awangdev/LintCode/blob/master/Java/Product%20of%20Array%20Except%20Self.java)**      Level: Medium      Tags: [Array, PreProduct]
      
time: O(n)
space: O(1)

给一串数字, output rst[n], 每个index是 除了nums[i]以外 所有itemd的乘积.

#### Array, PreProduct
- 分析普通做法, 了结到用从左到右一遍O(n), 从右到左一遍 O(n) 就可以
- 注意carry的维护
- 看第二个解答, 进一步简化了代码
- PreProduct, 跟preSum的感觉有点像, 就是差一位.



---

**194. [Total Hamming Distance.java](https://github.com/awangdev/LintCode/blob/master/Java/Total%20Hamming%20Distance.java)**      Level: Medium      Tags: [Bit Manipulation]
      
time: O(n)
space: O(1), 32-bit array

给出Hamming Distance定义(bit format时候有多少binary diff), 求一串数字的hamming distance总和.

#### Bit Manipulation
- Bit题: 考验 bit >>, mask & 1, 还有对题目的理解能力
- Put integers in binary, and compare each column:
- for each `1`, ask: how many are different from me? all the `0`
- `# of diffs at each bit-column = #ofZero * #ofOne `
- 1. countZero[], countOne[]; 2. loop over nums and populate the two array

##### 注意雷点
- 问清楚: 10^9 < 2^31, we are okay with 32 bits
- `最终的hamming distance 要从 [1 ~ 32] 哪个bit开始算起`? 取决于 `最长`的那个binary format: 但不用先去找bit length
- 在做countZero, countOne时候, 都做32-bit; 最终做乘积的时候, 如果 `1` 或者 `0` 个数为零, 乘积自然为0.




---

**195. [Smallest Subtree with all the Deepest Nodes.java](https://github.com/awangdev/LintCode/blob/master/Java/Smallest%20Subtree%20with%20all%20the%20Deepest%20Nodes.java)**      Level: Medium      Tags: [DFS, Divide and Conquer, Tree]
      
time: O(n)
space: O(n)

给一个tree, 按照题意找最一个node满足: 
1. 这个node的subtree涵盖最深level的所有leaves. 
2. 这个node必须是能找到的最deep那个

条件2的需求是因为: root本身就是满足条件1的node, 还有很多Higher-level node也是如此, 所以要找那个deepest.


#### DFS on tree
- 分析题目, 思想是: 看到tree里面所有的leaves, 找到他们最deep的 common ancestor
- Maintain a map <Node, maxChildDepth>
- Recursively dfs: return deepest node that has all leaves by these comparisons:
- 1. If left,right child same depth, return root: they need common ancestor
- 2. If not same depth, return the one with larger depth
- 被传送去上一个level的, 永远都是subtree里面符合题意的: the node containing all leaf nodes
- Visit all nodes once O(n), space O(n)

#### BFS
- Find all leaves at deepest level
- Use map to track each node-parent
- Backtrack all nodes to find common ancestor



---

**196. [Subarray Sum Equals K.java](https://github.com/awangdev/LintCode/blob/master/Java/Subarray%20Sum%20Equals%20K.java)**      Level: Medium      Tags: [Array, Hash Table, PreSum, Subarray]
      
time: O(n)
space: O(n)

给一串数字, 找其中的 # of subarray的 where subararySum == k.

#### Hash Table + PreSum
- Hash Table two sum 思想, but `save frequency of current preSum`
- map.get(priorSum) = the # of possible ways to reach k
- Keep counting
- O(n) time, O(n) space

##### Detailed explanation
- From the orignal presum solution: `target = preSum[j] - preSum[i - 1]`. Here: `k = sum - priorSum`, and reversely, `priorSum = sum - k`
- priorSum is just previously calcualted sum; track its frequency using `map<preSumValue, frequency>`
- map.get(priorSum): # ways to sum up to priorSum.
- Also, to get `priorSum + k = sum`: each unique way of building priorSum will append later elements to reach sum (the later elemnts will sum up to k)
- Therefore # ways to build `k = map.get(priorSum)`


#### PreSum, O(n^2)
- move from starting point i = [0 ~ n -1] and define range = [i ~ j]
- use presum to verify k: `preSum[j] - preSum[i - 1]`
- O(n^2): `1 + 2 + 3 + 4 ... + n ~= O(n^2)`




---

**197. [Simplify Path.java](https://github.com/awangdev/LintCode/blob/master/Java/Simplify%20Path.java)**      Level: Medium      Tags: [Stack, String]
      
time: O(n)
space: O(n)

给一个path, simplify成最简单形式. 注意考虑edge case

#### Stack
- 理解unix path 的情况, 不懂得要问: 
- 1. `.` 代表current directory, 可以忽略. 
- 2. `../` 表示previous level. 
- 3. double slash 可以忽略.
- 4. empty string 要output `/`
- 最终就是用stack (`上一个加进去的item, 用来备选pop() out`), 遇到 `../` pop()掉上一个加上去的item, 其余加进stack
- 最终用 '/' 把所有item连接起来.



---

**198. [Convert Binary Search Tree to Sorted Doubly Linked List (extra space).java](https://github.com/awangdev/LintCode/blob/master/Java/Convert%20Binary%20Search%20Tree%20to%20Sorted%20Doubly%20Linked%20List%20(extra%20space).java)**      Level: Medium      Tags: [Linked List, Stack, Tree]
      
time: O(n)
space: O(n)

给一个BST, convert成 sorted doubly DoublyListNode.

#### Inorder Traversal, Linked List
- 会iterative traverse Binary Search Tree（Stack && handle left-dig-down）
- create Doubly-ListNode, 注意用一个dNode作为tail node of the list

##### Iterative inorder traversal
- 在check right node的事后，    
- 不论right == null or != null, 每次都要强行move to right.    
- 如果不node = node.right,     
- 很可能发生窘境：       
- node always  = stack.top(), 然后stack.top()一直是一开始把left 全部遍历的内容。所以就会infinite loop, 永远在左边上下上下。      



---

**199. [Binary Tree Zigzag Level Order Traversal.java](https://github.com/awangdev/LintCode/blob/master/Java/Binary%20Tree%20Zigzag%20Level%20Order%20Traversal.java)**      Level: Medium      Tags: [BFS, Stack, Tree]
      
time: O(n)
space: O(n)
    
#### Queue
- 简单的level traversal.根据level奇数偶数而add到不同位子.
- Option1: based on level % 2, insert to front/end of list
- Option2: based on level, insert right/left of node into queue



---

**200. [Word Break.java](https://github.com/awangdev/LintCode/blob/master/Java/Word%20Break.java)**      Level: Medium      Tags: [DP, Hash Table, Sequence DP]
      
time: O(n^2)
space: O(n)

给一个String word, 和一个字典, 检查是否word可以被劈开, 而所有substring都应该是dictionary里面的words.

#### Sequence DP
- true/false problem, think about dp
- 子问题: 前i个字母, 是否可以有valid break
- 检查dp[j] && `if substring(j, i) valid`, for all j = [0 ~ i]
- dp = new boolean[n + 1]; dp[0] = true;
- goal: if there is a j,  `dp[j] == true && word[j, n] in dict`. Need iterate over i = [0 ~ n], also j = [0, i]
- 注意, 用set代替list, 因为要用 contains().

#### Previous notes
##### 方法2(attempt4 code)    
- 与Word BreakII用同样的DP。
- valid[i]: 记录从i到valid array末尾是否valid.

##### 方法1:（attempt3 code）
- state,rst[i]: 从[0～i] inclusive的string是否可以在dict中break开来找到？      
- function: rst[i] = true if (rst[i - j] && set.contains(s.substring(i - j, i))); j in[0~i]     
- 1. rst[i - j] 记录的是[0, i-j]这一段是否可以break后在dict找到。     
- 2. 若true，再加上剩下所有[i-j, i]都能在dict找到，那么rst[i] = rst[0, i - j] && rst[i-j, i] == true
- 优化：找dict里面最长string, 限制j的增大。




---

**201. [Longest Increasing Subsequence.java](https://github.com/awangdev/LintCode/blob/master/Java/Longest%20Increasing%20Subsequence.java)**      Level: Medium      Tags: [Binary Search, Coordinate DP, DP, Memoization]
      
time: O(n^2) dp, O(nLogN) binary search
space: O(n)

无序数组, 找最长的上升(不需要连续)数组 的长度. 先做O(n^2), 然后可否O(nLogN)?

#### DP, double for loop, O(n^2)
- 找subsequence: 不需要continous, 可以skip candidate
- 考虑nums[i]结尾的时候, 在[0, i), dp[i - 1] 里count有多少小于nums[i]
- dp[i]: 到i为止 (对于所有 j in [0, i], 记录max length of increasing subsequence
- max需要在全局维护: nums是无序的, nums[i]也可能是一个很小的值, 所以末尾dp[i]并不是全局的max, 而只是对于nums[i]的max.
- 正因此, 每个nums[i]都要和每个nums[j] 作比较, j < i.
- dp[i] = Maht.max(dp[i], dp[j] + 1); j = [0 , i - 1]
- 时间复杂度  O(n^2)

#### O(nLogN)
- 维持一个list of increasing sequence
- 这个list其实是一个base-line, 记录着最低的increasing sequence.
- 当我们go through all nums的时候, 如果刚好都是上升, 直接append
- 如果不上升, 应该去list里面, 找到最小的那个刚好大于new num的数字, 把它换成num
- 这样就完成了baseline. 举个例子, 比如替换的刚好是在list最后一个element, 等于就是把peak下降了, 那么后面其他的数字就可能继续上升.
- '维护baseline就是一个递增的数列' 的证明, 还没有仔细想.



---

**202. [Best Time to Buy and Sell Stock with Transaction Fee.java](https://github.com/awangdev/LintCode/blob/master/Java/Best%20Time%20to%20Buy%20and%20Sell%20Stock%20with%20Transaction%20Fee.java)**      Level: Medium      Tags: [Array, DP, Greedy, Sequence DP, Status DP]
      
time: O(n)
space: O(n), O(1) rolling array

跟Stock II 一样, 买卖无限, 需先买在卖. 附加条件: 每个sell transaction要加一笔fee.

#### Sequence DP
- 与StockII一样, dp[i]: represents 前i天的最大profit.
- sell 的时候, 才完成了一次transaction, 需要扣fee; 而买入不扣fee.
- model sell on dp[i] day (which depends on dp[i-1]) and each day can be sell/buy => add status to dp[i][status]
- status[0] buy on this day, status[1] sell on this day
- dp[i][0] = Math.max(dp[i-1][0], dp[i - 1][0] - prices[i]);
- dp[i][1] = Math.max(dp[i-1][1], dp[i - 1][1] + prices[i] - fee);
- init: dp[0][0,1] = 0; dp[1][1] = 0; dp[1][0] = - prices;
- return dp[n][1]



---

**203. [Random Pick Index.java](https://github.com/awangdev/LintCode/blob/master/Java/Random%20Pick%20Index.java)**      Level: Medium      Tags: [Reservior Sampling]
      
time: O(n)
space: O(n) for input int[], O(1) extra space used

#### Reservior sampling
- Random choose: think about reservoir sampling. https://www.youtube.com/watch?v=A1iwzSew5QY
- Use random generator rd.nextInt(x) pick integer between [0, x)
- try all numbers, when target is met, we want to model reservoir sampling:
- item was chosen out of i samples, and all other samples are failed.
- where we can use 'count' to represent the denominator/base to choose.
- **HAVE TO finish all samples** to make sure equal opportunity
- we can pick that last matched item as result
- `rd.nextInt(count++) == 0` make sure we are always picking num == 0 to meet definition of reservoir sampling.

#### Knowledge
- If multiply these probablities together to get the probability of one item being chosen with reservior sampling:
- probability = 1/i * (1 - 1/i+1) * (1 - 1/i+2) ....(1 - 1/n) = 1/n




---

**204. [Find the Celebrity.java](https://github.com/awangdev/LintCode/blob/master/Java/Find%20the%20Celebrity.java)**      Level: Medium      Tags: [Array, Greedy]
      
time: O(n)
space: O(1)

有n个人, 其中有个人是celebrity, 满足条件 `Celeb knows nobody; Everyone else knows the celeb`. 找到celeb

#### Understand the property
- If brutly find celeb by comparing all possible pair: take complete O(n^2) handshakes.
- Instead, we can perform pruning, or like survival mode:
- 1. Assume a celeb = 0, and compare with all i = [1~ n-1]
- 2. If `celeb candidate know i, set celeb = i` as the next candidate (ex: prev canddiate invalid when he knows i)
- 3. For last standing celeb candidate: compare with all for validation
- Why performing the last run of validation? There could be someone dropped out before we execute `know(celeb, i)`. 

##### 思考逻辑
- 先写出来[0 ~ n - 1], 最简单的方式 O(n^2) 检查, 记录每个人的状态.
- 逐渐发现, 因为 celeb 谁都不会认识, 那么当任何candidate knows anyone, 他自身就不是celeb.
- 我们可以greedy地, 一旦fail一个, 就立刻假设下一个是celeb candidate
- 最终还是要检查一遍, 避免错漏.
- 想一下happy case: 如果 celeb=0,  那么 know(celeb, i) 永远都是false, 然后 celeb一直保持0, 坚持到verify所有人.



---

**205. [Sparse Matrix Multiplication.java](https://github.com/awangdev/LintCode/blob/master/Java/Sparse%20Matrix%20Multiplication.java)**      Level: Medium      Tags: [Hash Table]
      
time: O(mnk), where `m = A.row`, `n = B.col`, `k = A.col = B.row`
space: O(1) extra

给两个matrics, 做乘积. 注意, 是sparse matrix (特点: 很多0).

#### Hash Table
- Recall matric multiplication rules: result[i][j] = sum(A-row[i] * B-col[j])
- `sparse matric: lots positions are zero`
- 平白地写matric multiplication 没有意义, 重点就是optimization:
- `optimization`: for A-zero-row, and B-zero-col, there is no need to calculate, just return 0.
- 1. Find A-zero-rows and store in setA, same for setB
- 2. during multiplication, reduce time complexity.
- Base: O(mnk), where `m = A.row`, `n = B.col`, `k = A.col = B.row`

#### Matrices
- 乘法规则: result[i][j] = sum(A-row[i] * B-col[j])
- A column size == B row size. 并且: 计算顺序是iterate over A column size



---

**206. [Brick Wall.java](https://github.com/awangdev/LintCode/blob/master/Java/Brick%20Wall.java)**      Level: Medium      Tags: [Hash Table]
      
time: O(mn)
space: O(X), X = max wall width

给一面墙, 每一行是一行bricks. 用一条vertical line 扫描, 会vertically割开brink. 找到割开最少brick的那条线的x index.

#### Hash Table
- Find the vertical line (x-coordinate of the grid), where most gaps are found.
- Each gap has (x,y) coordinate
- Create `map<x-coordinate, #occurrance>`, and maintain a max occurance. 
- 计算: x-coordinate: `x = 0; x += brick[i] width`
- Eventually: min-crossed bricks = wall.lenght - maxOccurrance 

##### 思想
- 分析题意, 找到题目的目标
- 虽然Map自己不能有sort的规律, 但是可以maintain global variable



---

**207. [Exclusive Time of Functions.java](https://github.com/awangdev/LintCode/blob/master/Java/Exclusive%20Time%20of%20Functions.java)**      Level: Medium      Tags: [Stack]
      

#### Stack
- 1. later function always appears after prior fn: 1 is called by 0
- 2. `Not mentione in the question`: a function can be started multiple times
- 3. `Not mentione in the question`: a fn cannot start if children fn starts
- 4. Use stack to keep id
- TODO: what leads to the choice of stack? stacking fn id



---

**208. [Friends Of Appropriate Ages.java](https://github.com/awangdev/LintCode/blob/master/Java/Friends%20Of%20Appropriate%20Ages.java)**      Level: Medium      Tags: [Array, Math]
      

#### Array, Math
- 这个问题更在于问题本身的分析 (而且还有多余条件); 最终的for loop 也比较不standard.
- People younger than 15 cannot make requests due to the first rule.
- From the age of 15, people can make requests to the same age: a[i] * (a[i] - 1) requests.
- People can make requests to younger people older than 0.5 * i + 7: a[j] * a[i] requests.
- The third rule is redundant as the condition is already covered by the second rule.
- TODO: the approach.



---

**209. [Target Sum.java](https://github.com/awangdev/LintCode/blob/master/Java/Target%20Sum.java)**      Level: Medium      Tags: [DFS, DP]
      

// 如何想到从中间initialize



---

**210. [Maximum Size Subarray Sum Equals k.java](https://github.com/awangdev/LintCode/blob/master/Java/Maximum%20Size%20Subarray%20Sum%20Equals%20k.java)**      Level: Medium      Tags: [Hash Table, PreSum, Subarray]
      
time: O(n)
space: O(n)

#### Map<preSumValue, index>
- use `Map<preSum value, index>` to store inline preSum and its index.
- 1. Build presum incline
- 2. Use map to cache current preSum value and its index: `Map<preSum value, index>`
- 3. Each iteration: calculate possible preSum candidate that prior target sequence. ex: `(preSum - k)`
- 4. Use the calculated preSum candidate to find index
- 5. Use found index to calculate for result. ex: calculate range.



---

**211. [Contiguous Array.java](https://github.com/awangdev/LintCode/blob/master/Java/Contiguous%20Array.java)**      Level: Medium      Tags: [Hash Table]
      

TODO: how aout without chaning the input nums?



---

**212. [Line Reflection.java](https://github.com/awangdev/LintCode/blob/master/Java/Line%20Reflection.java)**      Level: Medium      Tags: [Hash Table, Math]
      
time: O(n)
space: O(n)

给一串点, 找是否有一个所有点中间的, 跟y-axis平行的中线.

#### Hash Table
- 1. store in `Map<y, set<x>>`, 2. iterate over map, check head,tail against the mid point
- 很好的细节题目:
- 1. 除以2, 需要存double
- 2. (问面试官)可以有重复的点! 所以track `set<x>`
- 3. 处理 left==right时候, 就当做两个点来处理.
- 4. 存进set里面没有sort, 但是最后做check的时候, 需要sort list
- 时间: visit all nodes 两遍,  O(n)



---

**213. [Insert Delete GetRandom O(1).java](https://github.com/awangdev/LintCode/blob/master/Java/Insert%20Delete%20GetRandom%20O(1).java)**      Level: Medium      Tags: [Array, Design, Hash Table]
      
time: O(1) avg
space: O(n)

#### Hash Table
- 用`map<value, index> 来track value->index`, 用`list track index->value`
- map查看value是否存在
- list maintain 用来 insert/remove/random operations.
- 特点: 一旦remove, 换到list结尾然后 `list.remove(list.size() - 1)`, 这样remove的cost更低. 
- list.remove(object) 应该是要O(logn) 做一个search的.



---

**214. [Number of Longest Increasing Subsequence.java](https://github.com/awangdev/LintCode/blob/master/Java/Number%20of%20Longest%20Increasing%20Subsequence.java)**      Level: Medium      Tags: [Coordinate DP, DP]
      
time: O(n^2)
time: O(n)

给一串 unsorted sequence, 找到长 increasing subsequence 的个数!

#### Coordinate DP
- 需要能够判断综合题, 分清楚情况和套路: combination of `longest subsequence` and `ways to do`, as well as global variable. 
- len[i] (我们平时的dp[i]): 在前i个元素中, 最长的 increasing subsequence length;
- count[i]: 在前i个元素中, 并且以 len[i]这个长度为准的 subsequence的 count. 或者: 在前i个元素中, ways to reach longest increasing subsequence.
- `len[i] == len[j] + 1`: same length, but different sequence, so add all `count[i] += count[j]`
- `len[i] < len[j] + 1`: 这就是更长的情况找到了, 那么有多少次 count[j] 有多少, count[i] 就有多少. 仔细想sequence: 长度增长了, 但是ways to reach i 没有增长.
- 同样的判断需要用在 maxLen 和 maxFreq上:
- 如果没有增长 maxLen 不变, maxFreq上面需要 +=count[i] (同一种长度, 多了更多的做法)
- 如果maxLen 变长, maxFreq 也就是采用了 count[i] = count[j]
- TODO: Is rolling array possible?

#### 相关
- 都是 Coordiate DP, DP的鼻祖家族:
- Longest Increasing Subsequence (跟这道题的一部分一模一样)
- Longest Continuous Increasing Subsequence (连续, 只check dp[i - 1])
- Longest Increasing Continuous Subsequence I, II (Lintcode, II 是matrix)



---

**215. [Minimum Swaps To Make Sequences Increasing.java](https://github.com/awangdev/LintCode/blob/master/Java/Minimum%20Swaps%20To%20Make%20Sequences%20Increasing.java)**      Level: Medium      Tags: [Coordinate DP, DP, Status DP]
      


#### DP
- 特点: 上一步可能是swaped也可能是fixed
- 考虑A,B之间的现状: `A[i] > A[i - 1] && B[i] > B[i - 1]` 或者 `A[i] > B[i - 1] && B[i] > A[i - 1]`
- 问题: 如何把这个状态变成合理的strick-increasing状态?
- `A[i] > A[i - 1] && B[i] > B[i - 1]`: 1. 已经合理, 也不动.  2. [i], [i-1] 全部都swap
- `A[i] > B[i - 1] && B[i] > A[i - 1]`, 交错开来, 所以调换[i], 或者[i-1]: 1. 换[i-1]. 2. 换[i]
- 注意因为求min, 所以init value应该是 Integer.MAX_VALUE;



---

**216. [Binary Tree Vertical Order Traversal.java](https://github.com/awangdev/LintCode/blob/master/Java/Binary%20Tree%20Vertical%20Order%20Traversal.java)**      Level: Medium      Tags: [BFS, DFS, Hash Table, Tree]
      
time: O(n)
space: O(n)

给一个Binary Tree, traverse所有node, 按照vertial order 排列成output: List<List> 

重点是: col里面有排序, 在higher level的排在前面; 如果node遇到collision在同一个位置: 根据他们的相对位置 先放left, 再放right

#### BFS
- 应该比较好想: naturally level-traverse all nodes, add node to appropriate col list
- Use min/max to track map keys, since the keys are continous
- Map does not provide random access; unless map key is marked with sequence i = [min, max]

#### DFS
- 一开始很容易想到: enumerate一下, 先放curr node.val, 然后node.left.val, node.right.val. 非常简单
- 但是最简单的方法有错: assume所有left subtree都 排在right subtree. 但是: right subtree可能先有一个lower-left-branch,  appear in a column first.
- 所以还要preserve column list的order.
- 这里我们用了 `Map<col, Node>` 来track col, Node 里面用了 `node.level`来track level (其实再一个map也可以)
- 这样在结尾要sort,就会非常慢: Visit all nodes O(n) + O(logK) + O(KlogM), K = # of cols, M = # of items in col
- 应该也是可以optimize map keys的, 反正都是continuous key





---

**217. [Populating Next Right Pointers in Each Node II.java](https://github.com/awangdev/LintCode/blob/master/Java/Populating%20Next%20Right%20Pointers%20in%20Each%20Node%20II.java)**      Level: Medium      Tags: [DFS, Tree]
      
time: O(n)
space: O(1)

给一个binary tree, 用constant space link 所有所有node.next to same level next node.

#### DFS
- 用constant space 也就是不可以BFS, 但是mention了用dfs stack space没问题 (提示啊!)
- 1. link leftChild -> rightChild
- 2. resolve root.rightMost child -> first possible root.next.left/right child
- 3. dfs connect(rightChild), connect(leftChild)
- Each level should be fully linked from left side, so every reach to parent will have valid path or end.

#### Trick
- 1. 处理 nextNode -> next -> next ...的case: 找到第一个有child的next node才可以罢休. 这个case很容易miss
- 2. 我们的假设是, 上一个level的所有node都应该是linked, 那么在dfs时候, 就应该先connect(root.right). 右孩子的全处理完毕, 那么trick1才可以施行.



---

**218. [Search in Rotated Sorted Array.java](https://github.com/awangdev/LintCode/blob/master/Java/Search%20in%20Rotated%20Sorted%20Array.java)**      Level: Medium      Tags: [Array, Binary Search]
      
time: log(n)
space: O(1)

#### Binary Search
- 关键点, 是找到 [mid]是在左边/还是右边的continous increasing subarray: 比较 `A[start] < A[mid]`
- 在两个section 里面分别讨论 target 的位置     
- 1. `nums[start] < nums[mid]`: start是从index=0开始的, 那就说明 `mid在前半段`
- `start<target<mid`: target 在这个section里面, end = mid;
- `target > mid`: start = mid;
- 2. `nums[start] > nums[mid]`: start是从index=0开始的, 那就说明 `mid在后半段`
- `mid < target < end`: start = mid;
- `target < mid`: end = mid;   

#### binary search break point, 然后继续binary search target
- 1. binay search break point     
- 2. binary search target      
- 注意等号，在判断target在前半段还是后半段：if (A[p1] <= target && target <= A[breakPoint])      





---

**219. [Find the Weak Connected Component in the Directed Graph.java](https://github.com/awangdev/LintCode/blob/master/Java/Find%20the%20Weak%20Connected%20Component%20in%20the%20Directed%20Graph.java)**      Level: Medium      Tags: [Union Find]
      

遍历 weak connected graph, 将结果存在 List<List<Node>>种.

#### Union Find
- 跟传统的UnionFind有两点不同:
- 1. 用 Map<Integer, Integer> 代替 int[], 因为没有给出 graph node label的 boundary.
- 2. find(x)时候, 没有去update `parent[x]/map.put(x, ..)`. 因为我们最终需要找到这个path.
- 无法用传统dfs: directed node 无法point到上一个点; 必须用`存parent的方式把所有node遍历掉`

#### Identify这是个union-find问题
- 看到了weak component的形式： 一个点指向所有，那么所有的点都有一个公共的parent，然后就是要找出这些点。    
- 为何不能从一个点出发，比如A，直接print它所有的neighbors呢:
- 如果轮到了B点，那因为是directed,它也不知道A的情况，也不知道改如何继续加，或者下手。    
- 所以，要把所有跟A有关系的点，或者接下去和A的neighbor有关系的点，都放进union-find里面，让这些点有Common parents.     
- 最后output的想法：    
- 做一个 map <parent ID, list>。    
- 之前我们不是给每个num都存好了parent了嘛。    
- 每个num都有个parent, 然后不同的parent就创造一个不同的list。   
- 最后，把Map里面所有的list拿出来就好了。    



---

**220. [Accounts Merge.java](https://github.com/awangdev/LintCode/blob/master/Java/Accounts%20Merge.java)**      Level: Medium      Tags: [DFS, Hash Table, Hash Table, Union Find]
      

给一串account in format `[[name, email1, email2, email3], [name2, email,..]]`. 

要求把所有account merge起来 (可能多个record记录了同一个人, by common email)


#### Union Find
- 构建 `Map<email, email parent>`, 然后再反向整合: parent -> list of email
- init with <email, email> for all emails
- 因为不同account可能串email, 那么把所有email union的时候, 不同account 的email也会被串起来
- 最终: 所有的email都被union起来, 指向一个各自union的 parent email
- UnionFind 的 parent map 可以反向输出所有  child under parent.
- 同时要维护一个 <email -> account name> 的map, 最终用来输出.

#### Hash Table solution, passed but very slow
- Definitely need iterate over accounts: merge them by email.
- Account object {name, list of email}
- map<email, account>
- 1. iterate over accounts
- 2. find if 'account' exist;  if does, add emails
- 3. if not, add account to list and to map. map all emails to accounts.
- output -> all accounts, and sort emails
- space O(mn): m row, n = emails
- time O(mn)



---

**221. [Count of Smaller Number.java](https://github.com/awangdev/LintCode/blob/master/Java/Count%20of%20Smaller%20Number.java)**      Level: Medium      Tags: [Binary Search, Lint, Segment Tree]
      

给一串数字, array size = n. 给一串query: 每个query是一个数, 目的找 count# items smaller than query element.

#### Segment Tree
- 和平时的segment tree问题不同。 [0 ～ n] 代表实际数字: based on real value的segment tree.
- Modify时，把array里面的value带进去，找到特定的位子, 然后count + 1. 
- 最终在SegmentTree leaf上面全是array里面实际的数字。
- node.count: 在node range里面的有多少个数字

##### right use of modify()
- build() 只是 empty segment tree, 没有property
- modify() 需要: 1. 找到left, update count+=1; 2. aggregate all parent when after returning
- 所以每一个modify 都是在整个path上所有的node上 + count

##### query trick
- 在query前，给进去的start和end是： 0 ~ value-1.   
- `value-1`: 找比自己所在range小1的range（那么自然而然地就不包括自己了），这样就找到了smaller number.   

##### About other basic segment tree setup
- [那么其他做过的SegmentTree是怎么样呢？]   
- 那些构成好的SegmentTree(找min,max,sum)也有一个Array。但是构成Tree时候，随Array的index而构架。   
- 也就是说，假如有Array[x,y,....]:在leaf,会有[0,0] with value = x. [1,1] with value = y. 
- [但是这题]   
- 构成时，是用actual value.也就是比如Array[x,y,....]会产生leaf:[x,x]with value = ..; [y,y]with value =...    
- 其实很容易看穿:   
- 若给出一个固定的array构成 SegmentTree，那估计很简单：按照index从0~array.lengh，leaf上就是[0,0] with value = x.
- 若题目让构造一个空心SegmentTree, `based on value 0 ~ n-1 (n <= 10000)`, 然后把一个Array的value modify 进去。   
- 这样八成是另外一种咯。



---

**222. [My Calendar I.java](https://github.com/awangdev/LintCode/blob/master/Java/My%20Calendar%20I.java)**      Level: Medium      Tags: [Array, TreeMap]
      

Given a list of interval as calendar items. Check if newly added calendar item is overlapping.

Understand it is only checking time, but not requiring to insert into right spot. No need to overthink.

#### Simply O(n) check on array
- number of test cases is small, like 1000, so less concern about the time complexity
- simply loop over the list of intervals, and check if any overlapping.
- where to insert does not really matter: every time we are just checking for overlaopping, not merging any range
- **IMPORTANT**: if interval over lapping, they will have this property `Math.max(s1, s2) < Math.min(e1, e2)`. This will help detect the overlapping very easily.
- O(n^2) runtime, with simple code. But somehow this approach is faster than the TreeMap solution: maybe the test cause causes avg O(n)?

#### TreeMap
- One constraint from the simply array solution: it always cost O(n) to find the potential overlapping interval
- We can manually sort and always manually try to find the correct element via binary search, or we could store the interval in a treeMap<startKey, endValue>, where the intervals are sorted by `start`.
- As result, all we need to do for book(start, end) is to find the next element ceiling(start), last element floor(start), and check for overlapping
- This approach also saves the custom data structure
- Overall cost O(nlogn)

##### About TreeMap
- always with key sorted ascendingly 
- more costly than regular HashMap because of the sorting. Building treemap of n items: O(nlogn)

#### Sweep line
- use `Point{int start, end; boolean start}` to mark start/end of class. Add to pq.
- Adding new item to pq, sort, and check if overlapping occurs by counting started classes
- If started classes > 1, that means we overlapped.
- Every time it could consume all classes to find the overlap, O(n^2).
- Not quite need to sort or insert at correct point, and this solution requires longer code. Not quite worthy it for a simple problem.




---

**223. [Reverse Pairs.java](https://github.com/awangdev/LintCode/blob/master/Java/Reverse%20Pairs.java)**      Level: Medium      Tags: [Binary Indexed Tree, Binary Search Tree, Divide and Conquer, Merge Sort, Segment Tree]
      

给一串数字, count total reverse pair `nums[i] > 2*nums[j]`, i < j

This problem can be solved with Merge sort concept, BST, Segment Tree and Binary Indexed Tree. Good for learning/review.

#### Merge Sort
- Using merge sort concept, not exaclty merge sort implementation.
- One very simply concept: if we want to know how many elements between [i, j] are meeting requirements of `nums[i] > 2*nums[j]`, it would be really helpful, if the entire range is sorted:
- then we just need to keep one i index, and keep j++ for all elements meeting requirement `j<=e && nums[i]/2.0 > nums[j]`
- Then it comes to the sorting part: we cannot just directly sort entire array, because the restriction is `all elements on right side of curr element`. BUT, it is okay to sort `right side range` and compare with left side elements : )
- 灵感: use merge sort concept, divide and conquer:
- divide the elements from mid, compare each subarray
- sort once sub-array is completed (so that it can be used recursively at parent level)
- use classic while loop `while(j<=e && nums[i]/2.0 > nums[j])` to count pairs


#### Segment tree
- TODO
- split the array into index-based segment tree, where each element is at leaf
- store min of range: use max to determine if certain range is needed for further query
- query for each element right side range (i + 1, end), where it recursively query&aggregate sub-range if meeting requirement `nums[i] > 2*nums[j]`
- only when target > subRange.min * 2: there are possible candidates, query further
- worst case O(n^2) when all tailing elements are meeting requirement.

#### BST
- TODO
- Build the BST based on node value. It will be not applicable if we search after entire tree is built (our goal is right range), so we need to build right elements, and search/count right after the elements is added
- Worst case is still O(n^2), if all added nodes are meeting requirement 
- search(tree, curr / 2.0)



#### O(n^2)
- check each one of them




---

**224. [Kth Largest Element in an Array.java](https://github.com/awangdev/LintCode/blob/master/Java/Kth%20Largest%20Element%20in%20an%20Array.java)**      Level: Medium      Tags: [Divide and Conquer, Heap, MinHeap, PriorityQueue, Quick Sort]
      

kth largest in array

#### PriorityQueue, MinHeap
- Need to maintain k large elements, where the smallest will be compared and dropped if applicable: 
- Maintain k elements with min value: consider using minHeap
- add k base elements first
- Maintain MinHeap: only allow larger elements (which will squzze out the min value)
- Remove peek() of queue if over size
- O(nlogk)


#### Quick Sort
- 用Quick Sort 里面partion的一部分
- sort结束后是ascending的, 那么 n - k 就是第k大. 
- partion的结果是那个low, 去找 low==nums.size() - k， 也就是倒数第K个。    
- 没找到继续partion recursively.
- sort的过程是排一个从小到大的list. (同样的代码还可以好xth smallest，mid变成x就好)
- Steps:
- 每个iteration, 找一个pivot,然后从low,和high都和pivot作比较。    
- 找到一个low>pivot, high<pivot, 也就可以swap了。    
- 得到的low就是当下的partion point了
- Overall O(nlogN), average O(n) for this problem.



---

**225. [Merge k Sorted Lists.java](https://github.com/awangdev/LintCode/blob/master/Java/Merge%20k%20Sorted%20Lists.java)**      Level: Medium      Tags: [Divide and Conquer, Heap, Linked List, PriorityQueue]
      

给一个array of ListNode, 把所有node按照大小连成一条.

#### Priorityqueue
- Iterative, PQ来排列所有list的leading node.
- 记得k lists 需要是已经sort好的
- 时间：n*O(logk), where n = total node number, and PriorityQueue: logk, 
- Note:
- 1. 不要忘记customized priority需要一个customized new Comparator<T>()
- 2. Given list 里面也可能有null node, 不要忘记查.

#### Divide and Conquer
- always merge 2 list at a time
- 3 branches: 
- 1. start == end
- 2. start + 1 == end
- 3. or start + 1 < end (recursive and keep merging)
- T(k) = 2T(k/2) + O(mk), where m = longest list length
- time complexity: O(nklogk)
- TODO: write the recursive code.

#### Followup
- 如果k很大，一个机器上放不下所有的k list怎么办？ 
- 如果Merge起来的很长，一个机器上放不下怎么办？




---

**226. [Merge k Sorted Arrays.java](https://github.com/awangdev/LintCode/blob/master/Java/Merge%20k%20Sorted%20Arrays.java)**      Level: Medium      Tags: [Heap, MinHeap, PriorityQueue]
      

Same as merge k sorted list, use priorityQueue

#### Priority Queue
- 由Merge k sorted list启发。用PriorityQueue,存那k个首发element
- PriorityQueue需要存储单位: 自己建一个Class Node 存val, x, y index.    
- 因为array里没有 'next' pointer，只能存x,y来推next element
- Not sure why `new PriorityQueue<>(Comparator.comparing(a -> a.val));` is slower



---

**227. [Heapify.java](https://github.com/awangdev/LintCode/blob/master/Java/Heapify.java)**      Level: Medium      Tags: [Heap, MinHeap]
      

Turn unsorted array into a min-heap array, where for each A[i], 

A[i * 2 + 1] is the left child of A[i] and A[i * 2 + 2] is the right child of A[i].

#### Heap
- Heap用的不多. 得用一下, 才好理解. 通常default 的PriorityQueue就是给了一个现成的min-heap:
- 所有后面的对应element都比curr element 小。
- Heapify里面的**siftdown**的部分:
- 只能从for(i = n/2-1 ~ 0)， 而不能从for(i = 0 ~ n/2 -1): 必须中间开花，向上跑的时候才能确保脚下是符合heap规则的

#### Heapify/SiftDown做了什么?
- 确保在heap datastructure里面curr node下面的两个孩子，以及下面所有的node都遵循一个规律
- 比如在这里，若是min-heap,就是后面的两孩子都要比自己大。若不是，就要swap。    

#### min-heap的判断规律:
- for each element A[i], we will get A[i * 2 + 1] >= A[i] and A[i * 2 + 2] >= A[i].
- siftdown时：在curr node和两个child里面小的比较。如果的确curr < child, 搞定，break while.   
- 但若curr 并不比child小，那么就要换位子，而且继续从child的位子往下面盘查。    



---

**228. [Top K Frequent Elements.java](https://github.com/awangdev/LintCode/blob/master/Java/Top%20K%20Frequent%20Elements.java)**      Level: Medium      Tags: [Hash Table, Heap, MaxHeap, MinHeap, PriorityQueue]
      
time: O(n)
space: O(n)

给一串数字, 找到top k frequent element, 并且time complexity 要比nLogN要好

#### HashMap + bucket List[]
- Use HashMap to store <num, freq>
- Reverse mapping <count, list unique element with that count> in a `bucket = new List[n]`. 
- Size of the data structure will be m <= n
- The bucket[count] preserves order from end of the array.
- Simply loop over the reversed map, we can find the top k items.
- Solid O(n)

#### PriorityQueue, MinHeap
- Use regualr priorityQueue to sort by frequency ascendingly
- the queue.peek() record has lowest frequency, which is replacable
- Always only maintain k elements in the queue, so sorting is O(logk)
- IMPORTANT: remember to `rst.add(0, x)` for desired ordering
- time faster than maxHeap: O(nlogk)

#### PriorityQueue, MaxHeap
- 题目有提醒: 必须beetter than O(nLog(n)), 也就是说明要O(n)
- 首先想到就是PriorityQueue, 并且不能queue.offer on the fly
- 那么就先count, O(n), using HashMap
- 再priorityQueue, (mLog(m)), m是unique 数字的总量
- 最终find top k, O(k)
- Overall time: O(n) + O(mLogm) + O(k) => O(n), if m is small enough




---

**229. [Ugly Number II.java](https://github.com/awangdev/LintCode/blob/master/Java/Ugly%20Number%20II.java)**      Level: Medium      Tags: [DP, Enumeration, Heap, Math, PriorityQueue]
      
time: O(n)
space: O(n)

#### DP
- curr index is based on previous calculation: the min of all 3 previous factors
- O(n)

#### PriorityQueue, DP
- 非常brutle的。
- 每次把dp[i-1]拿出来，不管三七二十一，分别乘以2,3,5. 出来的结果放进priority queue做比较。
- 最后时间是n*log(n*3)
- 注意：use long, use HashSet确保没有重复
- O(nlogn)




---

**230. [Inorder Successor in BST.java](https://github.com/awangdev/LintCode/blob/master/Java/Inorder%20Successor%20in%20BST.java)**      Level: Medium      Tags: [BST, Tree]
      

找 Inorder traversal规则里的下一个.

主要想法是考虑: 
    1. 如果 node.right == null, 找上一个unprocessed node alone the inorder traversal path
    2. 如果 node.right != null, successor 一定在这个node.right那个subtree里面
最后竟然可以简化成几行, 非常全面的BST问题: 有search, 有对inorder traversal的理解, 还有坑.

#### Short Recursive and Iterative without Stack
- Previous solution, we use stack to hold previous cached/unprocessed items: but do we need use catch to hold them?
- If moving left: `p.val < root.val`, then root (parent of left child) is a successor candidate, so save `rst = root`.
- If moving right or equal: `p.val >= root.val`, the successor has nothing to do with curr node, so just directly dive into root.right.
- Both iterative and recursive solution can be simplified as such.


#### Previous Iterative + stack
- Iteratively search
- Still need stack to store previously unprocessed items along the path

#### Previous Recursive + Stack
- 画inorder图，发现规律.每个node的后继node(successor)有几种情况:   
- 1. node.right 是个leaf到底了。那么就return.   
- 2. set rightNode = node.right， 但发现rightNode has a lot left children to leaf.   
- 3. 比如, node.right == null， 也就是node自己是leaf，要回头看山顶找Inorder traversal规则里的下一个。   
- 发现：其实就是每层都把路过的curr node放在stack里，最上面的，就是当下改return的那个successor:) Done.



---

**231. [Walls and Gates.java](https://github.com/awangdev/LintCode/blob/master/Java/Walls%20and%20Gates.java)**      Level: Medium      Tags: [BFS, DFS]
      

给一个room 2D grid. 里面有墙-1, 门0, 还有empty space INF(Math.MAX_VALUE). 

对每个empty space而言, fill it with dist to nearest gate.

#### DFS
- Form empty room: it can reach different gate, but each shortest length will be determined by the 4 directions. 
- Option1(NOT applicable). DFS on INF, mark visited, summerize results of 4 directions. 
- hard to resue: we do not know the direction in cached result dist[i][j]
- Option2. DFS on gate, and each step taken to each direction will +1 on the spot: distance from one '0'; 
- Through dfs from all zeros, update each spot with shorter dist
- Worst time: O(mn), where entre rooms[][] are gates. It takes O(mn) to complete the iteration. Other gates be skipped by `if (rooms[x][y] <= dist) return;`

#### BFS
- Exact same concept. Init with `Queue<int[]> queue = new LinkedList<int[]>()`



---

**232. [Convert Binary Search Tree to Sorted Doubly Linked List.java](https://github.com/awangdev/LintCode/blob/master/Java/Convert%20Binary%20Search%20Tree%20to%20Sorted%20Doubly%20Linked%20List.java)**      Level: Medium      Tags: [BST, DFS, Divide and Conquer, Linked List, Tree]
      
time: O(n)
space: O(1)

题目描述起来有点复杂, 简而言之: 把 BST 转换成一个 sorted doubly linked list. (in-place)

#### Tree, In-order traversal
- 平时做过convert BST to sored list: 画一下就理解, 其实就是in-order traversal
- 只不过做的时候要小心地 doubly link them
- 理解之后就简单了, traverse all nodes,  DFS 好做: `left, curr, right`

##### 题目特殊特点
- 自始至终用了同一个 `Node {val, left, right}`, 而并不是开一个新的doubley linked list class
- extra space 的问题, 是因为它需要create new DoublyLinkedNode class: different from `Convert Binary Search Tree to Sorted Doubly Linked List (extra space)`
- 要求in-place: 不能重新create new node



---

**233. [String to Integer (atoi).java](https://github.com/awangdev/LintCode/blob/master/Java/String%20to%20Integer%20(atoi).java)**      Level: Medium      Tags: [Math, String]
      

#### String 
- check sign, leading-0, overall size > 11, check max/min in Long format 
- if passed all tests, parseInt()

#### regular expression
- if (!str.matches("[+-]?(?:\\d+(?:\\.\\d*)?|\\.\\d+)")).  猛了一点



---

**234. [Clone Graph.java](https://github.com/awangdev/LintCode/blob/master/Java/Clone%20Graph.java)**      Level: Medium      Tags: [BFS, DFS, Graph]
      

给一个graph node, 每个node有list of neighbors. 复制整个graph, return new head node.
       
实现起来就好像在crawl urls.

#### 思想
- Use HashMap to mark cloned nodes.    
- 先能复制多少Node复制多少. 然后把neighbor 加上
- Use `map<oldNode, newNode>` to mark visited

#### DFS
- Given graph node obj `{val, list of neighbor}`: copy the node and all neighbors
- Mark visited using map<oldNode, newNode>
- for loop on the each one of the neighbors: map copy, record in map, and further dfs
- once dfs completes, add newNeighbor as neighbor of the new node (get to it via map)
- 主要思想是: 一旦复制过了, 不必要重新复制

#### BFS
- Copy the root node, then copy all the neighbors. 
- Mark copied node in map.
- Use queue to contain the newly added neighbors. Need to work on them in the future.



---

**235. [Permutations.java](https://github.com/awangdev/LintCode/blob/master/Java/Permutations.java)**      Level: Medium      Tags: [Backtracking, DFS, Permutation]
      

#### Recursive: Backtracking
- Given a remaining list: 取, 或者不取
- always iterate over full `nums[]`, use list.contains() to check if item has been added.
- Improvement: maintain list (add/remove elements) instead of 'list.contains'
- time O(n!): visit all possible outcome
- T(n) = n * T(n-1) + O(1)

#### Iterative: Insertion
- 插入法:
- 1. 一个一个element加进去
- 2. 每一次把rst里面的每个list拿出来, 创建成新list, 然后选位置加上new element
- 3. 加新元素的时候, 要在list的每个位置insert, 最终也要在原始的list末尾加上new element
- 还是O(n!), 因为rst insert O(n!)个permutations
- 但是比dfs要快, 因该是因为 # of checks 少: 不需要check list.size(), 不需要maintain remaining list.

#### Previous Notes
- 用个queue，每次poll()出来的list, 把在nums里面能加的挨个加一遍
- Time O(n!)
- A bit slower, possibly because of the polling and saving the entire list every time




---

**236. [One Edit Distance.java](https://github.com/awangdev/LintCode/blob/master/Java/One%20Edit%20Distance.java)**      Level: Medium      Tags: [String]
      

如果S, T只用一个operation就能变成相等, return true.

#### Edit: 删除，增加，和替换
- 换完之后，理论上换成的String 就应该全等
- for loop, 一旦找到不一样的char, 就判断那三种可能性: insert/delete/replace
- insert/delete 对于2个string来说, 效果是类似的
- O(n)



---

**237. [4Sum.java](https://github.com/awangdev/LintCode/blob/master/Java/4Sum.java)**      Level: Medium      Tags: [Hash Table]
      

#### Based on 2sum
- 1. 利用2Sum的原理，把4Sum分为连个2Sum。左一个pair,右一个pair，每个pair里面放2个数字。   
- 2. 以一个点，i，作为分界口，也要列举出所有i之前的pair,作为基础。   
- 3. 再尝试从所有i+1后面,找合适的2nd pair。   
- Time: O(n^2 * x), where x = # of candidates, still slow
- 可以用HashSet<List>, 可以直接比较list里面每一个元素, 保证set不重复.
- Previous Notes: 在造class Pair时候，要做@override的function: hashCode(), equals(Object d). 平时不太想得起来用。
- 参见 http://lifexplorer.me/leetcode-3sum-4sum-and-k-sum/    

#### Based on 3Sum
- 3Sum外面再加一层. 参考3Sum. 时间O(n^3)。 但此方法在k-sum时候，无疑过于费时间. O(n^k)



---

**238. [Redundant Connection.java](https://github.com/awangdev/LintCode/blob/master/Java/Redundant%20Connection.java)**      Level: Medium      Tags: [BFS, DFS, Graph, Tree, Union Find]
      

#### unionFind
- keyword: tree has no `cycle`.
- 一旦两个node在edge中出现, 并且parent相同, 说明这两个node不union, 也在同一个tree里面, 所以可以break them.

#### Graph, DFS
- Add graph using adjacent list, and verify cycle alone the way
- IMPORTANT: use `pre` node in dfs to prevent backward dfs
- similar to `Graph Valid Tree` where it validates cycle and also needs to validate if all nodes are connected

#### BFS
- same concept as DFS, find first redundant edge that alreay exists in graph map.



---

**239. [Graph Valid Tree.java](https://github.com/awangdev/LintCode/blob/master/Java/Graph%20Valid%20Tree.java)**      Level: Medium      Tags: [BFS, DFS, Graph, Union Find]
      

给一个数字n代表n nodes, marked from 1 ~ n, 和一串undirected edge int[][]. 

检查这些edge是否能合成一个 valid tree

#### Union Find
- 复习Union-Find的另外一个种形式, track union size: tree does not have cycle, so eventually union size should == 1
- 1. 查找2个元素是不是在一个union里面。如果不在，false. 如果在，那就合并成一个set,共享parent.   
- 2. 验证cycle: `find(x) == find(y) => cycle`: new index has been visited before
- 存储的关键都是：元素相对的index上存着他的root parent.    
- 注意: 结尾要检查, 是否只剩下1个union: Tree必须连接到所有给出的node.
- 另一个union-find, 用hashmap的:
- http://www.lintcode.com/en/problem/find-the-weak-connected-component-in-the-directed-graph/

#### DFS
- Very similar to `Redundant Connection`
- Create adjacent list graph: Map<Integer, List<Integer>>
- 检查: 
- 1. 是否有cycle using dfs, check boolean[] visited
- 2. 是否所有的node全部链接起来: validate if all edge connected: # of visited node should match graph size
- IMPORTANT: use `pre` node to avoid linking backward/infinite loop such as (1)->(2), and (2)->(1)

#### BFS
- (还没做, 可以写一写)
- 也是检查: 1. 是否有cycle, 2. 是否所有的node全部链接起来



---

**240. [The Maze.java](https://github.com/awangdev/LintCode/blob/master/Java/The%20Maze.java)**      Level: Medium      Tags: [BFS, DFS]
      

#### BFS
- BFS on coordinates
- always attempt to move to end of border
- use boolean[][] visited to alingn with BFS solution in Maze II, III, where it uses Node[][] to store state on each item.



---

**241. [The Maze II.java](https://github.com/awangdev/LintCode/blob/master/Java/The%20Maze%20II.java)**      Level: Medium      Tags: [BFS, DFS, PriorityQueue]
      

#### BFS
- if already found a good/shorter route, skip
- `if (distMap[node.x][node.y] <= node.dist) continue;`
- This always terminates the possibility to go return to original route, because the dist will be double/higher



---

**242. [Predict the Winner.java](https://github.com/awangdev/LintCode/blob/master/Java/Predict%20the%20Winner.java)**      Level: Medium      Tags: [DP, MiniMax]
      

Detailed in `Coins in a Line III`



---

**243. [Group Shifted Strings.java](https://github.com/awangdev/LintCode/blob/master/Java/Group%20Shifted%20Strings.java)**      Level: Medium      Tags: [Hash Table, String]
      


#### Convert to orginal string
- shit by offset. `int offset = s.charAt(0) - 'a';`
- increase if less than 'a': `if (newChar < 'a') newChar += 26;`

#### Previous notes
- 相同shift规则的string, 能被推算到同一个零起始点，就是共同减去一个char,最后就相等。以此作为key，用HashMap。一目了然。
- 记得根据题目意思，一开始要String[] sort一下。



---

**244. [Delete Digits.java](https://github.com/awangdev/LintCode/blob/master/Java/Delete%20Digits.java)**      Level: Medium      Tags: [Greedy, Priority Queue]
      

#### Priority Queue
- TODO: parse into node(index, digitValue)
- find the top k, and remove from char array
- O(nlogn) time

#### Greedy
- 数位靠前的，权值更大. 所以硬来把靠前的相对更大的（跟following digit相比）去掉。



---

**245. [Flatten 2D Vector.java](https://github.com/awangdev/LintCode/blob/master/Java/Flatten%202D%20Vector.java)**      Level: Medium      Tags: [Design]
      

Implement an iterator to flatten a 2d vector.

Just move pointers carefully with next(), hashNext()

#### Basic Implementation using x, y corrdinate
- 就是把2D list里面的element全部遍历一遍。
- 跟一个nxn的matrix遍历，是没区别的拉; 所有来个x,y，把2d list跑一变。

#### Always return item at index 0, and remove from list?
- list 方便remove, 考虑吧reduce input vector (就像给的是linked list 一样)



---

**246. [The Spiral Matrix II.java](https://github.com/awangdev/LintCode/blob/master/Java/The%20Spiral%20Matrix%20II.java)**      Level: Medium      Tags: [Array]
      

#### Move forward till end
- Similar concept as `The Maze`: keep walking until hit wall, turn back
- fix direction `dx[direction % 4]`



---




 
 
 
## Hard (91)
**0. [Count of Smaller Number before itself.java](https://github.com/awangdev/LintCode/blob/master/Java/Count%20of%20Smaller%20Number%20before%20itself.java)**      Level: Hard      Tags: []
      
与Count of Smaller Number非常类似。以实际的value来构成segment tree，leaf上存（count of smaller number）。

Trick: 先Query，再modify.   
每次Query时候，A[i]都还没有加入到Segment Tree 里面，而A[i+1,...etc]自然也还没有加进去。   
那么就自然是coutning smaller number before itself.   
刁钻啊！   

另外注意：   
在modify里面：多Check了root.start <= index 和  index <= root.end。 过去都忽略了。以后可以把这个也写上。   
（其实是Make sense的，就是更加严格地check了index再 root.left 或者 root.right里面的站位）   



---

**1. [Kth Smallest Sum In Two Sorted Arrays.java](https://github.com/awangdev/LintCode/blob/master/Java/Kth%20Smallest%20Sum%20In%20Two%20Sorted%20Arrays.java)**      Level: Hard      Tags: []
      

用priority queue. 每次把最小的展开，移位。分别x+1,或者y+1:   
因为当下的Min里面x,y都是最小的。所以下一个最小的不是（x+1,y）,就是（x,y+1）。

每次就poll（）一个，放2个新candidate进去就好了。
注意，这样的做法会用重复，比如例子（7,4）会出现两次。用一个HashSet挡一下。

注意，HashSet的唯一性，用一个"x,y"的string就可以代为解决。



---

**2. [LFU Cache.java](https://github.com/awangdev/LintCode/blob/master/Java/LFU%20Cache.java)**      Level: Hard      Tags: [Design, Hash Table]
      

#### Hash Table
- 具体看thoughts, 几种不同的方式使用map
- `regular object map`: map of <key, item>, where `item : {int val; int count}`
- Use a Map<frequency count, doubly-linked node> to track the frequency
- Track constant capacity, and minimum frequency
- Every get(): update all frequency map as well
- Every put(): update all frequency map as well, with optional removal (if over capacity)

- Original post: http://www.cnblogs.com/grandyang/p/6258459.html
- TODO: one doubly linked list might be good enough to replace below:
- `frequency list map`: map of <frequency count, List<item>>, where the list preserves `recency`
- `item location in frequency map`: map of <key, int location index in list>:
- index relative to the item in a particular list, not tracking which list here



---

**3. [Prefix and Suffix Search.java](https://github.com/awangdev/LintCode/blob/master/Java/Prefix%20and%20Suffix%20Search.java)**      Level: Hard      Tags: [Trie]
      



---

**4. [Remove Node in Binary Search Tree.java](https://github.com/awangdev/LintCode/blob/master/Java/Remove%20Node%20in%20Binary%20Search%20Tree.java)**      Level: Hard      Tags: [BST]
      

方法1: Brutle一点。找到target和target的parent.    
把target remove时，把target的children nodes 重新排列组成新的BST: inorder traversal, build tree based on inorder traversal list.

方法2: 分析规律,先找到target和parent, 然后根据性质，把target remove时，移动children nodes, 保证还是BST。



---

**5. [Subarray Sum II.java](https://github.com/awangdev/LintCode/blob/master/Java/Subarray%20Sum%20II.java)**      Level: Hard      Tags: [Array, Binary Search, Two Pointers]
      



---

**6. [k Sum.java](https://github.com/awangdev/LintCode/blob/master/Java/k%20Sum.java)**      Level: Hard      Tags: [DP]
      

DP. 公式如何想到, 还需要重新理解.

dp[i][j][m]: # of possibilities such that from j elements, pick m elements and sum up to i. 
i: [0~target]

dp[i][j][m] = dp[i][j-1][m] + dp[i - A[j - 1]][j-1][m-1]
            (i not included)   (i included)



---

**7. [Copy Books.java](https://github.com/awangdev/LintCode/blob/master/Java/Copy%20Books.java)**      Level: Hard      Tags: [Binary Search, DP, Partition DP]
      

给一串书pages[i], k个人, pages[i] 代表每本书的页数. k个人从不同的点同时开始抄书. 

问, 最快什么时候可以抄完?

#### Partition DP
- 第一步, 理解题目要求的问题: 前k个人copy完n本书, 找到最少的用时; 也可以翻译成: `n本书, 让k个人来copy, 也就是分割成k段`.
- 最后需要求出 dp[n][k]. 开: int[n+1][k+1]. 
- 原理:
- 1. 考虑最后一步: 在[0 ~ n - 1]本书里, 最后一个人可以选择copy 1 本, 2 本....n本, 每一种切割的方法的结果都不一样
- 2. 讨论第k个人的情况, 在 j = [0 ~ i] 循环. 而循环j时候最慢的情况决定 第k个人的结果(木桶原理): `Math.max(dp[j][k - 1], sum)`. 
- 3. 其中: `dp[j][k-1]` 是 [k-1]个人读完j本书的结果, 也就是著名的`上一步`. 这里循环考虑的是第k个人不同的j种上一步 : )
- 4. 循环的结果, 是要存在 dp[i][k] = Math.min(Math.max(dp[j][k - 1], sum[j, i]), loop over i, k, j = [i ~ 0])
- Time: O(kn^2), space O(nk)

##### Init
- Init: dp[0][0] = 0, 0个人0本书
- Integer.MAX_VALUE的运用:
- 当 i = 1, k = 1, 表达式: dp[i][k] = Math.min(dp[i][k], Math.max(dp[j][k - 1], sum));
- 唯一可行的情况就只有一种: i=0, k=0, 刚好 0 个人 copy 0 本书, dp[0][0] = 0.
- 其他情况, i = 1, k = 0, 0 个人读 1本书, 不可能发生: 所以用Integer.MAX_VALUE来冲破 Math.max, 维持荒谬值.
- 当 i=0, k=0 的情况被讨论时候, 上面的方程式才会按照实际情况计算出 dp[i][k]
- 这道题的init是非常重要而tricky的

##### 计算顺序
- k个人, 需要一个for loop; 
- k个人, 从copy1本书开始, 2, 3, ... n-1,所以 i=[1, n], 需要第二个for loop
- 在每一个i上, 切割的方式可以有[0 ~ i] 中, 我们要计算每一种的worst time

##### 滚动数组
- [k] 只有和 [k - 1] 相关
- Space: O(n)

#### Binary Search
- 根据: 每个人花的多少时间(time)来做binary search: 每个人花多久时间, 可以在K个人之内, 用最少的时间完成?
- time variable的范围不是index, 也不是page大小. 而是[minPage, pageSum]
- validation 的时候注意3种情况: 人够用 k>=0, 人不够所以结尾减成k<0, 还有一种是time(每个人最多花的时间)小于当下的页面, return -1
- O(nLogM). n = pages.length; m = sum of pages.




---

**8. [Scramble String.java](https://github.com/awangdev/LintCode/blob/master/Java/Scramble%20String.java)**      Level: Hard      Tags: [DP, Interval DP, String]
      

- 给两个string S, T. 检验他们是不是scramble string.
- scramble string 定义: string可以被分拆成binary tree的形式, 也就是切割成substring;
- 旋转了不是leaf的node之后, 形成新的substring, 这就是原来string的 scramble.


#### Interval DP 区间型
- 降维打击, 分割, 按照长度来dp.
- dp[i][j][k]: 数组S从index i 开始, T从index j 开始, 长度为k的子串, 是否为scramble string

##### Break down
- 一切两半以后, 看两种情况: , 或者不rotate这两半. 对于这些substring, 各自验证他们是否scramble.
- 不rotate分割的两半: S[part1] 对应  T[part1] && S[part2] 对应  T[part2]. 
- rotate分割的两半: S[part1] 对应  T[part2] && S[part2] 对应  T[part1]. 

##### Initialization
- len == 1的时候, 其实无法旋转, 也就是看S,T的相对应的index是否字符相等.
- initialization非常非常重要. 很神奇, 这个initailization 打好了DP的基础, 后面一蹴而就, 用数学表达式就算出了结果.
- input s1, s2 在整个题目的主要内容里面, 几乎没有用到, 只是用在initialization时候.
- More details, 看解答



---

**9. [Interleaving String.java](https://github.com/awangdev/LintCode/blob/master/Java/Interleaving%20String.java)**      Level: Hard      Tags: [DP, String]
      

双序列DP, 从最后点考虑.
拆分问题的末尾, 考虑和s1, s2 subsequence之间的关联.

求存在性, boolean




---

**10. [Edit Distance.java](https://github.com/awangdev/LintCode/blob/master/Java/Edit%20Distance.java)**      Level: Hard      Tags: [DP, Double Sequence DP, Sequence DP, String]
      
time: O(MN)
Space: O(N)

两个字符串, A要变成B, 可以 insert/delete/replace, 找最小变化operation count

#### Double Sequence
- 考虑两个字符串的末尾index s[i], t[j]: 如果需要让这两个字符一样, 可能使用题目给出的三种operation: insert/delete/replace?
- 先calculate最坏的情况, 3种operation count + 1; 然后在比较match的情况.
- 注意, 在i或者j为0的时候, 变成另外一个数字的steps只能是全变.
- 第一步, 空间时间都是O(MN), O(MN)
- 滚动数组优化, 空间O(N)

##### Detail analysis
- insert: assume insert on s, `#ofOperation = (s[0 ~ i] to t[0 ~ j-1]) + 1;`
- delete: assume delete on t, `#ofOperatoin = (s[0 ~ i - 1] to t[0 ~ j]) + 1;`
- replace: replace both s and t, `#ofOperatoin = (s[0 ~ i - 1] to t[0 ~ j - 1]) + 1;`
- dp[i][j]代表了两个 sequence 互相之间的性质: s[0 ~ i] 转换成 s[0~j] 所需要的最少 operation count
- init: 当i==0, dp[0][j] = j; 每次都要 + j 个character; 同理, 当j==0, dp[i][0] = i;
- 而dp[i][j]有两种情况处理: `s[i] == t[j]` or `s[i] != t[j]`

##### 何时initialize
- 这种判断取决于经验: 如果知道initialization可以再 double for loop 里面一起做, 那么可以留着那么做
- 这样属于 `需要什么, initialize什么`
- 事后在做space optimization的时候, 可以轻易在 1st dimension 上做rolling array

#### Search
- 可以做, 但是不建议:这道题需要找 min count, 而不是search/find all solutions, 所以search会写的比较复杂, 牛刀杀鸡.



---

**11. [Distinct Subsequences.java](https://github.com/awangdev/LintCode/blob/master/Java/Distinct%20Subsequences.java)**      Level: Hard      Tags: [DP, String]
      

Double Sequence DP:
0. DP size (n+1): 找前nth的结果, 那么dp array就需要开n+1, 因为结尾要return dp[n][m]
1. 在for loop 里面initialize dp[0][j] dp[i][0]
2. Rolling array 优化成O(N): 如果dp[i][j]在for loop里面, 就很好替换 curr/prev



---

**12. [Ones and Zeroes.java](https://github.com/awangdev/LintCode/blob/master/Java/Ones%20and%20Zeroes.java)**      Level: Hard      Tags: [DP]
      

还是Double Sequence, 但是考虑第三种状态: 给的string array的用量.
所以开了3维数组.

如果用滚动数组优化空间, 需要把要滚动的那个for loop放在最外面, 而不是最里面.
当然, 这个第三位define在 dp[][][]的哪个位置, 问题都不大.

另外, 注意在外面calcualte zeros and ones, 节约时间复杂度.



---

**13. [Word Break II.java](https://github.com/awangdev/LintCode/blob/master/Java/Word%20Break%20II.java)**      Level: Hard      Tags: [Backtracking, DFS, DP, Hash Table, Memoization]
      

找出所有 word break variations, given dictionary

利用 memoization: `Map<prefix, List<suffix variations>>`

#### DFS + Memoization
- Realize the input s expands into a tree of possible prefixes.
- We can do top->bottom(add candidate+backtracking) OR bottom->top(find list of candidates from subproblem, and cross-match)
- DFS on string: find a valid word, dfs on the suffix. [NO backtraking in the solution]
- DFS returns List<String>: every for loop takes a prefix substring, and append with all suffix (result of dfs)
- IMPORANT: Memoization: `Map<prefix, List<suffix variations>>`, which reduces repeated calculation if the substring has been tried.
- Time O(n!). Worst case, permutation of unique letters: `s= 'abcdef....'`, and `dict=[a,b,c,d,e,f...]`

#### Regular DPs
- 两个DP一起用, 解决了timeout的问题: when a invalid case 'aaaaaaaaa' occurs, isValid[] stops dfs from occuring
- 1. isWord[i][j], subString(i,j)是否存在dict中？
- 2. 用isWord加快 isValid[i]: [i ～ end]是否可以从dict中找到合理的解？      
- 从末尾开始查看i：因为我们需要测试isWord[i][j]时候，j>i, 而我们观察的是[i,j]这区间；       
- j>i的部分同样需要考虑，我们还需要知道isValid[0～j+1]。 所以isValid[x]这次是表示[x, end]是否valid的DP。     
- i 从 末尾到0, 可能是因为考虑到isWord[i][j]都是在[0~n]之内，所以倒过来数，坐标比较容易搞清楚。     
- (回头看Word Break I， 也有坐标反转的做法)
- 3. dfs 利用 isValid 和isWord做普通的DFS。

#### Timeout Note
- Regarding regular solution: 如果不做memoization或者dp, 'aaaaa....aaa' will repeatedly calculate same substring
- Regarding double DP solution: 在Word Break里面用了set.contains(...), 在isValid里面，i 从0开始. 但是, contains()本身是O(n); intead,用一个isWord[i][j]，就O(1)判断了i~j是不是存在dictionary



---

**14. [Minimum Window Substring.java](https://github.com/awangdev/LintCode/blob/master/Java/Minimum%20Window%20Substring.java)**      Level: Hard      Tags: [Hash Table, String, Two Pointers]
      

基本思想: 用个char[]存string的frequency. 然后2pointer, end走到底, 不断validate.
符合的就process as result candidate.

HashMap的做法比char[]写起来要复杂一点, 但是更generic



---

**15. [Longest Substring with At Most K Distinct Characters.java](https://github.com/awangdev/LintCode/blob/master/Java/Longest%20Substring%20with%20At%20Most%20K%20Distinct%20Characters.java)**      Level: Hard      Tags: [Hash Table, Sliding Window, String]
      

大清洗 O(nk)   
map.size一旦>k，要把longest string最开头（marked by pointer:start）的那个char抹掉    
一旦某一个char要被清除，所以在这个char 的1st and last appearance之间的char都要被清洗from map




---

**16. [Find Minimum in Rotated Sorted Array II.java](https://github.com/awangdev/LintCode/blob/master/Java/Find%20Minimum%20in%20Rotated%20Sorted%20Array%20II.java)**      Level: Hard      Tags: [Array, Binary Search]
      

一个需要严谨思考的题目. 因为有duplicate, 会导致不断平移, 所以最终time complexity是O(n)
所以不如直接扫一遍, 给出答案.

但是还是写一个Binary Search的样子, 只不过worst结果是O(n)



---

**17. [Number of Islands II.java](https://github.com/awangdev/LintCode/blob/master/Java/Number%20of%20Islands%20II.java)**      Level: Hard      Tags: [Union Find]
      

给一个island grid[][], and list of operations to fill a particualr (x,y) position.

count # of remaining island after each operation.

#### Union Find, model with int[]
- 把board转换成1D array， 就可以用union-find来判断了. 
- 用int[] father 的unionFind, 需要转换2D position into 1D index. 这样比较clean
- 判断时，是在四个方向各走一步，判断是否是同一个Land.
- 每走一次operator，都会count++. 若发现是同一个island, count--
- count的加减, 都放在了UnionFind自己的function里面, 方便tracking, 给几个helper function就对了.
- Time: O(k * log(mn))

#### Union Find, model with Hashmap 
- 用HashMap的Union-find.


#### Note:
- Proof of UnionFind log(n) time: https://en.wikipedia.org/wiki/Proof_of_O(log*n)_time_complexity_of_union%E2%80%93find



---

**18. [Word Search II.java](https://github.com/awangdev/LintCode/blob/master/Java/Word%20Search%20II.java)**      Level: Hard      Tags: [Backtracking, DFS, Trie]
      

给一串words, 还有一个2D character matrix. 找到所有可以形成的words. 条件: 2D matrix 只可以相邻走位.

#### Trie, DFS
- 相比之前的implementation, 有一些地方可以优化:
- 1. Backtracking时候, 在board[][] 上面mark就可以, 不需要开一个visited[][]
- 2. 不需要implement trie的所有方程, 用不到: 这里只需要insert.
- 普通的trie题目会让你search a word, 但是这里是用一个board, 看board的每一个字母能不能走出个Word.
- 也就是: 这里的search是自己手动写, 不是传统的trie search() funcombination
- 3. TrieNode里面存在 end的时候存string word, 表示到底. 用完了 word = null, 刚好截断重复查找的问题.

##### 关于Trie
- Build Trie with target words: insert, search, startWith. Sometimes, just: `buildTree(words)` and return root.
- 依然要对board matrix做DFS。
- no for loop on words. 直接对board DFS:   
- 每一层,都会有个up-to-this-point的string. 在Trie里面check它是不是存在。以此判断。   
- 若不存在，就不必继续DFS下去了。
- Trie solution time complexity, much better:      
- build Trie:   n * wordMaxLength
- search: boardWidth * boardHeight * (4^wordMaxLength + wordMaxLength[Trie Search])


#### Regular DFS
- for loop on words: inside, do board DFS based on each word.     
- Time cpmplexity: word[].length * boardWidth * boardHeight * (4^wordMaxLength)

#### Previous Notes
- Big improvement: use boolean visited on TrieNode!     
- 不要用rst.contains(...), 因为这个是O(n) 在leetcode还是会timeout（lintcode竟然可以pass）!    
- 在Trie search() method 里面，凡是visit过的，mark一下。  




---

**19. [Word Squares.java](https://github.com/awangdev/LintCode/blob/master/Java/Word%20Squares.java)**      Level: Hard      Tags: [Backtracking, Trie]
      

可以开Trie class, 里面用到TrieNode. 开Trie(words) 可以直接initalize with for loop
TrieNode 里面可以有一个 List<String> startWith: 记录可以到达这个点的所有string: 有点像树形, ancestor形状的存储.

神操作:
根据square的性质, 如果选中了list of words, 设定 int prefixIndex = list.size().
取出list里面的所有word[prefixedIndex], 并且加在一起, 就是下一个word candidate的 prefix.

形象一点:
list = ["ball", "area"];
prefixIndex = list.size(); ball[prefixIndex] = 'l'; area[prefixIndex] = 'e';
//then
candidatePrefix = ball[prefixIndex] + area[prefixIndex] = "le";
这里就可以用到Trie的那个 findByPrefix function, 在每个点, 都存有所有这个点能产生的candidate.
这时, 试一试所有candidate: dfs

能想到这种倒转的结构来存prefix candidates 在 Trie里面, 这个想法非常值得思考.



---

**20. [Trapping Rain Water.java](https://github.com/awangdev/LintCode/blob/master/Java/Trapping%20Rain%20Water.java)**      Level: Hard      Tags: [Array, Stack, Two Pointers]
      

这道题目的方法比较多.
#### 方法1
Array, 维持一个左手最高墙array, 右手最高强array.
对于每个index而言, vertically 能存放的最大水柱, 就是靠左右最高墙决定的:
min(leftHighestWall, rightHighestWall) - currHeight.

#### 方法2
方法1上面的优化, two pointer, 还是找左边最高和右边最高. O(1) space.
利用到了方法3里面的想法一样: 整个structure是被中间的最高bar 二分天下:
左边按照maxLeft来计算, 右边按照maxRight来计算.

#### 方法3
2 Pointers， 双面夹击:
1. 找中间最高bar的index    
2. 两面往中心扫：每次加上（topBarIndex - currIndex）* (elevation from previous index).也就是每次加一个横条。    
3. 每次还要减去block自身的height

#### 方法4
主要想法和方法3一致: 在山坡下坡的基础上, 一直用stack堆积bottom. 
最后遇到上升之前, 此时bottom可以用来跟stack之前堆积的所有下坡index做比较, 算跟他们高度相差的积水.
用了stack记录下坡, 然后用个while loop一挖到底的想法非常棒.




---

**21. [Largest Rectangle in Histogram.java](https://github.com/awangdev/LintCode/blob/master/Java/Largest%20Rectangle%20in%20Histogram.java)**      Level: Hard      Tags: [Array, Monotonous Stack, Stack]
      

给n个bar,组成柱状图histogram. 求在这一排柱状图里面可以找到的面积最大的长方形.

思考: 找长方形面积, 无非是找两个index, 然后底边长度 * height.

#### Monotonous Stack
- 重点是根据找Histogram里面rectangle的性质, 维持一个单调递增的Stack
- 在loop over indexes的时候:
- 如果高度>= previous peek(), 那么对于那个peek, 就意味着, 往下走, 一直走高嘛, 之前的peek总可以继续抄底
- 什么时候不能抄底了呢? 就是有一个下降趋势的时候
- 这时候并不是calculate所有前面的peek, 而是考虑 大于 current height的之前所有的peek.
- 把这些peek到 current height 前一格的rectangle全部找出来: stack.pop()
- 这个stack.pop()的过程里面, 其实没有算上 current height, 因为需要留到下一轮, 把current index加进stack 再说
- 为什么用stack? 因为需要知道连续递增的peek, stack.peek() O(1), 好用
  而其实不用stack, 也可以用其他方式记录所有height, 只不过要 O(n)去找peek不方便

#### 知识点
- 理解monotonous stack 是如何被维护的
- 维护monotonous stack 是题目需要, 而不是stack本身性质, 是一种借助 stack.peek() O(1)的巧妙用法.




---

**22. [Find Peak Element II.java](https://github.com/awangdev/LintCode/blob/master/Java/Find%20Peak%20Element%20II.java)**      Level: Hard      Tags: [Binary Search, DFS, Divide and Conquer]
      

2Dmatrix, 里面的value有一些递增, 递减的特点(细节比较长, 看原题). 目标是找到peak element

peak: 比周围4个方向的点value大

#### DFS

##### 基本原理
- 我们不可能一口气准确定位(x,y), 但是我们可以再一个row/col里面, 找到1D array的 peak.
- 根据这个点, 再往剩下两个方向移动
- 1. 在中间的一行i=midX, 找到peak所在的y.
- 2. 在中间的一列j=midY, 找到peak所在的x. (有可能强势override之前找到的y, 也就是放弃那一行的peak, 在midY上找peak)
- 3. 根据 (x,y) 的4个neighbor check (x,y)是不是 peak, 如果不是, 像更高的位置移动一格
- 4. 根据之前算的 midX, midY 把board分成4个象限, 在每一份里面再继续找
- 这个题目LintCode不给做了, 所以思路对的, 但是解答还没有再次验证.

##### 剪枝/切分象限
- 每次只是找到一个row/col里面的peak而已!
- 找到这个点, 就等于把board切成了两半.
- 然后, 再跟剩下的相邻的两个位置比较, 就知道了哪里更大, 就去哪里找peak, 也就是又切了第二刀.
- 切第二刀的时候, 也要把(x, y) 移到需要取的象限. 进行DFS
- 根据mid row 切割: 
- http://www.jiuzhang.com/solution/find-peak-element-ii/#tag-highlight-lang-java
- http://courses.csail.mit.edu/6.006/spring11/lectures/lec02.pdf

##### 时间复杂度
- 每一个level都减一半
- T(n) = n + T(n/2) = n + n/2 + n/4 + ... + 1 = n(1 + 1/2 + .... + 1/n) = 2n = O(n)

#### Binary Search
- TODO
- O(nLogN)



---

**23. [Palindrome Pairs.java](https://github.com/awangdev/LintCode/blob/master/Java/Palindrome%20Pairs.java)**      Level: Hard      Tags: [Hash Table, String, Trie]
      

Obvious的做法是全部试一遍, 判断, 变成 O(n^2) * O(m) = O(mn^2). O(m): isPalindrome() time.

当然不行了, 那就看是O(nlogN), 还是O(n)?

#### 方法1: Hash Table + Palindrome的性质. 复合型.
O(mn)

##### 思路
- 每一个word, 都可以拆分成 front + mid + end. 如果这个word + 其他word可以组成palindrome,那就是说
- 砍掉 (mid+end), front.reverse() 应该存在 words[] 里面.
- 砍掉 (front+mid), end.reverse() 应该存在 words[] 里面.
- 我们用HashMap存所有的<word, index>, 然后reverse, 找配对就好.

##### Corner case
- 如果有 empty string "", 那么它跟任何一个palindrome word, 都可以配对, 并且根据位置前后变换, 凑成2份 distinct indexes.
- 这样就有了那个 `if (reverseEnd.equals("")) {...}` 的logic.
- 注意: 虽然在处理砍头/砍尾的两个 for loop里面都在根据 empty string 重复记录, 
  但因为 "" 自己本身不能作为起点, 所以overall只会在被其他palindrome配对时记录一次.


#### 方法2: Trie
还要做一下那.



---

**24. [Maximal Rectangle.java](https://github.com/awangdev/LintCode/blob/master/Java/Maximal%20Rectangle.java)**      Level: Hard      Tags: [Array, DP, Hash Table, Stack]
      

#### 方法1: monotonous stack
分解开来, 其实是'Largest Rectangle in Histogram', 只不过这里要自己model heights.
一个2D array里面的rectangle, 最终也是用height * width做出来的.
巧妙在于, 把每一行当做底边, 算出这个底边, 到顶部的height: 
- 如果底边上的一个value==0, 那么算作没有height(以这个底边做rectangle, value==0的位置是空中楼阁, 不能用)
- 如果底边上的value==1, 那么就把上面的height加下来, 做成histogram

如果看具体实例, 有些row似乎是白算的, 但是没有办法, 这是一个搜索的过程, 最终会比较出最优解.

#### 方法2: DP
Coordinate DP?



---

**25. [Longest Increasing Path in a Matrix.java](https://github.com/awangdev/LintCode/blob/master/Java/Longest%20Increasing%20Path%20in%20a%20Matrix.java)**      Level: Hard      Tags: [Coordinate DP, DFS, DP, Memoization, Topological Sort]
      

m x n 的matrix, 找最长增序的序列长度. 这里默认连续的序列.

- 接成圈是不行的, 所以visit过得 (x,y)就不能再去了.
- 斜角方向不能走, 只能走上下左右
- 无法按照坐标DP来做, 因为计算顺序4个方向都可以走.
- 最终要visit所有node, 所以用DFS搜索比较合适.

#### DFS, Memoization
- 简单版: longest path, only allow right/down direction: 
- `dp[x][y] = Math.max(dp[prevUpX][prevUpY], or dp[prevUpX][prevUpY] + 1)`; and compare the other direction as well
- This problem, just compare the direction from dfs result
- DFS太多重复计算; memoization (dp[][], visited[][]) 省去了重复计算
- initialize dp[x][y] = 1, (x,y) 自己也算path里的一格
- dfs(matrix, x, y): 每次检查(x,y)的4个neighbor (nx, ny), 如果他们到(x,y)是递增, 那么就考虑和比较:
- Maht.max(dp[x][y], dp[nx][ny] + 1); where dp[n][ny] = dfs(matrix, nx, ny)
- top level: O(mn), 尝试从每一个 (x,y) 出发
- O(m * n * k), where k is the longest path

#### Topological sort
还没有做



---

**26. [Coins in a Line III.java](https://github.com/awangdev/LintCode/blob/master/Java/Coins%20in%20a%20Line%20III.java)**      Level: Hard      Tags: [Array, DP, Game Theory, Interval DP, Memoization]
      

LeetCode: Predict the Winner

还是2个人拿n个coin, coin可以有不同的value. 

只不过这次选手可以从任意的一头拿, 而不限制从一头拿. 算先手会不会赢?

#### Memoization + Search
- 跟Coins in a Line II 一样, MaxiMin的思想: 找到我的劣势中的最大值
- `dp[i][j] 代表在[i,j]区间上 选手最多能取的value 总和`
- 同样, sum[i][j]表示[i] 到 [j]间的value总和
- 对手的最差情况, 也就是先手的最好情况:
- dp[i][j] = sum[i][j] - Math.min(dp[i][j - 1], dp[i + 1][j]);
- 这里需要search, 画出tree可以看明白是如何根据取前后而分段的.

#### 博弈 + 区间DP, Interval DP
- 因为是看区间[i,j]的情况, 所以可以想到是区间 DP
- 这个方法需要复习, 跟数学表达式的推断相关联: S(x) = - S(y) + m. 参考下面的公式推导.
- dp[i][j]表示 从index(i) 到 index(j), 先手可以拿到的最大值与对手的数字差. 也就是S(x).
- 其中一个S(x) = dp[i][j] = a[i] - dp[i + 1][j]
- m 取在开头, m 取在末尾的两种情况:
- dp[i][j] = max{a[i] - dp[i + 1][j], a[j] - dp[i][j - 1]}
- len = 1, 积分就是values[i]
- 最后判断 dp[0][n] >= 0, 最大数字和之差大于0, 就赢.
- 时间/空间 O(n^2)

##### 公式推导
- S(x) = X - Y, 找最大数字和之差, 这里X和Y是选手X的总分, 选手Y的总分. 
- 对于选手X而言: 如果S(x)最大值大于0, 就是赢了; 如果最大值都小于0, 就一定是输了. 
- 选手Y: S(y)来表示 对于Y,  最大数字和之差. S(y) = Y - X
- 根据S(x) 来看, 如果从 数字和X里面, 拿出一个数字 m, 也就是 X = m + Xwithout(m)
- S(x) = m + Xwithout(m) - Y = m + (Xwithout(m) - Y). 
- 如果我们从全局里面索性去掉m, 那么 S(y'') = Y - Xwithout(m)
- 那么推算下来: S(x) = m + (Xwithout(m) - Y) = m - (Y - Xwithout(m)) = m - S(y'')
- 在这个问题里面, 我们model X 和 Y的时候, 其实都是 dp[i][j], 而区别在于先手/后手.
- 将公式套用, 某一个S(x) = a[i] - dp[i + 1][j],  也就是m=a[i], 而 S(y'') = dp[i + 1][j]

##### 注意
- 如果考虑计算先手[i, j]之间的最大值, 然后可能还需要两个数组, 最后用于比较先手和opponent的得分大小 => 那么就要多开维.
- 我们这里考虑的数字差, 刚好让人不需要计算先手的得分总值, 非常巧妙.
- Trick: 利用差值公式, 推导有点难想到.

##### 区间型动态规划
- 找出[i, j]区间内的性质: dp[i][j]下标表示区间范围 [i, j]
- 子问题: 砍头, 砍尾, 砍头砍尾
- loop应该基于区间的length
- template: 考虑len = 1, len = 2; 设定i的时候一定是 i <= n - len; 设定j的时候, j = len + i - 1;




---

**27. [Burst Balloons.java](https://github.com/awangdev/LintCode/blob/master/Java/Burst%20Balloons.java)**      Level: Hard      Tags: [DP, Divide and Conquer, Interval DP, Memoization]
      

一排球, 每个球有value, 每次扎破一个, 就会积分: 左*中间*右 的值. 求, 怎么扎, 最大值?

TODO: Need more thoughts on why using dp[n + 2][n + 2] for memoization, but dp[n][n] for interval DP.

#### Interval DP
- 因为数组规律会变, 所以很难找'第一个burst的球'. 反之, 想哪一个是最后burst?
- 最后burst的那个变成一堵墙: 分开两边, 分开考虑, 加法原理; 最后再把中间的加上.
- dp[i][j] represent max value on range [i, j)
- Need to calculate dp[i][j] incrementally, starting from range size == 3 ---> n
- Use k to divide the range [i, j) and conquer each side.

##### Interval DP 三把斧:
- 中间劈开
- 砍断首或尾
- Range区间作为iteration的根本

##### Print the calculation process
- use pi[i][j] and print recursively.
- Print k, using pi[i][j]: max value taken at k

#### Memoization
- 其实会做之后挺好想的一个DP
- dp[i][j] =  balloons i~j 之间的 max. 
- 然后找哪个点开始burst? 设为x。
- For loop 所有的点作为x， 去burst。
- 每次burst都切成了三份：左边可以recusive 求左边剩下的部分的最大值 + 中间3项相乘 + 右边递归下去求最大值。
- Note: 这个是Memoization, 而不纯是DP
- 因为recursive了，其实还是搜索，但是memorize了求过的值，节省了Processing




---

**28. [K Edit Distance.java](https://github.com/awangdev/LintCode/blob/master/Java/K%20Edit%20Distance.java)**      Level: Hard      Tags: [DP, Double Sequence DP, Sequence DP, Trie]
      

给一串String, target string, int k. 找string array里面所有的candidate: 变化K次, 能变成target.

#### Trie
TODO

#### Double Sequence DP
- Edit Distance的follow up.
- 其实就是改一下 minEditDistance的function, 带入K作比较罢了.
- 写起来跟Edit Distance 的主要逻辑是一模一样的.
- 但是LintCode 86% test case 时候timeout. 
- Time O(mnh), where h = words.length, 如果 n ~ m, Time 就几乎是 O(n^2), 太慢.



---

**29. [Paint House II.java](https://github.com/awangdev/LintCode/blob/master/Java/Paint%20House%20II.java)**      Level: Hard      Tags: [DP, Sequence DP, Status DP]
      
time: O(NK^2):
space: (NK)

一排n个房子, 每个房子可涂成k种颜色, 涂每个房子的价钱不一样, 用costs[][]表示. 

costs[0][1]表示涂了index是0的房子, 用了color 1.

规则: 相邻的两个房子不能使同一种颜色

求: 最少的cost 

#### DP
- 跟Paint House I 几乎一模一样, 只不过paint color更多了: k colors.
- 先考虑单纯地用dp[i]表示涂前 i 个房子的最小cost
- 但是 dp[i] 和 dp[i-1] 两个index选什么颜色会互相影响, 难讨论, 于是加状态: 序列DP被加了状态变成2D. 
- 考虑最后位, 而前一位i-1又被i位的颜色限制, 于是在考虑 min dp[i] 时候, 又多了一层iteration.
- 做dp[i][j]: # cost for 前 i 个房子, 所以要先pick (i-1) 房子的cost, 然后在找出 (i-2)房子的cost
- K种颜色 => O(NK^2)
- 如果不优化, 跟Paint House I 几乎是一模一样的代码
- Time O(NK^2), space(NK)
- Rolling array: reduce space to O(K)

#### 注意
- 序列型dp[i]表示'前i-1个'的结果. 所以dp最好设定为 int[n + 1] size. 
- 然而, 颜色在这里是状态, 所以保留在 j: [ 0~k)
- [[8]] 这样的edge case. 跑不进for loop, 所以特殊handle.

#### Optimization Solution
- Time: O(NK)
- 如果已知每次都要从cost里面选两个不同的最小cost,那么先把最小两个挑出来, 就不必有第三个for loop 找 min
- 每次在数列里面找: 除去自己之外的最小值, 利用最小值/次小值的思想
- 维持2个最值: 最小值/次小值. 
- 计算的时候, 如果除掉的不是最小值的index, 就给出最小值; 如果除掉的是最小值的index, 就给出次小值.
- Every loop: 1. calculate the two min vlaues for each i; 2. calcualte dp[i][j]
- 如何想到优化: 把表达式写出来, 然后看哪里可以优化
- 另外, 还是可以rolling array, reduce space complexity to O(K)



---

**30. [Best Time to Buy and Sell Stock III.java](https://github.com/awangdev/LintCode/blob/master/Java/Best%20Time%20to%20Buy%20and%20Sell%20Stock%20III.java)**      Level: Hard      Tags: [Array, DP, Sequence DP]
      

比stock II 多了一个限制：只有2次卖出机会.

#### DP加状态
- 只卖2次, 把买卖分割成5个状态模块.
- 在状态index 0, 2, 4: 没有持有股票. 1. 一直在此状态, max profit不变; 2. 刚卖掉, dp[i][前状态] + profit
- 在状态index 1, 3: 持有股票. 1. 一直在此状态, daily profit. 2. 刚刚买进, 状态改变, 但是没有profit yet: dp[i][前状态]

##### Partial profit
- 把每天的partial profit (diff)加在一起, 最终的overall profit是一样的. 唯一更好的是, 不需要记录中间买入的时间点.
- 什么时候会积累profit呢? 
- 1. 原本就持有股票的, 如果毫无动作, 那么状态不变, 积累profit diff. 
- 2. 卖出了股票, 状态改变, 积累profit diff.
- 注意: 只有在状态index: 0, 2, 4, 也就是卖掉股票的时候, 才可以积累profit

##### Rolling Array
- [i] 只有和 [i-1] 打交道, reduce space
- O(1) space, O(n) time

#### 找峰头
- 找峰头；然后往下再找一个峰头。
- 怎么样在才能Optimize两次巅峰呢？从两边同时开始找Max！（棒棒的想法）
- leftProfit是从左往右，每个i点上的最大Profit。
- rightProfit是从i点开始到结尾，每个点上的最大profit.
- 那么在i点上，就是leftProfit，和右边rightProfit的分割点。在i点，leftProfit+rightProfit相加，找最大值。
- 三个O(n),还是O(n)



---

**31. [Best Time to Buy and Sell Stock IV.java](https://github.com/awangdev/LintCode/blob/master/Java/Best%20Time%20to%20Buy%20and%20Sell%20Stock%20IV.java)**      Level: Hard      Tags: [DP, Sequence DP]
      

有int[] price of stock, 最多做 k transactions.  求最大profit.

#### DP
- 根据StockIII, 不难发现StockIV就是把状态划分为2k+1份. 那么同样的代码, 移植.

##### 注意1: 
- 如果k很大, k>n/2, 那么长度为n的数组里面, 最多也只能n/2个transaction
- 那么题目简化为stockII, 给n数组, 无限次transaction.
- 注意, status的数量是 2k+1
- Time O(NK), Space O(2k+1) to store the status

##### 注意2: 
- 最后状态是'没有stock'的都该考虑, 做一个 for 循环比较max. 
- 当然, 来一个profit variable, 不断比较, 也是可以的.

#### 方法2
- (previous notes, 熟练第一种方法的思考就可以)
- 记得要理解：为什么 i-1天的卖了又买，可以和第 i 天的卖合成一次交易？    
- 因为每天交易的price是定的。所以卖了又买，等于没卖！这就是可以合并的原因。要对价格敏感啊少年。
- Inspired from here: http://liangjiabin.com/blog/2015/04/leetcode-best-time-to-buy-and-sell-stock.html

##### 局部最优解 vs. 全局最优解：     
- local[i][j] = max(global[i – 1][j – 1] + diff, local[i – 1][j] + diff)    
- global[i][j] = max(global[i – 1][j], local[i][j])     
- local[i][j]: 第i天，当天一定进行第j次交易的profit     
- global[i][j]: 第i天，总共进行了j次交易的profit.

- local[i][j]和global[i][j]的区别是：local[i][j]意味着在第i天一定有交易（卖出）发生。    
- 当第i天的价格高于第i-1天（即diff > 0）时，那么可以把这次交易（第i-1天买入第i天卖出）跟第i-1天的交易（卖出）合并为一次交易，即local[i][j]=local[i-1][j]+diff；    
- 当第i天的价格不高于第i-1天（即diff<=0）时，那么local[i][j]=global[i-1][j-1]+diff，而由于diff<=0，所以可写成local[i][j]=global[i-1][j-1]。    
- (Note:在我下面这个solution里面没有省去 +diff）   

- global[i][j]就是我们所求的前i天最多进行k次交易的最大收益，可分为两种情况：    
- 如果第i天没有交易（卖出），那么global[i][j]=global[i-1][j]；     
- 如果第i天有交易（卖出），那么global[i][j]=local[i][j]。    





---

**32. [Russian Doll Envelopes.java](https://github.com/awangdev/LintCode/blob/master/Java/Russian%20Doll%20Envelopes.java)**      Level: Hard      Tags: [Binary Search, Coordinate DP, DP]
      

俄罗斯套娃, 这里用envelope来表现. 给一串array, 每一个[x, y] 是envelope 长宽. [[5,4],[6,4],[6,7],[2,3]]. 

看用这些套娃, 可以最多套几个.

#### DP: 1D Coordinate
- envelopes没有顺序, 先排序 (主要根据第一个index排序)
- 然后观察: 排序过后, 就变成了1D的坐标动态规划.
- max number 取决于上一个成功Russian doll的 max value + 1
- 上一个index不知道, 所以遍历找上一个index. 
- 当下index i 的状态, 取决于前面index j 的状态, 所以遍历两个index.
- O(n^2)的DP, n = envelopes.length;

#### DP: 2D Coordinate
- 这个方法是自己想出来的, 但是时间复杂度太大, timeout
- 把envelop标记在2D grid上面, 然后像走机器人一样, 求到最右下角的最大 count max.
- count 当下能存在多少Russian doll
- 两种情况: 当下coordinate 没有target, 当下coordinate有target
- 当下coordinate 没有target: 如同机器人走法, Math.max(dp[i - 1][j], dp[i][j - 1])
- 当下coordinate 有target: dp[i - 1][j - 1] + dp[i][j]
- timeout: O(n^2), n = largest coordinate.




---

**33. [Expression Tree Build.java](https://github.com/awangdev/LintCode/blob/master/Java/Expression%20Tree%20Build.java)**      Level: Hard      Tags: [Binary Tree, Expression Tree, Minimum Binary Tree, Stack]
      

给一串字符, 表示的是 公式 expression. 把公式变成expression tree

#### Monotonous Stack
- 和Max-tree一样，https://leetcode.com/problems/maximum-binary-tree
- 用到bottom->top递增的stack: 最底下的root维持成最小的element.
- 这个题目是Min-tree， 头上最小，Logic 和max-tree如出一辙   
- Space: O(n) 
- Time on average: O(n).

#### 特点
- TreeNode: 用一个并不是最终结果的TreeNode, 存weight, 用来排序
- 用base weight的概念权衡同一个层面的 符号, 数字 顺序
- 每一个character都是一个节点, 都有自己的weight. 用一个TreeNode来存weight value, 利用用weight来判断: 
- 1. (while loop) 如果node.val <= stack.peek().nodeValue, 把当前stack.peek() 变成 left child. 
- 2. (if condition) 如果stack有残余, 把当前node变成 stack.peek().rightChild 




---

**34. [Expression Evaluation.java](https://github.com/awangdev/LintCode/blob/master/Java/Expression%20Evaluation.java)**      Level: Hard      Tags: [Binary Tree, DFS, Expression Tree, Minimum Binary Tree, Stack]
      

给一个公式 expression, array of strings, 然后evaluate expression 结果.

#### DFS on Expression Tree
- 计算 expression 的值: 1. 建造 expression tree. 2. DFS计算结果
- Expression Tree: Minimum Binary Tree (https://lintcode.com/en/problem/expression-tree-build/)
- build好Min Tree以后，做PostTraversal. 
- Divde and Conquer: 先recursively找到 left和right的大小， 然后evaluate中间的符号
- Time, Space O(n), n = # expression nodes

#### Note
- 1. Handle数字时，若left&&right Child全Null,那必定是我们weight最大的数字node了。   
- 2. 若有个child是null,那就return另外一个node。    
- 3. prevent Integer overflow　during operation:过程中用个Long，最后结局在cast back to int.



---

**35. [Convert Expression to Polish Notation.java](https://github.com/awangdev/LintCode/blob/master/Java/Convert%20Expression%20to%20Polish%20Notation.java)**      Level: Hard      Tags: [Binary Tree, DFS, Expression Tree, Stack]
      

给一串字符, 用来表示公式expression. 把这个expression转换成 Polish Notation (PN).

#### Expression Tree
- Expression Tree: Minimum Binary Tree (https://lintcode.com/en/problem/expression-tree-build/)
- 根据题意做出Expression Tree出来以后: 来个Pre-order-traversal 就能记录下 Polish Notation
- 本题没有给'ExpressionTreeNode', 所以把TreeNode就当做成我们需要的node, 里面扩展成有left/right child就可以了.
- Note: label需要是String. 虽然 Operator是长度为1的char, 但是数字可为多位



---

**36. [Convert Expression to Reverse Polish Notation.java](https://github.com/awangdev/LintCode/blob/master/Java/Convert%20Expression%20to%20Reverse%20Polish%20Notation.java)**      Level: Hard      Tags: [Binary Tree, DFS, Expression Tree, Stack]
      

给一串字符, 用来表示公式expression. 把这个expression转换成 Reverse Polish Notation (RPN).

#### Expression Tree
- Expression Tree: Minimum Binary Tree (https://lintcode.com/en/problem/expression-tree-build/)
- 根据题意做出Expression Tree出来以后: 来个Post-order-traversal 就能记录下 Reverse Polish Notation
- 本题没有给'ExpressionTreeNode', 所以把TreeNode就当做成我们需要的node, 里面扩展成有left/right child就可以了.



---

**37. [Decode Ways II.java](https://github.com/awangdev/LintCode/blob/master/Java/Decode%20Ways%20II.java)**      Level: Hard      Tags: [DP, Enumeration, Partition DP]
      

给出一串数字, 要翻译(decode)成英文字母. [1 ~ 26] 对应相对的英文字母. 求有多少种方法可以decode.

其中字符可能是 "*", 可以代表 [1 - 9]

#### DP
- 乘法原理
- 跟decode way I 一样, 加法原理, 切割点时: 当下是取了 1 digit 还是 2 digits 来decode
- 定义dp[i] = 前i个digits最多有多少种decode的方法. new dp[n + 1].
- 不同的情况是: 每一个partition里面, 如果有"*", 就会在自身延伸出很多不同的可能
- 那么: dp[i] = dp[i - 1] * (#variations of ss[i]) + dp[i - 2] * (#variations of ss[i,i+1])

##### 特点
- 枚举的能力: 具体分析 '*' 出现的位置, 枚举出数字, 基本功. 
- 注意!!题目说 * in [1, 9].   (如果 0 ~ 9 会更难一些)
- 理解取MOD的原因: 数字太大, 取mod来给最终结果: 其实在 10^9 + 7 这么大的 mod 下, 大部分例子是能通过的.
- 枚举好以后, 其实这个题目的写法和思考过程都不难




---

**38. [Palindrome Partitioning II.java](https://github.com/awangdev/LintCode/blob/master/Java/Palindrome%20Partitioning%20II.java)**      Level: Hard      Tags: [DP, Partition DP]
      

给一个String s, 找出最少用多少cut, 使致 切割出的每一个substring, 都是palindrome

#### Partition DP
- Find minimum cut: 分割型DP
- dp[i]: 最少cut多少刀, 使得前 i 长度的string, 割出来都是palindrome
- 最终要得到 dp[n], 所以 int[n + 1]
- 移动切刀, 看在哪里切, index j in [0 ~ i]
- 考虑[j, i - 1] 是否是回文串, 如果是, 那么: dp[i]= min(dp[i], d[j] + 1).
- note: 估计遍历 j 的时候, 反过来遍历也可以.

#### 计算Palindrome的优化
- 利用palindrome的性质, 可以算出 boolean palindrome[i, j]的情况. 
- 找一个任意mid point:
- 1. 假设palindrome是奇数长度, 那么 mid 是单独的字符, 而两边的字符 [mid-1], [mid+1] 应该完全相等.
- 2. 假设palindrome是偶数长度, 那么 [mid] 和 [mid + 1] 这样位置的字符应该相等.
- 这样做出来 palindrome[i, j]: 从字符 i 到 字符 j 的 substring 是否是 palindrome
- 这样就给我们的问题合理降维, 目前是time: O(n^2). 
- 不然求一次palindrome, 就是n, 会变成O(n^3)

#### Previous Notes
- Double for loop 检查每种substring string (i~j). 若i,j相邻或者同点，那么肯定isPal；否则，i,j之间的（i+1, j-1）一定得isPal。
- 看上去，在检查i,j的时候，中间按的（i+1, j-1）怎么可能先知道？ 其实不然..在j慢慢长大的时候，所有的0~j的substring都检查过。所以isPal[i+1][j-1]一定是已经知道结果的。
- okay.那么假如以上任意一种情况成立，也就是说isPal[i][j] == true。那就要判断，切到第一层循环参数j的末尾点时，有多少种切法？
- 想法很顺：我们naturally会想到，把i之前的cut加上i~j之间发生的不就好了。
- 反正现在j不变，现在就看吧i定在哪里，cut[i - 1]是否更小/最小； 再在cut[i-1]基础上+1就完了。
- 当然，如果i==0, 而 i~j又是isPal,那没啥好谈的，不必切，0刀。
- 最终，刷到cut[s.length() - 1] 也就是最后一点。 return的理所应当。




---

**39. [Backpack III.java](https://github.com/awangdev/LintCode/blob/master/Java/Backpack%20III.java)**      Level: Hard      Tags: [Backpack DP, DP]
      

给n种不同的物品, int[] A weight, int[] V value, 每种物品可以用无限次

问最大多少value可以装进size是 m 的包?

#### DP
- 可以无限使用物品, 就失去了last i, last unique item的意义: 因为可以重复使用.
- 所以可以转换一个角度:
- 1. 用i **种** 物品, 拼出w, 并且满足题目条件(max value). 这里因为item i可以无限次使用, 所以考虑使用了多少次K.
- 2. K虽然可以无限, 但是也被 k*A[i]所限制: 最大不能超过背包大小.
- dp[i][w]: 前i种物品, fill weight w 的背包, 最大价值是多少.
- dp[i][w] = max {dp[i - 1][w - k*A[i-1]] + kV[i-1]}, k >= 0
- Time O(nmk)
- 如果k = 0 或者 1, 其实就是 Backpack II: 拿或者不拿

#### 优化
- 优化时间复杂度, 画图发现:
- 所计算的 (dp[i - 1][j - k*A[i - 1]] + k * V[i - 1]) 
- 其实跟同一行的 dp[i][j-A[i-1]] 那个格子, 就多出了 V[i-1]
- 所以没必要每次都 loop over k times
- 简化: dp[i][j] 其中一个可能就是: dp[i][j - A[i - 1]] + V[i - 1]
- Time O(mn)

#### 空间优化到1维数组
- 根据上一个优化的情况, 画出 2 rows 网格
- 发现 dp[i][j] 取决于: 1. dp[i - 1][j], 2. dp[i][j - A[i - 1]]
- 其中: dp[i - 1][j] 是上一轮 (i-1) 的结算结果, 一定是已经算好, ready to be used 的
- 然而, 当我们 i++,j++ 之后, 在之前 row = i - 1, col < j的格子, 全部不需要.
- 降维简化: 只需要留着 weigth 这个 dimension, 而i这个dimension 可以省略: 
- (i - 1) row 不过是需要用到之前算出的旧value: 每一轮, j = [0 ~ m], 那么dp[j]本身就有记录旧值的功能.
- 变成1个一位数组
- 降维优化的重点: 看双行的左右计算方向
- Time(mn). Space(m)



---

**40. [First Missing Positive.java](https://github.com/awangdev/LintCode/blob/master/Java/First%20Missing%20Positive.java)**      Level: Hard      Tags: [Array]
      

给一串无序数字, 有负数: 找这个array里面第一个 missing的 positive integer

missing positive integer 其实是以 [1, n] 来做比较的.

#### Array分析, index 技巧
- 用while loop, 不断地尝试把 number 送到该放的地方
- 如果 index = nums[i] 超过了nums.length, 当然就不移动了
- 注意: 检查 val != nums[val], avoid infinitely loop
- 检验: nums[i] 是否等于 i, 如果不对, 就找到了结果

#### Edge Case
- 如果nums==null, 其实missing positive integer 自然而然是 1
- validation时, 有可能这串数字里没有断开的integer, 但是最大的integer在首位 (因为index超标, 无法被放到正确的地方)
- 这种时候, n被放在 index 0, 其实就是说, 下一个integer应该是 n + 1
- 最终, 如果array本来就是完全sorted, 也不缺, 还符合角标的条件, 那么唯一下一个就是array范围外的第一个positive number: n



---

**41. [N-Queens.java](https://github.com/awangdev/LintCode/blob/master/Java/N-Queens.java)**      Level: Hard      Tags: [Backtracking]
      

N-Queen 问题, 给数字n, 和 nxn board, 找到所有N-queens的答案.

#### Backtracking
- 用dfs找所有情况, 每一个iteration, 从找一行里挑合适的点, dfs
- 选中的点加进candidate list 里面, 记得要backtracking.
- 每一个candidate都需要validation, 检查 row, col, 2 diagnal 有没有queen

#### validate n queue at certain (x, y)
- 1. array 里面不能有 target row#
- 2. diagnal. 记得公式：
- row1 - row2 == col1 - col2.     Diagnal elelment.fail
- row1 - row2 == - (col1 - col2). Diagnal element. fail
- Draw a 3x3 board to test the 2 scanarios:
- (0,0) and (3,3) are diagnal
- (0,2) and (2,0) are diagnal




---

**42. [N-Queens II.java](https://github.com/awangdev/LintCode/blob/master/Java/N-Queens%20II.java)**      Level: Hard      Tags: [Backtracking]
      

跟 N-Queens 一样, 不是找所有结果, 而是count多少结果.

#### Backtracking
- 当list.size() == n 的时候，说明找到了一个Solution。
- 1. dfs function (List<Integer>, n)
- 2. validate function



---

**43. [LRU Cache.java](https://github.com/awangdev/LintCode/blob/master/Java/LRU%20Cache.java)**      Level: Hard      Tags: [Design, Hash Table, Linked List]
      

#### Double Linked List
- 用了一个特别的双向的ListNode，有了head和tail，这样就大大加快了速度。     
- 主要加快的就是那个‘更新排位’的过程，找到item hashmap O(1), 做减法换位也都是O(1)
- Overall O(1)

##### 巧妙点
- 1. head和tail特别巧妙：除掉头和尾，和加上头和尾，就都特别快。    
- 2. 用双向的pointer: pre和next, 当需要除掉任何一个node的时候，只要知道要除掉哪一个，     
- 直接把node.pre和node.next耐心连起来就好了，node就自然而然的断开不要了。     
- 一旦知道怎么解决了，就不是很特别，并不是难写的算法:    
- moveToHead()    
- insertHead()    
- remove()      

#### O(n) 检查重复
- timeout method, 天真的来了一个O(n) 的解法，结果果然timeout.     
- 一个map<key,value>存数值。一个queue<key>来存排位。     
- 每次有更新，就把最新的放在末尾；每次超过capaticity,就把大头干掉。很简单嘛，但是跑起来太久，失败了。     




---

**44. [Binary Tree Maximum Path Sum.java](https://github.com/awangdev/LintCode/blob/master/Java/Binary%20Tree%20Maximum%20Path%20Sum.java)**      Level: Hard      Tags: [DFS, DP, Tree, Tree DP]
      

找max path sum,  可以从任意treeNode 到任意 treeNode.

#### Kinda, Tree DP
- 两个情况: 1. combo sum: left+right+root; 2. single path sum
- Note1: the path needs to be continuous, curr node cannot be skipped
- Note2: what about I want to skip curr node: handled by lower level of dfs(), where child branch max was compared.
- Note3: skip left/right child branch sum, by comparing with 0. 小于0的, 没必要记录

#### DP的思想
- tree给我们2条branch, 每条branch就类似于 dp[i - 1], 这里类似于dp[left], dp[right] 这样
- 找到 dp[left], dp[right] 以后, 跟 curr node结合. 
- 因为是找max sum, 并且可以skip nodes, 所以需要全局变量max
- 每次dfs() return的一定是可以继续 `continuously link 的 path`, 所以return `one single path sum + curr value`.

#### DFS, PathSum object
- that just solves everything


---

**45. [Basic Calculator.java](https://github.com/awangdev/LintCode/blob/master/Java/Basic%20Calculator.java)**      Level: Hard      Tags: [Binary Tree, Expression Tree, Math, Minimum Binary Tree, Stack]
      

给一个expression String, 要evaluate这个expression的值.

Expression string 里面包括 +, -, 整数, 开合括号, 还有space.

#### Expression Tree
- Expression Tree是一个 weight-based的 min-tree 
- 基于 运算符号 + 数字的 tree: 数字永远在leaf, 然后符号是tree node,  括号不出现在tree里面
- 用 monotonuous stack 来构建这个tree

##### Thinking points
- Understand Expression Tree
- Use stack to build the expression tree + understand the weight system
- Use post-order traversal to evaluate the tree
- 注意, input里面的数字不会是single digit, 所以需要一个buffer存number string
- 整个题目的做法, 可以参照 `Expression Evaluation`



---

**46. [Longest Consecutive Sequence.java](https://github.com/awangdev/LintCode/blob/master/Java/Longest%20Consecutive%20Sequence.java)**      Level: Hard      Tags: [Array, Hash Table, Union Find]
      

给一串数字, unsorted, 找这串数字里面的连续元素序列长度 (consecutive序列, 是数字连续, 并不是说要按照原order)

#### HashSet
- 要想看连续元素, 必须要num++, num--这样搜索
- 1. 需要O(1)找到元素
- 2. 需要简单快速找到 num - 1, num + 1.
- 如果用min,max开array, 耗费空间
- 用HashSet来存, 用set.contains() 来查找 num - 1, num + 1 存在与否
- for loop. O(n) 
- 里面的while loop 一般不会有O(n); 一旦O(n), 也意味着set 清零, for loop也不会有更多 inner while 的衍生.
- overall O(n) 时间复杂度


#### Union Find
- 最终是要把相连的元素算一下总长, 其实也就是把元素group起来, 相连的group在一起, 于是想到UnionFind
- 这里用到了一个`int[] size` 来帮助处理 `合并的时候parent是哪个`的问题: 永远往group大的union里去
- main function 里面, 有一个map来track, 每个元素, 只处理1遍.
- union的内容: current number - 1, current number + 1
- https://www.jianshu.com/p/e6b955ca208f

##### 特点
- Union Find 在index上做好像更加容易
- 其他union find function: `boolean connected(a,b){return find(a) == find(b)}`



---

**47. [Serialize and Deserialize Binary Tree.java](https://github.com/awangdev/LintCode/blob/master/Java/Serialize%20and%20Deserialize%20Binary%20Tree.java)**      Level: Hard      Tags: [BFS, DFS, Deque, Design, Divide and Conquer, Tree]
      

Serialize and Deserialize Binary Tree

#### DFS, Divide and Conquer
##### Serilize
- Divide and conquer: Pre-order traversal to link all nodes together
- build the string data: use '#' to represent null child. 
- the preorder string, can be parsed apart by `split(',')`

##### Deserialize
- Use a list (here we use `Deque` for the ease of get/remove in 1 function: remove()) 
- to take all parts of the parsed sring data: dfs on the Deque
- first node from the list is always the head
- '#' will be a null child: this should break dfs
- Deque is a global variable, so dfs(right child) will happen after dfs(left child) completes

#### DFS, Recursive [previous note]
- serilize: divide and conquer, pre-order traversal
- deserialize: 稍微复杂, 用dfs. 每次要truncate input string: 
- 一直dfs找left child, 接着right child until leaf is found.
- 用一个StringBuffer来hold string, 因为string 是primitive, 我们这里需要pass reference

#### BFS, Non-recursive
- using queue. 想法直观。level-order traversal. save到一个string里面就好。
- 遇到null child, 不是直接忽略, 而是assign一个Integer.MIN_VALUE, 然后 mark as '#'
- BFS需要track queue size, 每一次只process特定数量的nodes



---

**48. [Count of Smaller Numbers After Self.java](https://github.com/awangdev/LintCode/blob/master/Java/Count%20of%20Smaller%20Numbers%20After%20Self.java)**      Level: Hard      Tags: [BST, Binary Indexed Tree, Binary Search, Divide and Conquer, Segment Tree]
      

给一串数字nums[], 求一个新数组result, where result[i] = # of smaller items on right of nums[i]

#### Binary Search
- sort and insert 进一个新list, 新的list是sorted
- 从末尾 i = n-1 遍历nums[]
- 每一次insert nums[i] 进list的位置, 就是# of smaller items on right side of nums[i]
- 每次记录下result[i]
- **问题**: 这里的binary search 是用 `end = list.size(); while(start<end){...}`做的, 可否换成用`end=list.size() - 1`?


#### Segment Tree based on actual value
- Build segment tree based on min/max values of array: set each possible value into leaf
- query(min, target - 1): return count # of smaller items within range [min, target - 1]
- Very similar to `Count of Smaller Number`, where segment tree is built on actual value!!
- IMPORTANT: goal is to find elements on right -> elements processed from left-hand-side can be removed from segment tree
- Use `modify(root, target, -1)` to remove element count from segment tree. Reuse function
- time: `n * log(m)`, where m = Math.abs(max-min). log(m) is used to modify() the leaf element

##### Segment Tree solution - tricky part:
- negative nubmer works oddly with mid and generates endless loop in build(): `[-2, -1]` use case
- build entire segment tree based on [min, max], where min must be >= 0. 
- we can do this by adding Math.abs(min) onto both min/max, as well as +diff during accessing nums[i]



#### Binary Indexed Tree
- TODO, have code



---

**49. [Remove Duplicate Letters.java](https://github.com/awangdev/LintCode/blob/master/Java/Remove%20Duplicate%20Letters.java)**      Level: Hard      Tags: [Greedy, Hash Table, Stack]
      

#### Hash Table, Greedy
- count[] = int[256], 不需要 `c-'a'`
- boolean visited[]: 一旦一个字母固定了位置后, 再次遇到时候, 直接跳过用过的character
- 如果tail字母可以变小, 那就delete掉tail, 重新接上新字母 (前提条件: 去掉的字母后面还会再出现, set visited[tail] = false)
- Space: O(1) count[], visited[].
- Time: Go through all letters O(n)

#### Stack
- Use stack instead of stringBuffer: keep append/remove last added item
- However, stringBuffer appears to be faster than stack.



---

**50. [Expression Add Operators.java](https://github.com/awangdev/LintCode/blob/master/Java/Expression%20Add%20Operators.java)**      Level: Hard      Tags: [Backtracking, DFS, Divide and Conquer, String]
      

给一个数字String, 数字来自`0-9`, 给3个操作符 `+`,`-`,`*`, 看如何拼凑, 可以做出结果target.

output 所有 expression

#### string dfs, use list to track steps (backtracking)
- 跟string相关, 写起来可能稍微繁琐一点
- 数字有 dfs([1,2,3...]) 组合方法
- operator有[`+`,`-`,`*`] 3种组合方法
- 注意1: 乘号要特殊处理, pass along 连乘的数字, 计算下一步乘积的时候, 要 sum - preProduct + product
- 注意2: '01' 这种数字要skip
- 注意3: 第一个选中数字不需要加操作符, 直接加进去
- Time: O(4^n)， Space: O(4^n)
- T(n) = 3 * T(n-1) + 3 * T(n-2) + 3 * T(n-3) + ... + 3 *T(1);
- T(n-1) = 3 * T(n-2) + 3 * T(n-3) + ... 3 * T(1);
- Thus T(n) = 4T(n-1) = 4^2 * T(n - 1) = .... O(4^n)

#### String dfs, use string as buffer
- 逻辑一样, 代码更短, 只不过不做list, 直接pass `buffer + "+" + curr`
- 因为每次都创建新string, 所以速度稍微慢一点. Time complexity 一样



---

**51. [Insert Interval.java](https://github.com/awangdev/LintCode/blob/master/Java/Insert%20Interval.java)**      Level: Hard      Tags: [Array, PriorityQueue, Sort]
      

#### Sweep Line
- Interval 拆点，PriorityQueue排点
- Merge时用count==0作判断点
- 注意, 一定要compare curr `p.x == queue.peek().x` 确保重合的点全部被process: `count+=p.x`
- PriorityQueue: O(logN). 扫n点, 总共：O(nLogn)


#### Basic Implementation
- 这里已经给了 **sorted** intervals by start point.
- 直接找到可以insert newInterval的位子. Insert
- 然后loop to merge entire interval array
- 因为给的是个list, 所以方便`intervals.remove(i)`
- remove之前都会重新assgin `pre.end`, 确保被remove的node.end 被capture
- O(n) 

#### 另外
- 因为interval已经sort, 本想用Binary Search O(logn). 
- 但是找到interval insert position 最后 merge还是要用 O(n), 所以不必要 binary Search



---

**52. [Shortest Palindrome.java](https://github.com/awangdev/LintCode/blob/master/Java/Shortest%20Palindrome.java)**      Level: Hard      Tags: [KMP, String]
      

#### Divide by mid point, Brutle
- check (mid, mid+1), or (mid-1, mid+1).
- If the two position matches, that is a palindrome candidate
- 比较front string 是否是 end string 的substring
- O(n^2)
- timeout on last case: ["aaaaaa....aaaacdaaa...aaaaaa"]

#### KMP
- TODO



---

**53. [K Empty Slots.java](https://github.com/awangdev/LintCode/blob/master/Java/K%20Empty%20Slots.java)**      Level: Hard      Tags: [Array, BST, TreeSet]
      

题目解析后: find 2 number, that: 1. k slots between the 2 number, 2. no slots taken between the two number.

#### BST
- BST structure not given, use TreeSet to build BST with each node
- Every time find last/next inorder element 
- `treeSet.lower(x)`, `treeSet.higher(x)`
- 一旦位置相隔(k + 1), 就满足题目条件
- O(nlogn), good enough

#### Track slots of days
- Reverse the array, save days index into days[], where the new index is slot.
- days[i]: at slot i, which day a flower will be planted
- O(n)
- Needs to understand: http://www.cnblogs.com/grandyang/p/8415880.html



---

**54. [Count of Range Sum.java](https://github.com/awangdev/LintCode/blob/master/Java/Count%20of%20Range%20Sum.java)**      Level: Hard      Tags: [BST, Divide and Conquer, Merge Sort, PreSum]
      

TODO: Write the code + merge function

#### Divide and Conquer + PreSum + MergeSort
- 算法非常厉害就是了: 先做presum[], 那么 sum range [i,j] 就等于是preSum[j+1] - preSum[i]
- 分治: 考虑[start, mid] range里面的结果, 再考虑[mid, end] range里面的结果. (分开来 mergeSort)
- 最后考虑[low,high]总体的结果
- 小技巧: PreSum 做成了 (n + 1) length, 那么求range sum [i,j] 就可以简化成 preSum[j] - preSum[i]
- NOTE: should write merge() function, but that is minor, just use `Arrays.sort(nums, start, end)`, OJ passed
- Every mergeSort() has a for loop => O(n log n)

##### 如何 count range?
- 这里比较特别的一个做法: 找一个 [low, mid]里面的i, mid 之后的preSum作比较 (解释源自: https://blog.csdn.net/qq508618087/article/details/51435944)
- 即在右边数组找到两个边界, 设为`m, n`, 
- 其中m是在右边数组中第一个使得`sum[m] - sum[i] >= lower`的位置, 
- n是第一个使得`sum[n] - sum[i] > upper`的位置, 
- 这样`n-m`就是与左边元素i所构成的位于`[lower, upper]`范围的区间个数. 

##### 神奇的重点: 为什么要 merge and sort
- 边界[lower, higher] 在 sorted array 好作比较, 一旦国界, 就可以停止计算, 减少不必要计算.
- 上面这个n,m的做法可行的前提: preSum[]里面前后两个 range[low, mid], [mid, high]已经sorted了
- 也就是说, 在recursively mergeSort()的时候, 真的需要merge sorted 2 partitions
- 也许会问: 能不能sort呢, sort不久打乱了顺序? 对,打乱的是preSum[]的顺序.
- 但是不要紧: 很巧妙的, 分治的时候, 前半段/后半段 都在原顺序保留的情况下 分开process完了, 最后才merge
- 在做m,n 的range的时候, 原理如下, 比如preSum被分成这么两段: `[A,B,C]`, `[D,E,F]`
- 每一个preSum value `A` 在跟 preSum[i] 作比较的时候 `A - preSum < lower`, 都是单一作比较, 不牵扯到 B, C
- 因此, `[A, B, C]` 是否保留一开始 preSum的顺序在此时不重要
- 此时最重要的是, `[A,B,C]`以及排序好, 那么在于 `lower` boundary 作比较的时候, 一旦过界, 就可以停止计算(减少不必要的计算)


#### BST
- TODO?



---

**55. [Max Sum of Rectangle No Larger Than K.java](https://github.com/awangdev/LintCode/blob/master/Java/Max%20Sum%20of%20Rectangle%20No%20Larger%20Than%20K.java)**      Level: Hard      Tags: [Array, BST, Binary Search, DP, Queue, TreeSet]
      

给定一个非空的二维矩阵matrix与一个整数k，在矩阵内部寻找和不大于k的最大矩形和。

#### BST, Array, preSum
- 将问题reduce到: row of values, find 1st value >= target.
- 1. loop over startingRow; 2. loop over [startingRow, m - 1]; 3. Use TreeSet to track areas and find boundary defined by k.
- When building more rows/cols the rectangle, total sum could be over k: 
- when it happens, just need to find a new starting row or col, 
- where the rectangle area can reduce/remain <= k
- 找多余area的起始点: extraArea = treeSet.ceiling(totalSum - k). 也就是找 减去k 后 起始的/左边的area.
- 去掉这些左边的起始area, 剩下的就 <=k.    (num - extraArea)
- 为什么用TreeSet: area的大小无规律, 并且要找 >= 任意值 的第一个value. 给一串non-sorted数字, 找 >= target的数, 如果不写binary search, 那么用BST最合适
- O(m^2*nlogn)

#### 思想
- 从最基本的O(m^2*n^2) 考虑: 遍历 startingRow/startingCol
- rectangle? layer by layer? 可以想到Presum的思想, 大于需要的sum的时候, 减掉多余的部分
- 如何找到多余的area? 那么就是search: 把需要search的内容存起来, 可以想到用BST(TreeSet), 或者自己写Binary Search.



---

**56. [Perfect Rectangle.java](https://github.com/awangdev/LintCode/blob/master/Java/Perfect%20Rectangle.java)**      Level: Hard      Tags: [Design, Geometry, Hash Table]
      

看的list of coordinates 是否能组成perfect rectangle, 并且不允许overlap area.

#### 画图发现特点
- 特点1: 所有给出的点(再找出没有specify的对角线点), 如果最后组成perfect rectangle, 都应该互相消除, 最后剩下4个corner
- 特点2: 找到所有点里面的min/max (x,y), 最后组成的 maxArea, 应该跟过程中accumulate的area相等
- 特点1确保中间没有空心的部分, 保证所有的重合点都会互相消除, 最后剩下4个顶点
- 特点2确保没有重合: 重合的area会最终超出maxArea



---

**57. [Max Points on a Line.java](https://github.com/awangdev/LintCode/blob/master/Java/Max%20Points%20on%20a%20Line.java)**      Level: Hard      Tags: [Array, Geometry, Hash Table, Math]
      

给list of (x,y) coordinates. Determine  # of points on the same line

#### Observation
- If given n points, we can calculate all possible slopes. O(n^2) times
- For the two dots that generates the same slope, these dots could be on **parallel** slopes
- figure out how to prune the parallel dots

#### Trick: prune parallel dots using greatest common divider
- GCD: greatest common divider
- Devide the x and y by their greatest common divider, such that x and y can be reduced to minimum value
- All other x and y can be reduced to such condition as well
- track the final reduced (x,y) in a map: they are the key to the count
- No need to use Map<Integer, Map<Integer, Integer>> to perform 2 level mapping; just `map<String, Integer>`, where the key is "x@y"



---

**58. [Number of Digit One.java](https://github.com/awangdev/LintCode/blob/master/Java/Number%20of%20Digit%20One.java)**      Level: Hard      Tags: [Math]
      

Pure math problem, not quite representative

Explanation
https://leetcode.com/problems/number-of-digit-one/discuss/64381/4+-lines-O(log-n)-C++JavaPython



---

**59. [Binary Representation.java](https://github.com/awangdev/LintCode/blob/master/Java/Binary%20Representation.java)**      Level: Hard      Tags: [Bit Manipulation, String]
      

#### String
- 首先要分两半解决，断点是'.': str.split("\\.");
- Integer那一半好弄，whie loop里: num%2, num/2. 做一个 `parseInteger()` function
- Decimal那边复杂点. 做一个 `parseDecimal()` function:
- bit == 1的数学条件: 当下num * 2 >= 1。 更新: num = num * 2 - 1;
- bit == 0的数学条件: num * 2 < 1. 更新: num = num * 2

#### 注意
- num是 double, 小数在 `num = num * 2 - 1` 的公式下可能无限循环
- 因此check: num重复性，以及binary code < 32 bit.
- 所以题目也才有了32BIT的要求!



---

**60. [Recover Binary Search Tree.java](https://github.com/awangdev/LintCode/blob/master/Java/Recover%20Binary%20Search%20Tree.java)**      Level: Hard      Tags: [BST, DFS, Tree]
      

BST里面有2个node misplace, 要归为. 要求: O(1) extra space

#### Observation
- BST inorder traversal should give small -> large sequence
- misplaced means: a **large**->small item would occur, and later a large>**small** would occur. 
- The first large && second small item are the 2 candidates. Example
- [1, 5,  7, 10,    12, 15, 18]
- [1, 5, `15, 10`, `12,  7`, 18]

#### dfs, O(1) extra space
- traverse, and take note of the candidate
- at the end, swap value of the 2 candidates

#### O(n) space
- inorder traversal the nodes and save in array, find the 2 items misplanced and swap them
- But O(n) space should not be allowed




---

**61. [Jump Game II.java](https://github.com/awangdev/LintCode/blob/master/Java/Jump%20Game%20II.java)**      Level: Hard      Tags: [Array, Coordinate DP, DP, Greedy]
      

给一串数字 是可以跳的距离. goal: 跳到最后的index 所可能用的最少次数.

#### Greedy
- always aiming for the `farest can go`
- if the `farest can go` breaches the end, return steps
- otherwise, send `start=end+1`, `end=farest` and keep stepping from here
- though trying with 2 loops, worst case [1,1,1,...1,1] could have O(n^2)
- But on average should be jumpping through the array without looking back
- time: average O(n)

#### Previous Notes, Greedy
- 维护一个range, 是最远我们能走的. 
- index/i 是一步一步往前, 每次当 i <= range, 做一个while loop， 在其中找最远能到的地方 maxRange
- 然后更新 range = maxRange
- 其中step也是跟index是一样, 一步一步走.
- 最后check的condition是，我们最远你能走的range >= nums.length - 1, 说明以最少的Step就到达了重点。Good.

#### Even simpler Greedy
- 图解 http://www.cnblogs.com/lichen782/p/leetcode_Jump_Game_II.html
- track the farest point
- whenver curr index reachest the farest point, that means we are making a nother move, so count++
- there seems to have one assumption: must have a solution. Otherwise, count will be wrong number. 
- 其实跟第一个greedy的思维模式是一模一样的.


#### DP 
- DP[i]: 在i点记录，走到i点上的最少jump次数
- dp[i] = Math.min(dp[i], dp[j] + 1);
- condition (j + nums[j] >= i)
- 注意使用 dp[i] = Integer.MAX_VALUE做起始值, 来找min
- time: O(n^2), slow, and timesout



---

**62. [Longest Valid Parentheses.java](https://github.com/awangdev/LintCode/blob/master/Java/Longest%20Valid%20Parentheses.java)**      Level: Hard      Tags: [Coordinate DP, Stack, String]
      

给一串string, 里面只有`(`, `)`. 找最长valid parentheses 的长度.

#### 1D Coordinate DP
- use dp[i] track local max, maintain global max
- int[] dp. dp[i]: longest valid string that ends on i.
- 结尾是 ')', 2种情况: 1. 刚好s[i-1]是'('; 2. s[i]的')'更前面的一个起始'(' 对应
- 注意, 结尾如果是'('属于不合理情况, 忽略.
- init: dp[0] = 0, 单个char不可能成型.
- 计算顺序: 从左到右, 找local max, maintain global max
- O(n) space, O(n) runtime

#### Stack
- Stack 里面存所有的open/close parentheses.
- 如果遇到stack.top()刚好开合结掉, 就stack.pop().
- 剩下的都是不合理的elements.
- 有点像negatively找 solution: `endIndex - 最后一个failedIndex(stack.pop()) - 1`, 应该就是最后一个succeeded string的长度
- 每次更新 endIndex 为stack.top(), 然后从stack继续找下一个failedIndex
- 所有的length作比较, 就可以找出最长length
- O(n) stack space, O(n) runtime. 应该比dp慢一点, 因为做了2遍O(n)




---

**63. [Rearrange String k Distance Apart.java](https://github.com/awangdev/LintCode/blob/master/Java/Rearrange%20String%20k%20Distance%20Apart.java)**      Level: Hard      Tags: [Greedy, Hash Table, Heap]
      

给一个string, 全是lowercase letter, 要求重新排列: 然后每个unique的character要有k distance apart.

跟Task Scheduler有点像, 只不过Task那道题里面还可以用其他方法求count, 这道题要求出排列结果

#### PriorityQueue + HashTable
- PriorityQueue排序+分布排列的一个经典用法.
- Count frequency and store in pq.
- Consume element of pq for k rounds, each time pick one element from queue.
- Exception: if k still has content but queue is consumed: cannot complete valid string, return "";
- space, O(n) extra space in sb, O(26) constant space with pq.
- time: O(n) to add all items



---

**64. [Valid Number.java](https://github.com/awangdev/LintCode/blob/master/Java/Valid%20Number.java)**      Level: Hard      Tags: [Enumeration, Math, String]
      
time: O(n)

分析edge case, 和各种情况, 然后判别是否是valid number

#### 情况总结
- 遇到 `.`, `e`, `+/-`, `int`的几种不同情况
- 分别遇到的顺序不同时候, 结果也不同.
- 这道题更多是分析情况, 然后把edge case enumerate出来, 算法的意义比较少.



---

**65. [Bricks Falling When Hit.java](https://github.com/awangdev/LintCode/blob/master/Java/Bricks%20Falling%20When%20Hit.java)**      Level: Hard      Tags: [Union Find]
      

给一个matrix of 1 and 0, `1` 代表brick. 连着ceiling的brick就不会drop. 给一串coordinate hits[][], 记录每次take down 1 brick 后, 会drop多少个.

#### UnionFind
- 1. 我们知道大部分的brick可能都是连着ceiling, 所以每次正向检查都traverse all and timeout
- 2. 能否用union, 把connect都装在一起, 然后drop brick的时候把连着的都drop掉? 难: 因为还是要check所有brick当下的status.
- 受其他人的解答启发, 由于是计算count,我们可以`反向考虑`: 
- 把hit-brick全部mark=2 (就当舍弃不算), 观察整个局面的最后一步, 先把所有还连着ceiling的brick算一下总数, 统计在unionFind的 全部统计在count[0] 里面. 
- 剩下的不连着ceiling的也就是一个个isolated island
- 做法: 把hit-brick 一个个加回去, 然后再做一次union, 看看最终连到ceiling的有多少个. 增加的count, 就是正向思考时 dropped brick 数量!

##### Union Find 变种
- 还是用数字index做union find, 但是把每一个index都+1, 右移一位, 而[0]留下来做特殊用途:
- 用union at 0来 统计总共的remain count of ceiling-connected bricks, where `x = 0`. 
- 如果在其他其他题目种, 条件可能就不是`x=0`, 但也可以用这个 union index = 0 来做一个root的统计
- 关键: 把最后一个hit brick加回去, 然后再重新union一下这个hit-brick周围: count增加的变化, 不就是缺少hit-brick时候掉下去的数量.


#### DFS (timeout)
- 考虑每个hit的四周, 全部traverse, 没有连着ceiling就全部: 
- 比如是 200 x 200 的 全部是1的matrix, 任何一次traverse都要到顶; 重复计算, 所以timeout
- 算法是没错, 但是不efficient.
- 想要减少重复计算, 但是又不能提前计算: grid在不断变化. 所以看能不能把连着ceiling的都group起来, 可以O(1)快速check?




---

**66. [Interval Sum II.java](https://github.com/awangdev/LintCode/blob/master/Java/Interval%20Sum%20II.java)**      Level: Hard      Tags: [Binary Search, Lint, Segment Tree]
      

SegmentTree大集合. Methods: `build, query, modify`. 不难。只是要都记得不犯错.

#### Segment Tree
- build: recursively build children based on index-mid and link to curr node
- query: recursively try to find `node.start == targetStart && node.end == targetEnd`. Compare with node.mid
- modify: recursively try to find `node.start == targetStart && node.end == targetEnd`; modify and recursively assign upper interval with updated interval property.



---

**67. [HashHeap.java](https://github.com/awangdev/LintCode/blob/master/Java/HashHeap.java)**      Level: Hard      Tags: [HashHeap, Heap]
      

非题.是从九章找来的HashHeap implementation.



---

**68. [Trapping Rain Water II.java](https://github.com/awangdev/LintCode/blob/master/Java/Trapping%20Rain%20Water%20II.java)**      Level: Hard      Tags: [BFS, Heap, MinHeap, PriorityQueue]
      

给一个2Dmap, 每个position 有 height. 找Trapping water sum.


#### Min Heap
- 用PriorityQueue把选中的height排序,为走位, create class Cell (x,y, height).

##### 注意几个理论
- 1. 从matrix四周开始考虑，发现matrix能Hold住的水，取决于height低的block
- 2. 必须从外围开始考虑，因为水是被包裹在里面，外面至少需要现有一层
- 以上两点就促使我们用min-heap: 也就是natural order的PriorityQueue<Cell>.

##### Steps
- 1. process的时候，画个图也可以搞清楚: 就是四个方向都走走，用curr cell的高度减去周围cell的高度.
- 2. 若大于零，那么周围的cell就有积水: 因为cell已经是外围最低, 所以内部更低的, 一定有积水.
- 3. 每个visited的cell都要mark, avoid revisit
- 4. 根据4个方向的走位 `(mX, mY)` 创建新cell 加进queue里面: cell(mX, mY) 已经计算过积水后, 外围墙小时, `(mX, mY)`就会变成墙.
- 5. 因为做的是缩小一圈的新围墙, height = Math.max(cell.h, neighbor.h);
- 和trapping water I 想法一样。刚刚从外围，只是能加到跟外围cell高度一致的水平面。往里面，很可能cell高度变化。   
- 这里要附上curr cell 和 move-to cell的最大高度。

##### 为什么想到用Heap (min-heap - priorityQueue)
- 要找到bucket的最短板
- 每次需要最先处理最短的那条 (on top)

##### 为什么从外向里遍历
- 木桶理论, 包水, 是从外面包住里面
- 洋葱剥皮, 用完丢掉



---

**69. [Find Median from Data Stream.java](https://github.com/awangdev/LintCode/blob/master/Java/Find%20Median%20from%20Data%20Stream.java)**      Level: Hard      Tags: [Design, Heap, MaxHeap, MinHeap]
      

#### 原理
- 把Input stream想成向上的山坡. 山坡中间那点，自然就是median.
- 前半段，作为maxHeap,关注点是PriorityQueue的峰点，也就是实际上的median.   
- 后半段，作为minHeap,正常的PriorityQueue。 开头是最小的。

#### 注意
- 这里要首先定好, 哪一个queue是多存一个element的. 这里选maxHeap: maxHeap.size() == minHeap.size() + 1 || minHeap.size()
- 必须先维护maxHeap里面有个元素, 否则null了会在比较大小时出问题.



---

**70. [Sliding Window Median.java](https://github.com/awangdev/LintCode/blob/master/Java/Sliding%20Window%20Median.java)**      Level: Hard      Tags: [Design, Heap, MaxHeap, MinHeap, Sliding Window]
      

Data Stream Median 的同理题目: 不只是不断增加的Sequence, 而且要remove item (保持一个window size)

#### MaxHeap, MinHeap
- Median还是用min-heap 和 max-heap. Time(logN)
- 加/减: prioirtyQueue, log(n)
- findMedian: O(1)
- 加一个数, 减一个数。
- 加减时看好，是从前面的maxheap里面抽，还是从后面的minHeap里面抽。
- 抽完balance一下

#### 注意
- 用maxHeap, minHeap时候, 习惯选择让maxHeap多一个数字:
- 左边的maxHeap总有 x+1或者x个数字
- 后边minHeap应该一直有x个数字



---

**71. [Design Search Autocomplete System.java](https://github.com/awangdev/LintCode/blob/master/Java/Design%20Search%20Autocomplete%20System.java)**      Level: Hard      Tags: [Design, Hash Table, MinHeap, PriorityQueue, Trie]
      
time: input: O(x), where x = possible words, constructor: O(mn) m = max length, n = # of words
space: O(n^2), n = # of possible words, n = # of trie levels; mainlay saving the `Map<S, freq>`

Description is long, but in short: 做 search auto complete. 

Best problem to review Trie (prefix search), Top K frequent elements (Hash Map), and MinHeap (PriorityQueue)

Easier to revisit https://leetcode.com/problems/design-search-autocomplete-system/description/

#### 思考方向
- 做text的search, 毋庸置疑要用Prefix tree, trie.

##### Find all possible word/leaf, 两种方案:
- Trie造好之后, 做prefix search, 然后DFS/BFS return all leaf items. [high runtime complexity]
- 在TrieNode里面存所有的possible words. [high space usage]
- in memory space 应该不是大问题, 所以我们可以选择 store all possible words

##### Given k words, find top k frequent items. 肯定用MinHeap, 但也有两种方案:
- Store MinHeap with TrieNode: 因为会不断搜索新此条, 同样的prefix (尤其是在higher level), 会被多次搜索.
- [complexity: need to update heaps across all visited TrieNodes once new sentence is completed]
- Compute MinHeap on the fly: 当然我们不能每次都来一个DFS不然会很慢, 所以就必须要store list of possible candidates in TrieNode.
- 这里就用到了`Top K Frequent Words` 里面的 `Map<String, freq>`, 这样O(m) 构建 min-heap其实很方便.

##### Train the system
- 每次 `#` 后 标记一个词条被add进search history. 那么就要 `insert it into trie`.
- 这一条在最后遇到`#`再做就可以了, 非常简洁

#### Trie, PriorityQueue, HashMap
- Trie Prefix Search + maintain top k frequent items
- 



---

**72. [Integer to English Words.java](https://github.com/awangdev/LintCode/blob/master/Java/Integer%20to%20English%20Words.java)**      Level: Hard      Tags: [Enumeration, Math, String]
      

给一个小于 Integer.MAX_VALUE (2^31 - 1) 的数字, 转换成英语. (不需要加 'and')

#### String
- 基本implementation
- `分类讨论`: thounsand, million, billion.  `3个数字一格`.
- 用array枚举 token
- 运用 % 和 / 来找到每个分段的英语翻译
- 3-digit 的部分, 可以用一个helper funtion来找到结果, 每段的处理方法都是一样的

#### 注意
- StringBuffer 更有效率! `sb.insert(0, xxx)` append在sb前面
- 注意加 " " 的时候, 如果多余, 要`trim()`
- 注意, 小于20的数字, 有自己的特殊写法, 需要额外handle
- 这道题目就是要细致`耐心`, 几乎么有什么算法, 就是想要写的efficient并且正确, 需要很小心




---

**73. [Alien Dictionary.java](https://github.com/awangdev/LintCode/blob/master/Java/Alien%20Dictionary.java)**      Level: Hard      Tags: [BFS, Backtracking, DFS, Graph, Topological Sort]
      

给一个 array of strings: 假如这个array是按照一个新的字母排序表(alien dictionary)排出来的, 需要找到这个字母排序.

有可能有多重排序的方法, 给出一种就可以.

#### Graph
- 本质: 上下两行string, 相对应的相同的index上, 如果字母不同, 就说明排在第一行的字母在字母表里更领先
- 把 string array 变成topological sort的 graph: `map<char, list<char>>`
- 也可以`List[26] edges` (Course Schedule problem)
- Build edges: find char diff between two row, and store the order indication into graph
- 注意: indegree 永远是反向的 (跟 node to neighbors 相反的方式建立)

#### BFS
- topological sort 本身很好写, 但是要在题目中先了解到字母排序的本质
- 其实上面这个排序的本质很好想, 但是把它具体化成构建graph的代码, 会稍微有点难想到
- 算indegree, 然后用 BFS 来找到那些 inDegree == 0的 node
- 最先inDegree == 0的node, 就排在字母表前面.
- 下面的解法, 用了Graph: map<Character, List<Character>>, 而不是 List[26], 其实更加试用超过26个字母的dictionary.
- 如果 `inDegree.size() != result.length()`, there is nodes that did not make it into result. 
- ex: cycle nodes from input, where inDegree of a one node would never reduce to 0, and will not be added to result
- In this case, it will be treated as invalid input, and return ""

#### DFS
- 跟BFS建立 grpah 的过程一模一样
- DFS的不同在于: 用visited map 来标记走过的地方
- 走到leaf的时候, add to result: 但因为走到了底才add, 最终的顺序应该颠倒 (或者, sb.insert(0, x) 直接用颠倒的顺序add)



---

**74. [Word Ladder II.java](https://github.com/awangdev/LintCode/blob/master/Java/Word%20Ladder%20II.java)**      Level: Hard      Tags: [Array, BFS, Backtracking, DFS, Hash Table, String]
      

给一串string, start word, end word. 找到所有从 startWord -> endWord的最短路径list. 

变化方式: mutate 1 letter at a time.

#### BFS + Reverse Search
- 用BFS找最短路径.
- 问题: how to effectively store the path, if the number of paths are really large? 
- If we store Queue<List<String candidates>>: all possibilities will very large and not maintainable
- 用BFS做出一个反向structure, 然后再reverse search

##### BFS Prep Step
- BFS 找到所有start string 可以走到的地方 s, 放在一个overall structure里面: 注意, 存的方式 Map<s, list of sources>
- BFS时候每次都变化1step, 所以记录一次distance, 其实就是最短路径candidate (止步于此)
- 1. 反向mutation map: `destination/end string -> all source candidates` using queue: `Mutation Map`
- Mutation Map<s, List<possible src>>: list possible source strings to mutate into target key string.
- 2. 反向distance map: `destination/end string -> shortest distance to reach dest`
- Distance Map<s, possible/shortest distance>: shortest distance from to mutate into target key string.
- BFS prep step 并没解决问题, 甚至都没有用到end string. 我们要用BFS建成的反向mapping structure, 做search

##### Search using DFS
- 从结尾end string 开始扫, 找所有可以reach的candidate && only visit candidate that is 1 step away
- dfs 直到找到start string.

##### Bi-directional BFS: Search using BFS
- reversed structure 已经做好了, 现在做search 就可以: 也可以选用bfs.
- `Queue<List<String>>` to store candidates, searching from end-> start



---

**75. [Text Justification.java](https://github.com/awangdev/LintCode/blob/master/Java/Text%20Justification.java)**      Level: Hard      Tags: [Enumeration, String]
      

按照规则 adjust text. 就是Word里面: 有一行太长, adjust word 中间的space, 然后保证每一行的total width 顶格.

还有一些细节规则, 看原题

#### String
- Summing space = `width + (size-1)`. maintain: 1. list of candidates, 2. width of actual words
- calculate space in between: `remain/(size - 1)`
- overall for loop; clean up list: 1. over size; 2. last item
- 一点也不难, 但是要小心: deal with list of string的时候, 注意处理干净sum size of list<string>, 就行了.
- `干净处理space`: 只处理 (n-1) items, 然后最后一个拿到for loop 外面, 特殊处理.

#### Notes
- Clarification, observation:
- can start with greedy approach to stack as many words as possible
- once exceed the length, pop the top, and justify the added words (untouched words tracked by index)
- left justify: given list/stack of words with size t, overall remaining space length m, 
- deal with last line with special care: just fill one space, and fill the rest of the row with space
- Does not seem very complicated, but need additional care of calculating the amount of space needed.
- Overall runtime: O(n) to go over all space
- Overall space O(maxWidth) for maxWidth amount of strings



---

**76. [Read N Characters Given Read4 II - Call multiple times.java](https://github.com/awangdev/LintCode/blob/master/Java/Read%20N%20Characters%20Given%20Read4%20II%20-%20Call%20multiple%20times.java)**      Level: Hard      Tags: [Enumeration, String]
      

Read N Character using `Read4(char[] buf)` 的加强版: 可以不断读 read(buf, n)

#### String 
- 注意String的index handle, 慢慢写edge case
- 理解题目意思: `read4(char[] buf)` 这样的 `populate input object` 的function稍微少一点. 
- 遇到时候, 仔细理解function用法, 不要慌乱. 其实思考方式很简单, 仔细handle string 还有 edge case就好了.



---

**77. [Frog Jump.java](https://github.com/awangdev/LintCode/blob/master/Java/Frog%20Jump.java)**      Level: Hard      Tags: [DP, Hash Table]
      

Frog jump 的题目稍微需要理解: 每个格子可以 jump k-1, k, k+1 steps, 而k取决于上一步所跳的步数. 默认 0->1 一定是跳了1步.

注意: int[] stones 里面是stone所在的unit (不是可以跳的步数, 不要理解错).

#### DP
- 原本想按照corrdiante dp 来做, 但是发现很多问题, 需要track 不同的 possible previous starting spot.
- 根据jiuzhang答案: 按照定义, 用一个 map of <stone, Set<possible # steps to reach stone>>
- 每次在处理一个stone的时候, 都根据他自己的 set of <previous steps>, 来走下三步: k-1, k, or k+1 steps.
- 每次走一步, 查看 stone + step 是否存在; 如果存在, 就加进 next position: `stone+step`的 hash set 里面

##### 注意init
- `dp.put(stone, new HashSet<>())` mark 每个stone的存在
- `dp.get(0).add(0)` init condition, 用来做 dp.put(1, 1)

##### 思想
- 最终做下来思考模式, 更像是BFS的模式: starting from (0,0), add all possible ways 
- 然后again, try next stone with all possible future ways ... etc



---

**78. [Longest Substring with At Most Two Distinct Characters.java](https://github.com/awangdev/LintCode/blob/master/Java/Longest%20Substring%20with%20At%20Most%20Two%20Distinct%20Characters.java)**      Level: Hard      Tags: [Hash Table, Sliding Window, String, Two Pointers]
      

如题.

#### Two Pointer + HashMap
- 原本想用 DP, 但是其实用 sliding window 的思想
- sliding window 的切割: 用hashmap 存 last occurrance of char index; 
- map.remove(c) 之后, 就等于彻底切掉了那一段; 那么 map.get(c) + 1 也就是新的 left window border



---

**79. [Shortest Distance from All Buildings.java](https://github.com/awangdev/LintCode/blob/master/Java/Shortest%20Distance%20from%20All%20Buildings.java)**      Level: Hard      Tags: [BFS]
      

给Walls and Gates很像, 不同的是, 这道题要选一个 coordinate, having shortest sum distance to all buildings (marked as 1).

#### BFS
- BFS 可以 mark shortest distance from bulding -> any possible spot.
- Try each building (marked as 1) -> BFS cover all 0. 
- time: O(n^2) * # of building; use new visited[][] to mark visited for each building.
- O(n^2) find smallest point/aggregation value.
- 注意, 这道题我们update grid[][] sum up with shortest path value from building.
- 最后找个min value 就好了, 甚至不用return coordinate.
- 分析过, 还没有写.



---

**80. [Sliding Window Maximum.java](https://github.com/awangdev/LintCode/blob/master/Java/Sliding%20Window%20Maximum.java)**      Level: Hard      Tags: [Deque, Heap, Sliding Window]
      

#### Deque, Monotonous queue
- 维持monotonuous queue: one end is always at max and the other end is min. Always need to return the max end of queue.
- when adding new elements x: start from small-end of the queue, drop all smaller elements and append to first element larger than x.
- when sliding window: queue curr window 里面 最大的已经在max-end,  remove it if needed.
- 妙：用deque数据结构（实际上采用LinkedList的形式）来做一个`递减的queue`.
- 每次把小于当前node的，全部剔除，剩下的，自然就是:最大的>第二大的>第三大的...ETC.
- 我们只在乎最大值的存在；而任何小于当前（正要新就加进去的）值的，反正以后也成不了最大值，于是扔掉！



---

**81. [Median of Two Sorted Arrays.java](https://github.com/awangdev/LintCode/blob/master/Java/Median%20of%20Two%20Sorted%20Arrays.java)**      Level: Hard      Tags: [Array, Binary Search, DFS, Divide and Conquer]
      

著名的找两个sorted array的中位数. 中位数定义: 如果两个array总长为偶数, 取平均值.
题目要求在 log(m + n) 时间内解决

- 看到log(m+n), 就想到binary search, 或者是recursive 每次砍一半
- 两个sorted array 参差不齐, 肯定不能做简单的binary search

#### Divide and Conquer, recursive
- 这里有个数学排除思想: 考虑A, B各自的中间点.
- 如果A[mid] < B[mid], 那么 A[0 ~ mid - 1] 就不在 median的range里面, 可以排除. divide/conquer就这么来的.
- 具体逻辑看代码, 大致意思就是: 每次都取比较A 和 B [x + k / 2 - 1] 的位置, 然后做range 排除法
- end cases: 
- 1. 如果我们发现dfs()里面A或者B的start index溢出了, 那么就是最简单的case: midian一定在另外那个array里面
- 2. 如果 k == 1: 就是找A/B 里面的1st item, 那么做个 `Math.max(A[startA], B[startB])` 就可以
- 总共的数字长度是 (m + n) 而且每次都有一般的内容被删除, 那么time就是 O(log(m + n))




---

**82. [Bus Routes.java](https://github.com/awangdev/LintCode/blob/master/Java/Bus%20Routes.java)**      Level: Hard      Tags: [BFS]
      



---

**83. [Sliding Puzzle.java](https://github.com/awangdev/LintCode/blob/master/Java/Sliding%20Puzzle.java)**      Level: Hard      Tags: [BFS, Graph]
      



---

**84. [Cracking the Safe.java](https://github.com/awangdev/LintCode/blob/master/Java/Cracking%20the%20Safe.java)**      Level: Hard      Tags: [DFS, Greedy, Math]
      

#### Greedy, Iterative
- For 2 passwords, the shortest situation is both passwords overlap for n-1 chars.
- We can use a window to cut out last (n-1) substring and append with new candidate char from [k-1 ~ 0]
- Track the newly formed string; if new, add the new char to overall result
- Note: this operation will run for k^n times: for all spots of [0 ~ n - 1] each spot tries all k values [k-1 ~ 0]
- Same concept as dfs

#### DFS
- Same concept: use window to cut out tail, and append with new candidate
- do this for k^n = Math.pow(k, n) times



---

**85. [Redundant Connection II.java](https://github.com/awangdev/LintCode/blob/master/Java/Redundant%20Connection%20II.java)**      Level: Hard      Tags: [DFS, Graph, Tree, Union Find]
      

#### Union Find
- 讨论3种情况
- http://www.cnblogs.com/grandyang/p/8445733.html



---

**86. [The Maze III.java](https://github.com/awangdev/LintCode/blob/master/Java/The%20Maze%20III.java)**      Level: Hard      Tags: [BFS, DFS, PriorityQueue]
      

#### BFS
- 跟 Maze I, II 类似, 用一个 Node[][] 来存每一个(x,y)的state.
- Different from traditional BFS(shortest path): `it terminates BFS when good solution exists (distance), but will finish all possible routes`
- 1. `Termination condition`: if we already have a good/better solution on nodeMap[x][y], no need to add a new one
- 2. Always cache the node if passed the test in step1
- 3. Always offer the moved position as a new node to queue (as long as it fits condition)
- 4. Finally the item at nodeMap[target.x][target.y] will have the best solution.



---

**87. [Regular Expression Matching.java](https://github.com/awangdev/LintCode/blob/master/Java/Regular%20Expression%20Matching.java)**      Level: Hard      Tags: [Backtracking, DP, Double Sequence DP, Sequence DP, String]
      

跟WildCard Matching 一样, 分清楚情况讨论 string p last char is '*' 还有并不是 '*'

这里的区别是, '*' 需要有一个preceding element, 那么:
- repeat 0 times
- repeat 1 times: need s[i-1] match with prior char p[i-2]



---

**88. [Wildcard Matching.java](https://github.com/awangdev/LintCode/blob/master/Java/Wildcard%20Matching.java)**      Level: Hard      Tags: [Backtracking, DP, Double Sequence DP, Greedy, Sequence DP, String]
      

Double sequence DP. 与regular expression 很像.

#### Double Sequence DP
- 分析字符 ?, * 所代表的真正意义, 然后写出表达式.
- 搞清楚initialization 的时候 dp[i][0] 应该always false. 当p为empty string, 无论如何都match不了 (除非s="" as well)
- 同时 dp[0][j]不一定是false. 比如s="",p="*" 就是一个matching.
- A. p[j] != '*'
    1. last index match => dp[i - 1][j - 1]
    2. last index == ?  => dp[i - 1][j - 1]
- B. p[j] == "*"
    1. * is empty => dp[i][j - 1]
    2. * match 1 or more chars => dp[i - 1][j]




---

**89. [Robot Room Cleaner.java](https://github.com/awangdev/LintCode/blob/master/Java/Robot%20Room%20Cleaner.java)**      Level: Hard      Tags: [Backtracking, DFS]
      

#### DFS
- Different from regular dfs to visit all, the robot move() function need to be called, backtrack needs to move() manually and backtracking path shold not be blocked by visited positions
- IMPORTANT: Mark on the way in using set, but `backtrack directly without re-check against set`
- Mark coordinate 'x@y'
- Backtrack: turn 2 times to revert, move 1 step, and turn 2 times to revert back.
- Direction has to be up, right, down, left.
- `int [] dx = {-1, 0, 1, 0};`, `int[] dy = {0, 1, 0, -1};`



---

**90. [Maximum Vacation Days.java](https://github.com/awangdev/LintCode/blob/master/Java/Maximum%20Vacation%20Days.java)**      Level: Hard      Tags: [DP]
      



---




 
 
 
## Review (5)
**0. [Maximum Subarray III.java](https://github.com/awangdev/LintCode/blob/master/Java/Maximum%20Subarray%20III.java)**      Level: Review      Tags: []
      


---

**1. [Valid Perfect Square.java](https://github.com/awangdev/LintCode/blob/master/Java/Valid%20Perfect%20Square.java)**      Level: Review      Tags: [Binary Search, Math]
      

Binary找sqrt. 基本 mid+1, mid-1 template.
注意: define index as long. 



---

**2. [Maximum Average Subarray II.java](https://github.com/awangdev/LintCode/blob/master/Java/Maximum%20Average%20Subarray%20II.java)**      Level: Review      Tags: [Array, Binary Search, PreSum]
      

给int[] nums 和 window min size k. window size可以大于K. 找最大的连续数列average value.

- Binary Search的思想, 用在所要找的这个 average sum 上面. 大小是在[min, max]之中
- 找k的时候, 是>=k都可以, 巧用一个 min(preSum)的概念.
- 找k的时候, 画图, 可以看出来, 其实要的是 k window 里面的sum [x, i], 所以要用 sum[0, i] - sum[0, x]

需要仔细去读下面的notes.



---

**3. [The Skyline Problem.java](https://github.com/awangdev/LintCode/blob/master/Java/The%20Skyline%20Problem.java)**      Level: Review      Tags: [Binary Indexed Tree, Divide and Conquer, Heap, PriorityQueue, Segment Tree, Sweep Line]
      

又叫做skyline. 用Sweep Line做的O(nLogN), 但是貌似还有很多做法: segement tree, hashheap, treeSet?

#### Sweep Line, Time O(nLogN), Space O(n)
- original reference http://codechen.blogspot.com/2015/06/leetcode-skyline-problem.html?_sm_au_=isVmHvFmFs40TWRt
- 画图分析: 需要找到 non-overlaping height point at current index; also height needs to be different than prev height peek to be visible.
- 把所有点分出来， 每个点有index x, 再加上一个height.         
- 在这个list上排序，根据index和height. 注意用负数标记building start point height, 这样保证start在end 之前
- 用负数的height标记start: 在priority queue里面同一个x-pos比较 startPoint.height, endPoint.height 的时候, 因为end height是整数, 所以compare时会自动把start point放在end point前面
- 当然了, 如果两个 start point比较, 第二个point的负数超大的话(也就是height很高), 就会顺理compare return正数, 成章形成倒位
- 在processs时候用max-heap (reversed priorityqueue)，再iterate heightPoints 来存最大的height . 遇到peek,就是一个合理的解    
- heightQueue里面加一个0, 用来在结尾的时候做closure

#### Segment Tree
- 看了一些做法, segment tree写法很复杂, 估计在面试中难以用segment tree来写: https://www.cnblogs.com/tiezhibieek/p/5021202.html

#### HashHeap
- HashHeap template 可以考虑: https://www.jiuzhang.com/solution/building-outline/#tag-highlight-lang-java

Binary Indexed Tree?





---

**4. [Remove Invalid Parentheses.java](https://github.com/awangdev/LintCode/blob/master/Java/Remove%20Invalid%20Parentheses.java)**      Level: Review      Tags: [BFS, DFS, DP]
      

给一个string, 里面有括号和其他字符. 以最少刀 剪出 valid string, 求所有这样的string.

这个题目有多种解法, 最强就是O(n) space and time

#### DFS and reduce input string
- in dfs: remove the incorrect parentheses one at a time
- detect the incorrect parentheses by tracking/counting (similar to validation of the parentheses string): `if(count<0)`
- once detected, remove the char from middle of s, and dfs on the rest of the s that has not been tested yet.

##### Core concept: reverse test
- `if a parenthese string is valid, the reverse of it should also be valid`
- Test s with open='(', close=')' first; **reverse s**, and test it with open=')', close='('

##### Minor details
- only procceed to remove invalid parenthese when `count<0`, and also break && return dfs after the recursive calls.
- The above 2 facts eliminates all the redundant results.
- Reverse string before alternating open and close parentheses, so when returning final result, it will return the correct order.
- Open questions: how does it guarantee minimum removals?

##### Backtracking
- 如果用stringbuffer, 那么久不会每次create new string, 但是需要maintain这个string buffer, 就会backtracking

##### Complexity
- Seems to be O(n), but need to derive

#### BFS
TODO

#### DP



---




