## **代码随想录算法训练营第五十八天|503.下一个更大元素II, 42. 接雨水**
<hr/>

**LeetCode503.下一个更大元素II**

[503. Next Greater Element II](https://leetcode.cn/problems/next-greater-element-ii/description/)

- 单调递增栈
- 用取模的方式来避免重新建一个双倍长度的数组

<hr/>

**LeetCode42. 接雨水**

[42. Trapping Rain Water](https://leetcode.cn/problems/trapping-rain-water/description/)

- 暴力解法
- 双指针法：纵向获得水量
- 单调递增栈：横向获得水量
  - 加入栈时判断大于/等于/小于
  - while比较是否为空栈&&栈口元素小于当前i最大
  - while中时刻更新栈口元素为pop mid后的新的栈口元素进行while的比较