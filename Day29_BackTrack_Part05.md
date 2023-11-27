## **代码随想录算法训练营第二十九天| 491.递增子序列, 46.全排列, 47.全排列 II**
<hr/>

**LeetCode491.递增子序列**

[491. Non-decreasing Subsequences](https://leetcode.cn/problems/non-decreasing-subsequences/description/)

- 注意判断是否大于处用continue而不是return
- hashmap树组放置的位置
- 或者用树组 `int[] used = new int[201]` [-100, 100]

<hr/>

**LeetCode46.全排列**

[46. Permutations](https://leetcode.cn/problems/permutations/description/)

- `boolean[] used` 代替 `startIndex` 的使用

<hr/>

**LeetCode47.全排列 II**

[47. Permutations II](https://leetcode.cn/problems/permutations-ii/description/)

- 类似于组合总和2，`if(i > 0 && nums[i] == nums[i - 1] && used[i - 1] == false) continue;`
