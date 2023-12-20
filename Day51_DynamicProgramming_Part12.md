## **代码随想录算法训练营第五十一天| 309.最佳买卖股票时机含冷冻期, 714.买卖股票的最佳时机含手续费, 总结**
<hr/>

**LeetCode309.最佳买卖股票时机含冷冻期**

[309. Best Time to Buy and Sell Stock with Cooldown](https://leetcode.cn/problems/best-time-to-buy-and-sell-stock-with-cooldown/description/)

- 四种状态：不持有，买，卖，冷冻期
- 二维dp/一维dp数组（空间优化）
- 冷冻期只持续一天，之前是卖出，之后是买入/不持有

<hr/>

**LeetCode714.买卖股票的最佳时机含手续费**

[714. Best Time to Buy and Sell Stock with Transaction Fee](https://leetcode.cn/problems/best-time-to-buy-and-sell-stock-with-transaction-fee/description/)

- 在买卖的基础上加上了一次手续费，放在卖出的时候即可

<hr/>

**买卖股票总结篇**

- 买卖一次
- 买卖多次
- 最多买卖2次
- 最多买卖k次
- 冷冻期
- 手续费

- 考虑各个状态，推导递推公式
- dp数组初始化
- 二维dp数组空间优化成一维dp数组