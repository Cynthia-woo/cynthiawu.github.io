## **代码随想录算法训练营第四十九天| 123. 买卖股票的最佳时机III， 188.买卖股票的最佳时机IV **
<hr/>

**LeetCode123. 买卖股票的最佳时机III**

[123. Best Time to Buy and Sell Stock III](https://leetcode.cn/problems/best-time-to-buy-and-sell-stock-iii/description/)

- 五种状态：不持有，第一次买入，第一次卖出，第二次买入，第二次卖出
- 二维dp/一维dp数组（空间优化）

<hr/>

**LeetCode188.买卖股票的最佳时机IV**

[188. Best Time to Buy and Sell Stock IV](https://leetcode.cn/problems/best-time-to-buy-and-sell-stock-iv/description/)

- 用上一版的买卖2次变成买卖k次，考虑不持有，买1次，卖1次，买2次，卖2次....，买k次，卖k次
- 优化空间之后是`int[] dp = new int[2 * k]`
- 递推公式内部对于2k进行内循环找递推公式的规律