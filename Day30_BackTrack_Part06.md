## **代码随想录算法训练营第三十天| 332.重新安排行程, 51. N皇后, 37. 解数独, 总结**
<hr/>

**LeetCode332.重新安排行程**

[332. Reconstruct Itinerary](https://leetcode.cn/problems/reconstruct-itinerary/description/)

- 难，后面再学 

<hr/>

**LeetCode51.N皇后**

[332. N Queens](https://leetcode.cn/problems/n-queens/description/)

- char[][]二维数组
- array char[][]转换为arraylist
- 检查row/col/45/135

<hr/>

**LeetCode37. 解数独**

[37.Sudoku Solver](https://leetcode.cn/problems/sudoku-solver/description/)

- 类似于n皇后，二维递归，2层for循环
- 检出row/col/小九宫格

<hr/>

**回溯法总结**

- 子集问题分析：

    - 时间复杂度：O(2^n)，因为每一个元素的状态无外乎取与不取，所以时间复杂度为O(2^n)
    - 空间复杂度：O(n)，递归深度为n，所以系统栈所用空间为O(n)，每一层递归所用的空间都是常数级别，注意代码里的result和path都是全局变量，就算是放在参数里，传的也是引用，并不会新申请内存空间，最终空间复杂度为O(n)

- 排列问题分析：

    - 时间复杂度：O(n!)，这个可以从排列的树形图中很明显发现，每一层节点为n，第二层每一个分支都延伸了n-1个分支，再往下又是n-2个分支，所以一直到叶子节点一共就是 n * n-1 * n-2 * ..... 1 = n!。
    - 空间复杂度：O(n)，和子集问题同理。

- 组合问题分析：

    - 时间复杂度：O(2^n)，组合问题其实就是一种子集的问题，所以组合问题最坏的情况，也不会超过子集问题的时间复杂度。 
    - 空间复杂度：O(n)，和子集问题同理。

- N皇后问题分析：

    - 时间复杂度：O(n!) ，其实如果看树形图的话，直觉上是O(n^n)，但皇后之间不能见面所以在搜索的过程中是有剪枝的，最差也就是O（n!），n!表示n * (n-1) * .... * 1。
    - 空间复杂度：O(n)，和子集问题同理。

- 解数独问题分析：

    - 时间复杂度：O(9^m) , m是'.'的数目。
    - 空间复杂度：O(n^2)，递归的深度是n^2