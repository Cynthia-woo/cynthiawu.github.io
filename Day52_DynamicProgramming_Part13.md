## **代码随想录算法训练营第五十二天| 300.最长递增子序列，674. 最长连续递增序列，718. 最长重复子数组**
<hr/>

**LeetCode300.最长递增子序列**

[300. Longest Increasing Subsequence](https://leetcode.cn/problems/longest-increasing-subsequence/description/)

- dp[i]的定义是i以前包括i的以nums[i]结尾的最长递增子序列的长度
- 一个比较： dp[i] > dp[j]
- 两个取最大值：以nums[i] 结尾的最长递增子序列的长度；所有nums[i]的递增子序列长度的最大值的

<hr/>

**LeetCode674. 最长连续递增序列**

[674. Longest Continuous Increasing Subsequence](https://leetcode.cn/problems/longest-continuous-increasing-subsequence/description/)

- dp[i]的定义是i以前包括i的以nums[i]结尾的最长连续递增子序列的长度
- dp法只有当前大于上一个才加1，其他都初始化到1
- 也可以用贪心法

<hr/>

**LeetCode718. 最长重复子数组**

[718. Maximum Length of Repeated Subarray](https://leetcode.cn/problems/maximum-length-of-repeated-subarray/description/)

- dp[i][j]的定义是以i - 1号元素结尾的nums1和以j - 1号元素结尾的nums2的重复子数组
- `int[][]dp = int[nums1.length][nums2.length]`减少初始化时的两层循环