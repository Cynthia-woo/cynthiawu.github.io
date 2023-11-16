## **代码随想录算法训练营第十八天| 513.找树左下角的值, 112. 路径总和, 113.路径总和ii, 106.从中序与后序遍历序列构造二叉树 105.从前序与中序遍历序列构造二叉树**
<hr/>

**LeetCode513. 找树左下角的值**

[513. Find Bottom Left Tree Value](https://leetcode.cn/problems/find-bottom-left-tree-value/description/)

- Iteration：层序遍历到最后一层的第一个
- Recursion：比较左层的深度和当前深度再赋值，内部循环体可拆开看回溯的过程

<hr/>

**LeetCode112. 路径总和**

[112. Path Sum](https://leetcode.cn/problems/path-sum/description/)

- Recursion: 1. 类似于259二叉树的所有路径，左右中 2. 用count - root.val，然后再简化到自身递归

<hr/>

**LeetCode113. 路径总和ii**

[113. Path Sum II](https://leetcode.cn/problems/path-sum-ii/description/)

- Recursion: 类似于找path，要注意指向的list是地址，再存入resultList的时候要另外创建一个新的ArrayList

<hr/>

**LeetCode106.从中序与后序遍历序列构造二叉树**

[106. Construct Binary Tree from Inorder and Postorder Traversal](https://leetcode.cn/problems/construct-binary-tree-from-inorder-and-postorder-traversal/description/)

- Recursion: 注意开始和结束的值！！左闭右开

<hr/>

**LeetCode105.从前序与中序遍历序列构造二叉树**

[105. Construct Binary Tree from Preorder and Inorder Traversal](https://leetcode.cn/problems/construct-binary-tree-from-preorder-and-inorder-traversal/description/)

- 类似于上一题106，把后序遍历换成了前序遍历

