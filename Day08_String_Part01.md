## **代码随想录算法训练营第八天| 344.反转字符串, 541. 反转字符串II, 剑指Offer 05.替换空格, 151.翻转字符串里的单词, 剑指Offer58-II.左旋转字符串**
<hr/>

**LeetCode344：反转字符串**

[344. Reverse String](https://leetcode.cn/problems/reverse-string/description/)

- for loop/ while loop

两次异或交换

        s[l] ^= s[r];  //构造 a ^ b 的结果，并放在 a 中
        s[r] ^= s[l];  //将 a ^ b 这一结果再 ^ b ，存入b中，此时 b = a, a = a ^ b
        s[l] ^= s[r];  //a ^ b 的结果再 ^ a ，存入 a 中，此时 b = a, a = b 完成交换

<hr/>

**LeetCode541：反转字符串 II**

[541. Reverse String II](https://leetcode.cn/problems/reverse-string-ii/description/)

- 提取翻转字符串为一个函数方法，每个2k个反转前k个，如果尾数不够k个则全部反转，注意反转的包含不包含/尾数是否要-1

<hr/>

**LeetCode剑指offer 05：替换空格**

[LCR 122. 路径加密](https://leetcode.cn/problems/ti-huan-kong-ge-lcof/description/)

- 创建字符串法：StringBuilder的使用

        StringBuilder sb = new StringBuilder();
        sb.append(' ')//这里记住一定要用单引号 ' '，表示字符而不是" "表示String
        sb.append("Hello")

- 双指针法

        if (path.charAt(i) == '.') {
            str.append("  ");
        }

<hr/>

**LeetCode151: 反转字符串中的单词**

[151. Reverse Words in a String](https://leetcode.cn/problems/reverse-words-in-a-string/description/)

- 1.去除多余的空格 2.全部反转 3.反转单词
- toCharArray(不修改的时候使用这个) vs StringBuilder(修改时空间复杂度低)
 
<hr/>


**LeetCode剑指Offer58-II.左旋转字符串**

[LCR 182. 动态口令](https://leetcode.cn/problems/zuo-xuan-zhuan-zi-fu-chuan-lcof/description/)

- 直接用string的substring方法，记得左闭右开
- toCharArray/ StringBuilder target前后分别反转再一起反转

<hr/>

