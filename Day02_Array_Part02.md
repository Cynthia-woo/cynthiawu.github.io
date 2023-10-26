## **代码随想录算法训练营第二天| 977.有序数组的平方 ，209.长度最小的子数组 ，59.螺旋矩阵II ，总结**
<hr/>

**LeetCode977: 有序数组的平方**

[977. Squares of a Sorted Array](https://leetcode.cn/problems/squares-of-a-sorted-array/description/)

- 暴力解法：Arrays.sort(arr);
- 双指针法：创建新的array，比较大的从右往左填，注意 k++, i--的使用

<hr/>


**LeetCode209: 长度最小的子数组**

[209. Minimum Size Subarray Sum](https://leetcode.cn/problems/minimum-size-subarray-sum/description/)

_滑动窗口问题_

- 暴力解法：两遍for循环，
    但当测试用例为target = 396893380;
                nums = [3571,9780,8138,1030,2959,6988,2983,9220,6800,7669,2528,3994,6090,311,5683,9232,9698,1784,6543,4018,1340,3170,5097,9876,8881,6303,7964,2469,1119,9259,9429,9355,9904,2971,6240,3973,4972,1874,7037,4631,4666,7809,...]; 时超出时间限制，不能使用
- 简化的暴力解法：单一for循环（终止位置）
    注意初始化sum/起始位置的时机


- 等同于C++中INT32_MAX -> JAVA中使用Integer.MAX_VALUE

<hr/>

**LeetCode59: 螺旋矩阵**

[59. Spiral Matrix II](https://leetcode.cn/problems/spiral-matrix-ii/description/)

- 循环内容： loop的定义，最中心的loop的完整性，最闭右闭

<hr/>

**总结篇**

数组：数组是存放在连续内存空间上的相同类型数据的集合

- 数组下标都是从0开始的。
- 数组内存空间的地址是连续的
- 数组的元素是不能删的，只能覆盖