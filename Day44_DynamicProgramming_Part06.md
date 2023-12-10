## **代码随想录算法训练营第四十四天| 完全背包， 518. 零钱兑换 II， 377. 组合总和 Ⅳ**
<hr/>

**完全背包**

        public void bagProblem(int[] values, int[] weights, int bagSize) {
            int[] dp = new int[bagSize + 1];
            for (int i = 0; i < values.length; i++) {// 遍历物品
                for (int j = weight[i]; j < bagSize + 1; j++){// 遍历背包容量
                    dp[j] = Math.max(dp[j], dp[j - weight[i]] + values[i]);
                }
            }
            return dp[bagSize];
        }

<hr/>

**LeetCode518.零钱兑换 II**

[518. Coin Change II](https://leetcode.cn/problems/coin-change-ii/description/)

- 注意初始化值：dp[j] += dp[j - nums[i]]，如果 j - nums[i] == 0， dp[0] = 1;
- 先遍历物体再遍历背包

<hr/>

**LeetCode377.组合总和 Ⅳ**

[1049. Last Stone Weight II](https://leetcode.cn/problems/last-stone-weight-ii/description/)

- 类似于上一道题，但是1，2和2，1是不同的集合，排列问题：先遍历背包再遍历物体 
