## **代码随想录算法训练营第三十四天| 1005.K次取反后最大化的数组和，134. 加油站，135. 分发糖果**
<hr/>

**LeetCode1005.K次取反后最大化的数组和**

[1005. Maximize Sum Of Array After K Negations](https://leetcode.cn/problems/maximize-sum-of-array-after-k-negations/description/)

- 第一次贪心算法：排序，处理负数最小值
- 第二次贪心算法：如果遍历完k还有剩的，判断奇偶，取反最小值

<hr/>

**LeetCode134. 加油站**

[134. Gas Station](https://leetcode.cn/problems/gas-station/description/)

- 贪心算法：如果剩余油量小于0，则起点重新计算，currSum重新计算
- 优化全局算法：1.sum < 0 return -1; 2. min >= 0 return 0; 3. return min(min)之后的index

<hr/>

**LeetCode135. 分发糖果**

[135. Candy](https://leetcode.cn/problems/candy/description/)

- 单向处理，从左往右判断右大于左
- 从右往左判断左大于右，取`Math.max(candys[i - 1], candys[i] + 1))`

