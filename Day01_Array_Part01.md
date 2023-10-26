## **代码随想录算法训练营第一天| 704. 二分查找、27. 移除元素**
<hr/>

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

**LeetCode35: 搜索插入位置**

[35. Search Insert Position](https://leetcode.cn/problems/search-insert-position/description/)

- 双指针法  -> 注意不存在时输出的index位置

<hr/>

**LeetCode34: 在排序数组中查找元素的第一个和最后一个位置**

[34. Find First and Last Position of Element in Sorted Array](https://leetcode.cn/problems/find-first-and-last-position-of-element-in-sorted-array/description/)

- 双指针法  -> 左右两侧分别遍历找到第一个是target的index
- 二分法  -> 找到target再向两侧拓展找到不是target的
- 左右分别采用二分法

// 左端点

        int findLeftBorder(int[] nums, int target) {
            int start = 0;
            int end = nums.length - 1;
            while (start <= end) {
                int mid = start + (end - start) / 2;
                if (nums[mid] < target) {
                    start = mid + 1;//[mid + 1, end]
                } else if (nums[mid] == target){// [start, mid]
                    if(mid == 0 || nums[mid - 1] < target){
                        return mid;
                    }
                    end = mid - 1;
                } else{// [start, mid - 1]
                    end = mid - 1;
                }
            }
            return -1;
        }

// 右端点

        int findRightBorder(int[] nums, int target) {
            int start = 0;
            int end = nums.length - 1;
            while (start <= end) {
                int mid = start + (end - start) / 2;
                // int mid = (start + end) >>> 1;// 取中间数行为改成向上取整
                if (nums[mid] < target) {
                    start = mid + 1;//[mid + 1, end]
                } else if (nums[mid] == target){
                    if (mid == nums.length - 1 || nums[mid + 1] > target){
                        return mid;
                    }
                    start = mid + 1;// [start, mid]
                } else{// nums[mid] > target
                    end = mid - 1;// [start, mid - 1]
                }
            }
            return -1;
        }

// 调用方式

        public int[] searchRange(int[] nums, int target) {
            if (nums.length == 0) {return new int[]{-1,-1};}
            int leftBorder = findLeftBorder(nums, target);
            int rightBorder = findRightBorder(nums, target);
            if (leftBorder == -1 || rightBorder == -1) {
                return new int[]{-1, -1};
            }
            if (rightBorder - leftBorder >= 0) {
                return new int[]{leftBorder, rightBorder};
            }
            return new int[]{-1, -1};
        } 


<hr/>

**LeetCode27: 移除元素**

[27. Remove Element](https://leetcode.cn/problems/remove-element/description/)

- 暴力解法：两个for循环
- 单向指针
- 双向指针 （number++; && ++number;） 一个for循环
<hr/>






