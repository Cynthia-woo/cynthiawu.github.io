## **代码随想录算法训练营第十六天| 104.二叉树的最大深度, 559.n叉树的最大深度, 111.二叉树的最小深度, 222.完全二叉树的节点个数**
<hr/>

**LeetCode104.二叉树的最大深度**

[104. Maximum Depth of Binary Tree](https://leetcode.cn/problems/maximum-depth-of-binary-tree/description/)

- 迭代法Iteration/递归法Recursion（更好）

<hr/>

**LeetCode559.n叉树的最大深度**

[559. Maximum Depth of N-ary Tree](https://leetcode.cn/problems/maximum-depth-of-n-ary-tree/description/)

- 迭代法Iteration/递归法Recursion

<hr/>

**LeetCode111.二叉树的最小深度**

[111. Minimum Depth of Binary Tree](https://leetcode.cn/problems/minimum-depth-of-binary-tree/description/)

- 迭代法Iteration（更好）/递归法Recursion

<hr/>

**LeetCode222.完全二叉树的节点个数**

[222. Count Complete Tree Nodes](https://leetcode.cn/problems/count-complete-tree-nodes/description/)

- 迭代法Iteration/递归法Recursion（更好）
- 递归法用后序排列
- 可以利用完全二叉树的特性，判断左节点的最长深度是否等于右节点的最长深度，如果相等就是满二叉树

`2<<depth - 1`利用bit manipulation operation位操作

