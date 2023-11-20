## **代码随想录算法训练营第二十七天| 39. 组合总和, 40.组合总和II, 131.分割回文串**

**LeetCode39.组合总和**

[39. Combination Sum](https://leetcode.cn/problems/combination-sum/description/)

- 回溯，注意循环的开始

<hr/>

**LeetCode40.组合总和II**

[40. Combination Sum II](https://leetcode.cn/problems/combination-sum-ii/description/)

- 树层去重+树枝去重，`boolean[] used`
- 判断`used[i - 1] == 0`和`candidates[n] == candidates[n - 1];

<hr/>

**LeetCode131.分割回文串**

[131. Palindrome Partitioning](https://leetcode.cn/problems/palindrome-partitioning/description/)

- 回溯的为startIndex不重复，且用作判断是否为回文串的参数之一

