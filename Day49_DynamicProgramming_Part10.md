## **代码随想录算法训练营第四十九天| 121. 买卖股票的最佳时机， 122.买卖股票的最佳时机II **
<hr/>

**LeetCode121. 买卖股票的最佳时机**

[121. Best Time to Buy and Sell Stock](https://leetcode.cn/problems/best-time-to-buy-and-sell-stock/description/)

- 判断股票是否持有的两种状态
- 注意股票只买卖一次
- 只和前一次有关，所以可以简化成`int[2][2]`
- 再简化成一维dp数组，只判断持不持有两种状态，时刻更新

<hr/>

**LeetCode122.买卖股票的最佳时机II**

[122. Best Time to Buy and Sell Stock II](https://leetcode.cn/problems/best-time-to-buy-and-sell-stock-ii/description/)

- 类似于上一题，注意股票可以买卖多次，所以在判断持有的时候是累加状态
- 0表示持有，1表示卖出