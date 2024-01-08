## **代码随想录算法训练营第五十五天| 392.判断子序列，115.不同的子序列**
<hr/>

**LeetCode392.判断子序列**

[392. Is Subsequence](https://leetcode.cn/problems/is-subsequence/description/)

- 双指针法
- 最长公共子序列的长度应该是s的长度 -> 求最长公共子序列
- dp[i][j] 表示[0, i-1]的s子字符串和[0, j-1]的t字符串的重复子序列的长度

<hr/>

**LeetCode115.不同的子序列**

[115. Distinct Subsequences](https://leetcode.cn/problems/distinct-subsequences/description/)

- dp[i][j] 表示[0, i-1]的s子字符串中包含[0, j-1]的t字符串的个数
- 在相同时，考虑计算当前s[i - 1]或者不计算s[i - 1]
- `dp[i][j] = dp[i - 1][j - 1]（考虑）+ dp[i - 1][j]（不考虑，j的变化是不是此时的是上次的）`