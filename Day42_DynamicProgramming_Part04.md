## **代码随想录算法训练营第四十二天| 01背包问题，你该了解这些！, 滚动数组, 416. 分割等和子集**
<hr/>

**0-1背包 二维dp数组**

- 判断比较不带i，带i：减去weight[i] + value[i]的最大值
- 递推公式：dp[i][j] = Math.max(dp[i - 1][j], dp[i - 1][j - weight[i]] + value[i])//放i和不放i取最大值

        const class BagProblem {
            public static void main (String[] args) {
                int[] weight = {1,3,4};
                int[] value = {15,20,30};
                int bagSize = 4;
                testWeightBagProblem(weight, value, bagSize);
            public static void testWeightBagProblem(int[] weight, int[] value, int bagSize) {
                int len = weight.length;
                int[][] dp = new int[len][bagSize + 1];
                for (int j = weight[0]; j <= bagSize; j++) {//初始化
                    dp[0][j] = value[0];
                }
                for (int i = 1; i < len; i++){
                    for (int j = 1; i <= bagSize; j++) {
                        if (j < weight[i]) {
                            dp[i][j] = dp[i - 1][j];
                        } else {
                            dp[i][j] = Math.max(dp[i - 1][j], dp[i - 1][j - weight[i]] + value[i]);
                        }
                    }
                }
                //print
                for (int i = 0; i < len; i++) {
                    for (int j = 0; j < bagSize + 1; j++) {
                        System.out.print(dp[i][j] + "\t");
                    }
                    System.out.print("\n")；
                }
            }
        }

<hr/>

**0-1背包问题 滚动数组：一维dp数组**

- 状态是可压缩的
- 递推公式：dp[j] = Math.max(dp[j], dp[j - weight[i]] + value[i]);

        const class BagProblem {
            public static void main (String[] args) {
                int[] weight = {1,3,4};
                int[] value = {15,20,30};
                int bagSize = 4;
                testWeightBagProblem(weight, value, bagSize);
            public static void testWeightBagProblem(int[] weight, int[] value, int bagSize) {
                int len = weight.length;
                int[] dp = new int[bagSize + 1];
                for (int j = weight[0]; j < bagSize + 1; j++) {
                    dp[j] = value[0];
                }
                for (int i = 1; i < len; i++) {
                    for (int j = bagSize; j >= weight[i] ; j--) {
                        dp[j] = Math.max(dp[j], dp[j - weight[i]] + value[i]);
                    }
                }
                //print
                for (int j = 0; j < bagSize + 1; j++) {
                    System.out.print(dp[j] + "\t");
                }
                System.out.println("\n");
            }
        }

**LeetCode416. 分割等和子集**

[416. Partition Equal Subset Sum](https://leetcode.cn/problems/partition-equal-subset-sum/description/)

- 获取总和，第一次剪枝sum
- dp[i][j]表示从数组的 [0, i] 这个子区间内挑选一些正整数；每个数只能用一次，使得这些数的和恰好等于 j。
- 如果某个物品单独的重量恰好就等于背包的重量，那么也是满足dp数组的定义的
- 如果某个物品的重量小于j，那就可以看该物品是否放入背包