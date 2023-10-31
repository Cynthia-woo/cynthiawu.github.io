## **代码随想录算法训练营第五天| 哈希表理论基础, 242.有效的字母异位词, 349. 两个数组的交集, 202. 快乐数, 1. 两数之和**
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

**LeetCode242.有效的字母异位词**

[242. Valid Anagram](https://leetcode.cn/problems/valid-anagram/)

- 计算26个字母出现的次数
- 0(n), 0(1)

<hr/>

