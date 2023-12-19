## **代码随想录算法训练营第四十八天| 198.打家劫舍，213.打家劫舍II，337.打家劫舍III**
<hr/>

**LeetCode198.打家劫舍**

[198. House Robber](https://leetcode.cn/problems/house-robber/description/)

- 偷i和不偷i的最大的金币数量
- 初始化0和1

<hr/>

**LeetCode213.打家劫舍II**

[213. House Robber II](https://leetcode.cn/problems/house-robber-ii/description/)

- 提取打家劫舍的方法，判断不考虑首元素和不考虑尾元素两种情况的最大值
- 1. 提取subArray
- 2. 通过不用dp数组，用三个int代表前前一个，前一个和当前个

<hr/>

**LeetCode337.打家劫舍III**

[337. House Robber III](https://leetcode.cn/problems/house-robber-iii/description/)

- 树形dp数组
- 每个节点都有两个可能性，偷和不偷的最大价值的`int[] dp = new int[2]`
- 后序遍历，左右判断完向上推中间的最值