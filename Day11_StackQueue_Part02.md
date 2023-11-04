## **代码随想录算法训练营第十一天| 20. 有效的括号, 1047. 删除字符串中的所有相邻重复项, 150. 逆波兰表达式求值**
<hr/>

**LeetCode 20. 有效的括号**

[20. Valid Parentheses](https://leetcode.cn/problems/valid-parentheses/description/)

- 三种情况：（反转）
- 左括号多于右括号
- 左括号少于右括号 
- 左括号和右括号不相同
- 剪枝：奇数肯定不对称

- 不反转直接配对比较法

<hr/>


**LeetCode 1047. 删除字符串中的所有相邻重复项**

[1047. Remove All Adjacent Duplicates In String](https://leetcode.cn/problems/remove-all-adjacent-duplicates-in-string/description/)

- 栈的方法
- StringBuilder：模拟栈的储存
- 快慢指针法

<hr/>

**LeetCode 150. 逆波兰表达式求值**

[150. Evaluate Reverse Polish Notation](https://leetcode.cn/problems/evaluate-reverse-polish-notation/description/)

- 逆波兰表达式：是一种后缀表达式，所谓后缀就是指运算符写在后面, ( ( 1 2 + ) ( 3 4 + ) * )
- 平常使用的算式则是一种中缀表达式，如 ( 1 + 2 ) * ( 3 + 4 )
- Deque法， LinkedList

<hr/>