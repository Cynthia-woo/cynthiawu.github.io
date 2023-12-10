## **代码随想录算法训练营第四十五天| 70. 爬楼梯 （进阶）, 322. 零钱兑换, 279.完全平方数**
<hr/>

**LeetCode70. 爬楼梯（进阶版）**

[70. 爬楼梯（进阶版）](https://kamacoder.com/problempage.php?pid=1067)

        import java.util.Scanner;
        class climbStairs{
            public static void main(String [] args){
                Scanner sc = new Scanner(System.in);
                int m, n;
                while (sc.hasNextInt()) {
                    // 从键盘输入参数，中间用空格隔开
                    n = sc.nextInt();
                    m = sc.nextInt();
        
                    // 求排列问题，先遍历背包再遍历物品
                    int[] dp = new int[n + 1];
                    dp[0] = 1;
                    for (int j = 1; j <= n; j++) {
                        for (int i = 1; i <= m; i++) {
                            if (j - i >= 0) dp[j] += dp[j - i];
                        }
                    }
                    System.out.println(dp[n]);
                }
            }
        }

<hr/>

**LeetCode322. 零钱兑换**

[518. Coin Change II](https://leetcode.cn/problems/coin-change-ii/description/)

- dp[j]：凑足总额为j所需钱币的最少个数为dp[j]
- 初始化0为0，其他为最大值
- 判断上一个是否为最大值，如果是，不能+1， 防止最大值+1 溢出成最小负数

<hr/>

**LeetCode279.完全平方数**

[279. Perfect Squares](https://leetcode.cn/problems/perfect-squares/description/)

- 组合和，先遍历背包和物体相同，注意边界条件 i * i <= n  
