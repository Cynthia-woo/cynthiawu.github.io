## **代码随想录算法训练营第十四天| 理论基础, 递归遍历, 迭代遍历, 统一迭代**
<hr/>

**理论基础**

- 种类：满二叉树（2k - 1）和完全二叉树(1 ~ 2k - 1)
- 堆就是一颗完全二叉树


- 二叉搜索树：有数值，有序树
- 平衡二叉搜索树：空树/左右两个子树的高度差绝对值不超过1（map, multimap, set, multiset）


- 储存方法：链式/顺序


- **遍历方式：**
1. 深度优先遍历: 先往深走，遇到叶子节点再往回走
- 前序遍历（递归法，迭代法）
- 中序遍历（递归法，迭代法）
- 后序遍历（递归法，迭代法）
2. 广度优先遍历: 一层一层的去遍历
- 层次遍历（迭代法） 

**二叉树的定义**

        public class TreeNode {
            int val;
            TreeNode left;
            TreeNode right;
            TreeNode() {}
            TreeNode(int val, TreeNode left, TreeNode right) {
                this.val = val;
                this.left = left;
                this.right = right;
            }
        }

<hr/>

**二叉树的递归遍历Recursion**
递归算法三要素：
1. 递归函数的参数和返回值
2. 确定终止条件
3. 确定单层递归逻辑

[144. Binary Tree Preorder Traversal](https://leetcode.cn/problems/binary-tree-preorder-traversal/description/)

[145. Binary Tree Postorder Traversal](https://leetcode.cn/problems/binary-tree-postorder-traversal/description/)

[94. Binary Tree Inorder Traversal](https://leetcode.cn/problems/binary-tree-inorder-traversal/description/)

<hr/>

**二叉树的迭代遍历Iteration**
- 前序：中左右
- 后序：左右中
- 中序：左中右

- 前序和后序是标准方法，中间先入stack先进result
- 中序需要考虑怎么让左侧先进，需要一个指针curr

**二叉树的统一迭代法**
- 无法同时访问（遍历节点）并处理节点，在需要处理节点的后面加上一个null空指针作为标记，如果遇到null，就说明结果可以处理



