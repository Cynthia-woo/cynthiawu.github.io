## **代码随想录算法训练营第二十二天| 235. 二叉搜索树的最近公共祖先，701.二叉搜索树中的插入操作，450.删除二叉搜索树中的节点**
<hr/>

**LeetCode235. 二叉搜索树的最近公共祖先**

[235. Lowest Common Ancestor of a Binary Search Tree](https://leetcode.cn/problems/lowest-common-ancestor-of-a-binary-search-tree/description/)

- 迭代法/递归法，判断是否result在中间

<hr/>

**LeetCode701.二叉搜索树中的插入操作**

[701. Insert into a Binary Search Tree](https://leetcode.cn/problems/insert-into-a-binary-search-tree/description/)

- 迭代法/递归法，判断val与左右子树之间的关系
- 判断叶子节点`while(curr.val == val)` `if (curr.val == null)`

<hr/>

**LeetCode450.删除二叉搜索树中的节点**

[450. Delete Node in a BST](https://leetcode.cn/problems/delete-node-in-a-bst/description/)

- 迭代法/递归法，需要考虑删除的各种情况
- 1.叶子节点，左右节点都为空
- 2.左不空右空
- 3.左空右不空
- 4.左不空右不空 -> 需要到迭代到叶子节点再赋值

