## **代码随想录算法训练营第五十七天| 647. 回文子串，516.最长回文子序列，动态规划总结篇**
<hr/>

**LeetCode647. 回文子串**

[392. Is Subsequence](https://leetcode.cn/problems/is-subsequence/description/)

- dp表示[i,j]的子字符串是否为回文子串
- 注意根据递推公式推导方向

<hr/>

**LeetCode5. 最长回文子串**

[5. Longest Palindromic Substring](https://leetcode.cn/problems/longest-palindromic-substring/description/)

- 多参数记录最长回文子串的长度和边界

<hr/>

**LeetCode516.最长回文子序列**

[516. Longest Palindromic Subsequence](https://leetcode.cn/problems/longest-palindromic-subsequence/description/)

- dp表示[i,j]的最长回文子序列
- 如果相同：`dp[i + 1][j - 1] + 2`
- 如果不相同：包含左/包含右边界的最大值
