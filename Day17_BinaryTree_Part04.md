## **代码随想录算法训练营第十七天| 110.平衡二叉树, 257. 二叉树的所有路径, 404.左叶子之和**
<hr/>

**LeetCode110.平衡二叉树**

[110. Balanced Binary Tree](https://leetcode.cn/problems/balanced-binary-tree/description/)

- 递归法：简单
- 1. 如果遇到左右两侧不相等的情况返回-1进行判断
- 2. 或者直接判断两侧是否相差小于1且左右都为true 双重迭代

<hr/>

**LeetCode257. 二叉树的所有路径**

[257. Binary Tree Paths](https://leetcode.cn/problems/binary-tree-paths/description/)

- 迭代法，用两个list分别储存`paths`和`List<String> result`

<hr/>

**LeetCode404.左叶子之和**

[404. Sum of Left Leaves](https://leetcode.cn/problems/sum-of-left-leaves/description/)

- 迭代法Iteration
- 递归法Recursion:考虑父元素的左子树的左右孩子为空，后序遍历

