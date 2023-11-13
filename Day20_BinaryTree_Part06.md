## **代码随想录算法训练营第二十天| 654.最大二叉树， 617.合并二叉树， 700.二叉搜索树中的搜索， 98.验证二叉搜索树**
<hr/>

**LeetCode654.最大二叉树**

[654. Maximum Binary Tree](https://leetcode.cn/problems/maximum-binary-tree/description/)

- sublist解法，冗余
- 不新建int[]，提供左右区间，然后动态滑动窗口

<hr/>

**LeetCode617.合并二叉树**

[617. Merge Two Binary Trees](https://leetcode.cn/problems/merge-two-binary-trees/description/)

- 递归：前序遍历 >> 考虑到非空的情况 
- 迭代：注意放入栈是相反顺序，left/right&&node1/node2

<hr/>

**LeetCode700.二叉搜索树中的搜索**

[700. Search in a Binary Search Tree](https://leetcode.cn/problems/search-in-a-binary-search-tree/description/)

- 递归Recursion
- 迭代Iteration

<hr/>

**LeetCode98.验证二叉搜索树**

[98. Validate Binary Search Tree](https://leetcode.cn/problems/validate-binary-search-tree/description/)

- 递归，需要注意：1. 中节点和左右两子树的所有元素对比，引入min/max 2. 不一定只是int，元素有可能是long类型 
- 自身递归，中序遍历。左中右
- 双指针递归/迭代


