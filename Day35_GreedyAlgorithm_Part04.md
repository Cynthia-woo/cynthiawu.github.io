## **代码随想录算法训练营第三十五天| 860.柠檬水找零, 406.根据身高重建队列, 452. 用最少数量的箭引爆气球**
<hr/>

**LeetCode860.柠檬水找零**

[860. Lemonade Change](https://leetcode.cn/problems/lemonade-change/description/)

- 每次判断之前的charge够不够找零

<hr/>

**LeetCode406.根据身高重建队列**

[860. Lemonade Change](https://leetcode.cn/problems/lemonade-change/description/)

- 类似于分发糖果，两次排序，有限高度排序，再根据k排序
- LinkedList<int[]> que;

        Arrays.sort(people, (a, b) -> {
            if (a[0] == b[0]) return a[1] - b[1];   // a - b 是升序排列，故在a[0] == b[0]的狀況下，會根據k值升序排列
            return b[0] - a[0];   //b - a 是降序排列，在a[0] != b[0]，的狀況會根據h值降序排列
        });

<hr/>

**LeetCode452. 用最少数量的箭引爆气球**

[452. Minimum Number of Arrows to Burst Balloons](https://leetcode.cn/problems/minimum-number-of-arrows-to-burst-balloons/description/)

- 为了不溢出，采用Integer的内置比较方法
- 实时更新右边界

