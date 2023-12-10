## **代码随想录算法训练营第四十三天| 1049. 最后一块石头的重量 II, 494. 目标和, 474.一和零**
<hr/>

**LeetCode1049.最后一块石头的重量II**

[1049. Last Stone Weight II](https://leetcode.cn/problems/last-stone-weight-ii/description/)

- 求两堆的差值最小值，类似于上一题的等分：分割等和子集
- 求如果等分成两堆的最大价值，然后用sum-2*maxValue是最小差值

<hr/>

**LeetCode494.目标和**

[494. Target Sum](https://leetcode.cn/problems/target-sum/description/)

- 分成两部分，一部分是加法的元素，一部分是减法的元素
- 加法+减法 = sum
- 加法-减法 = target
- 初始化：容积为0的数组的方法为1
- 类似于爬楼梯法，递加

<hr/>

**LeetCode474.一和零**

[474. Ones and Zeroes](https://leetcode.cn/problems/ones-and-zeroes/description/)

- 相当于两个背包（容量为m和容量为n），三维数组压缩成二维dp数组
