## **代码随想录算法训练营第六天| 哈希表理论基础, 242.有效的字母异位词, 349. 两个数组的交集, 202. 快乐数, 1. 两数之和**
<hr/>

**哈希表理论基础**

- 哈希表都是用来快速判断一个元素是否出现集合里
- 哈希函数 hash function: 
    index = hashFunction(name)
    hashFunction  = hashCode(name)%tableSize
- 哈希碰撞Collisions:两个元素映射到索引下标的位置
    拉链法：在1位置出现冲突，第二个元素链接到第一个元素上
    线性探测法：在1位置出现冲突，第二个元素链接到第一个元素下一位
- 哈希结构：数组array，集合set，映射map

<hr/>

**LeetCode242题.有效的字母异位词**

[242. Valid Anagram](https://leetcode.cn/problems/valid-anagram/)

- 计算26个字母出现的次数
- 0(n), 0(1)

<hr/>

**LeetCode第349题. 两个数组的交集**

[349. Intersection of Two Arrays](https://leetcode.cn/problems/intersection-of-two-arrays/description/)

- hashSet: 遍历一个数组，变成hashSet，遍历另一个，看这个hashSet有没有相同元素，若有，则加入新的hashSet
    hashSet转元素流再转int和转arr
    新的arr加入元素
- hash数组: 类似于242题，int[元素]++，再进行判断

<hr/>

**LeetCode第202题. 欢乐数**

[202. Happy Number](https://leetcode.cn/problems/happy-number/description/)

- 使用hashSet可以避免重复，而且运用哈希表处理未知量数据比较迅速合理

<hr/>

**LeetCode第1题. 两数之和**

[1. Two Sum](https://leetcode.cn/problems/two-sum/description/)

- hashMap kay-value，注意快速遍历的元素和储存在value中的分别是什么

<hr/>

