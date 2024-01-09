## **代码随想录算法训练营第五十六天| 583. 两个字符串的删除操作，72. 编辑距离，编辑距离总结篇**
<hr/>

**LeetCode583. 两个字符串的删除操作**

[392. Is Subsequence](https://leetcode.cn/problems/is-subsequence/description/)

- 1.dp数组中存储word1和word2最长相同子序列的长度
- 2.dp数组中存储最小删除数，注意初始化不是只有0和1

<hr/>

**LeetCode72. 编辑距离**

[72. Edit Distance](https://leetcode.cn/problems/edit-distance/)

- dp数组中存储[0, i - 1]的word1变成[0, j - 1]的word2的增删替的个数
- 增：`dp[i - 1][j] + 1`
- 删：`dp[i][j - 1] + 1`
- 替：`dp[i - 1][j - 1] + 1`

<hr/>

**编辑距离总结篇**

- 递推公式！！！非常重要
- 初始化：定义的时候为了减少初始化，定义`dp[len1 + 1][len2 + 1]`
- 判断相等/加一/减一