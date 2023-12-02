## **代码随想录算法训练营第三十八天| 理论基础, 509. 斐波那契数, 70. 爬楼梯, 746. 使用最小花费爬楼梯**
<hr/>

**动态规划理论基础**

---动规五部曲---
- dp数组，dp[i]的定义
- 递推公式
- dp数组的初始化
- 遍历顺序
- 打印dp数组：检查正确性

<hr/>

**LeetCode509. 斐波那契数**

[09. Fibonacci Number](https://leetcode.cn/problems/fibonacci-number/description/)

- dp数组保存之前的元素
- 状态压缩，只需要保留两层即可

<hr/>

**LeetCode70. 爬楼梯**

[70. Climbing Stairs](https://leetcode.cn/problems/climbing-stairs/description/)

- 类似于fibonacci

<hr/>

**LeetCode 746. 使用最小花费爬楼梯**

[70. Climbing Stairs](https://leetcode.cn/problems/climbing-stairs/description/)

- dp[i] -> 到达i位置的最小花费（分别考虑跳一步和跳两）