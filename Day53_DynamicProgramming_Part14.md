## **代码随想录算法训练营第五十三天| 1143.最长公共子序列，1035.不相交的线，53. 最大子序和  动态规划**
<hr/>

**LeetCode1143.最长公共子序列**

[1143. Longest Common Subsequence](https://leetcode.cn/problems/longest-common-subsequence/description/)

- dp[i][j]的定义是 [0, i-1] 的text1和 [0, j-1] 的text2的最长公共子序列的长度
- 相关性：左上，上，左
- 把string变为charArray，时间复杂度减小

<hr/>

**LeetCode1035.不相交的线**

[1035. Uncrossed Lines](https://leetcode.cn/problems/uncrossed-lines/description/)

- 同1143，求两个数组的最长公共子序列的长度

<hr/>

**LeetCode53. 最大子序和**

[3. Maximum Subarray](https://leetcode.cn/problems/maximum-subarray/description/)

- 贪心算法
- dp数组：为以nums[i]结尾的最大连续子序列的和
- 然后遍历dp求这个和的最大值