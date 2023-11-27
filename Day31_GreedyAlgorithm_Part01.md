## **代码随想录算法训练营第三十一天| 理论基础, 455.分发饼干, 376. 摆动序列, 53. 最大子序和**

<hr/>

**理论基础**

- 本质：选择每一阶段的局部最优，从而达到全局最优
- 常识性推导加上举反例
- 解题步骤：
  - 将问题分解为若干个子问题
  - 找出适合的贪心策略
  - 求解每一个子问题的最优解
  - 将局部最优解堆叠成全局最优解

<hr/>

**LeetCode455.分发饼干**

[455. Assign Cookies](https://leetcode.cn/problems/assign-cookies/description/)

- 最大的饼干去依次投喂
- 先满足胃口最小的人

<hr/>

**LeetCode376. 摆动序列**

[376. Wiggle Subsequence](https://leetcode.cn/problems/wiggle-subsequence/description/)

- 摆动的定义：左侧>=,右侧< || 左侧<=, 右侧>
- 考虑首尾：首前为平坡，尾后默认有坡
- 考虑同坡度和平坡的情况

<hr/>

**LeetCode53. 最大子序和**

[53. Maximum Subarray](https://leetcode.cn/problems/maximum-subarray/description/)

- 连续和为负数，抛弃
- result赋值为最小负数，反例[-2, -1]