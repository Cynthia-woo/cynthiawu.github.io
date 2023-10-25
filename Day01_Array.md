## **代码随想录算法训练营第一天| 704. 二分查找、27. 移除元素**
**数组的理论基础**
<hr/>

**LeetCode704: 二分查找** 

[704. Binary Search](https://leetcode.cn/problems/binary-search/description/)
- 左闭右闭[ ] && 左闭右开 [  )
- startIndex&endIndex

// 左闭右闭 [ ]

        int start = 0;
        int end = nums.length - 1;
        int mid;
        while(start <= end) {
            mid = start + (end - start) / 2;
            if (nums[mid] > target) {
                end = mid - 1;
            } else if(nums[mid] < target) {
                start = mid + 1;
            } else{
                return mid;
            }
        }
        return -1;

// 左闭右开 [ )

        int start = 0;
        int end = nums.length;
        int mid;
        while(start < end) { 
            mid = start + (end - start)/2;
            if (nums[mid] > target) {
                end = mid;
            } else if(nums[mid] < target) {
                start = mid + 1;
            } else{
                return mid;
            }
        }
        return -1;


<hr/>

**LeetCode27: 移除元素**

[27. Remove Element](https://leetcode.cn/problems/remove-element/description/)

- 暴力解法：两个for循环
- 单向指针
- 双向指针 （number++; && ++number;）
<hr/>

**LeetCode977: 有序数组的平方**

[977. Squares of a Sorted Array](https://leetcode.cn/problems/squares-of-a-sorted-array/description/)

- 暴力解法：Arrays.sort(arr);
- 双指针法：创建新的array，比较大的从右往左填

