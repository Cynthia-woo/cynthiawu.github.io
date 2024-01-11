## **代码随想录算法训练营第六十天|84.柱状图中最大的矩形**
<hr/>

**LeetCode84.柱状图中最大的矩形**

[84. Largest Rectangle in Histogram](https://leetcode.cn/problems/largest-rectangle-in-histogram/description/)

- 单调递减栈：类似于42接雨水
    - 找一个元素两个方向上的第一个小于它的值
    - 扩容heights：前后都加0，避免[1]或者[2,4,6,8]遇不到小于它的值时候的max不存在
    - 加入栈时判断大于/等于/小于
    - while持续比较i小于栈口元素
    - 栈口元素更新