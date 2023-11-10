## **代码随想录算法训练营第十五天| 层序遍历  10, 226.翻转二叉树, 101.对称二叉树 2**
<hr/>

**层序遍历**
- 迭代法，借助队列 `List<List<Integer>>` 和 `Queue<TreeNode>`(临时队列)
- 递归法，每层创建一个`ArrayList<Integer>`，如果左边有过，就不加新的，如果没有，创建新的数组，先搭建框架，再向内输入值
- 图论中的广度优先搜索

<hr/>

**LeetCode102.二叉树的层序遍历**

[102. Binary Tree Level Order Traversal](https://leetcode.cn/problems/binary-tree-level-order-traversal/description/)

- 迭代法Iteration/递归法Recursion

<hr/>

**LeetCode107.二叉树的层次遍历 II**

[102. Binary Tree Level Order Traversal II](https://leetcode.cn/problems/binary-tree-level-order-traversal-ii/description/)

- 迭代法Iteration: 利用链表可以进行 O(1) 头部插入, 这样最后答案不需要再反转
  `LinkedList<List<Integer>> ans = new LinkedList<>();`
  `ans.addFirst(innerList)`
- 递归法Recursion

<hr/>

**LeetCode199.二叉树的右视图**

[199. Binary Tree Right Side View](https://leetcode.cn/problems/binary-tree-right-side-view/description/)

- 迭代法Iteration
- 递归法Recursion：注意取右视图先放右侧元素

<hr/>

**LeetCode637.二叉树的层平均值**

[637. Average of Levels in Binary Tree](https://leetcode.cn/problems/average-of-levels-in-binary-tree/description/)

- 迭代法Iteration/递归法Recursion

<hr/>

**LeetCode429.N叉树的层序遍历**

[429. N-ary Tree Level Order Traversal](https://leetcode.cn/problems/n-ary-tree-level-order-traversal/description/)

- 迭代法Iteration/递归法Recursion

<hr/>

**LeetCode515.在每个树行中找最大值**

[515. Find Largest Value in Each Tree Row](https://leetcode.cn/problems/find-largest-value-in-each-tree-row/description/)

- 迭代法Iteration 在int类型寻找最小值： `int maxNUM = Integer.MIN_VALUE`
- 递归法Recursion

<hr/>

**LeetCode116.填充每个节点的下一个右侧节点指针**

[116. Populating Next Right Pointers in Each Node](https://leetcode.cn/problems/populating-next-right-pointers-in-each-node/description/)

- 迭代法Iteration：上一个指向现在
- 递归法Recursion：`ArrayList<Node>`注意pre与curr之间的关系

<hr/>

**LeetCode117.填充每个节点的下一个右侧节点指针II**

[117. Populating Next Right Pointers in Each Node II](https://leetcode.cn/problems/populating-next-right-pointers-in-each-node-ii/description/)

- 迭代法Iteration：上一个指向现在
- 递归法Recursion：`ArrayList<Node>`注意pre与curr之间的关系

<hr/>

**LeetCode104.二叉树的最大深度**

[104. Maximum Depth of Binary Tree](https://leetcode.cn/problems/maximum-depth-of-binary-tree/description/)

- 迭代法Iteration/递归法Recursion（更好）

<hr/>

**LeetCode111.二叉树的最小深度**

[111. Minimum Depth of Binary Tree](https://leetcode.cn/problems/minimum-depth-of-binary-tree/description/)

- 迭代法Iteration（更好）/递归法Recursion

<hr/>

**LeetCode226.翻转二叉树**

[226. Invert Binary Tree](https://leetcode.cn/problems/invert-binary-tree/description/)

- 前中后序
- 层序遍历

<hr/>

**LeetCode101. 对称二叉树**

[101. Symmetric Tree](https://leetcode.cn/problems/symmetric-tree/description/)

- 左边的左边和右边的右边相等
- 递归法+后序遍历
- 迭代法+队列Queue/双端队列Deque/栈Stack





