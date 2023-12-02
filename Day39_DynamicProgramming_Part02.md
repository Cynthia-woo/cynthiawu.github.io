## **代码随想录算法训练营第三十九天| 62.不同路径， 63. 不同路径 II**
<hr/>

**LeetCode62.不同路径**

[62. Unique Paths](https://leetcode.cn/problems/unique-paths/description/)

- 注意初始化每一行和每一列
- 初始化圆点：dp[i] 代表的是路径的数量

<hr/>

**LeetCode63. 不同路径 II**

[63. Unique Paths II](https://leetcode.cn/problems/unique-paths-ii/description/)

- 注意第一排和第一列的初始化，一旦遇到一个障碍物就不能往后动
- stl容器中有默认初始化值 比如int[][]默认初始化值为0

        //如果在起点或终点出现了障碍，直接返回0
        if (obstacleGrid[m - 1][n - 1] == 1 || obstacleGrid[0][0] == 1) {
            return 0;
        }

- 优化空间，一维数组，另一个在主循环遍历时判断