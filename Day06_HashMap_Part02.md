## **代码随想录算法训练营第六天| 454.四数相加II, 383. 赎金信, 15. 三数之和, 18. 四数之和, 总结**
<hr/>

**LeetCode第454题.四数相加II**

[454. 4Sum II](https://leetcode.cn/problems/4sum-ii/description/)

- 暴力解法
- 通过两两分组降低时间复杂度，学会用hashMap储存值和值出现的次数，然后再寻找0 - 后两个元素的值

<hr/>

**LeetCode第383. 赎金信**

[454. 4Sum II](https://leetcode.cn/problems/4sum-ii/description/)

- hashMap
- 类似于242，有限的key可以用哈希映射数组，更加快、省空间

        magazine.toCharArray() //转化string转化为字符串数组

<hr/>

**LeetCode第15. 三数之和**

[15. 3Sum](https://leetcode.cn/problems/3sum/submissions/479062207/)

- 双指针法，排序，移动第二第三个元素，判断for中i和i-1的去重，判断left和right到下个循环之前去重

        Arrays.sort()；
        result.add(List.of(1,2,3)) //给列表中添加整数列表

<hr/>

**LeetCode第18. 四数之和**

[18. 4Sum](https://leetcode.cn/problems/4sum/description/)

- 15三数之和基础上增加一层loop
- 注意区分剪枝shortcut和去重i == i - 1的判断条件
- shortcut时注意只有target大于0/nums[i]>=0才可以使用shortcut

<hr/>

**哈希表总结**

- 数组：小写字母，已知数组长度，节约空间
- set：数组大小是有限的，受到系统栈空间影响。如果哈希值比较少、特别分散、跨度很大会造成空间的浪费
- map：同上，如果还需要保存其他信息，如下标、数值，使用map

<hr/>