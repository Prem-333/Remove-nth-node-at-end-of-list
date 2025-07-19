Description
Given the head of a linked list, remove the nth node from the end of the list and return its head.
Example 1:
Input: head = [1,2,3,4,5], n = 2
Output: [1,2,3,5]

Example 2:
Input: head = [1], n = 1
Output: []

Example 3:
Input: head = [1,2], n = 1
Output: [1]
 
Constraints:
The number of nodes in the list is sz.
1 <= sz <= 30
0 <= Node.val <= 100
1 <= n <= sz
 

Follow up: Could you do this in one pass?

Solutions
Solution 1: Fast and Slow Pointers
We define two pointers fast and slow, both initially pointing to the dummy head node of the linked list.

Next, the fast pointer moves forward 
n
 steps first, then fast and slow pointers move forward together until the fast pointer reaches the end of the linked list. At this point, the node pointed to by slow.next is the predecessor of the 
n
-th node from the end, and we can delete it.

The time complexity is 
O(n),where nis the length of the linked list. The space complexity is O(1).
