## **代码随想录算法训练营第五十八天|739. 每日温度, 496.下一个更大元素 I**
<hr/>

**LeetCode739. 每日温度**

[739. Daily Temperatures](https://leetcode.cn/problems/daily-temperatures/description/)

- 单调递增栈，栈中存放元素的位置
- 只有遇到当前大于顶端时才获得大于顶端元素的第一个元素的位置
- Deque LinkedList比ArrayDeque的速率

<hr/>

**LeetCode496.下一个更大元素 I**

[496. Next Greater Element I](https://leetcode.cn/problems/next-greater-element-i/description/)

- 单调递增栈+一个map
- 遍历nums1的位置：之前（map先遍历nums1，如果map里有才对result赋值）或者之后（处理stack剩余元素为-1）