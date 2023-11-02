## **代码随想录算法训练营第九天| 28. 实现 strStr(), 459.重复的子字符串, 字符串总结, 双指针回顾**
<hr/>

**LeetCode28. 实现 strStr()**

[28. Find the Index of the First Occurrence in a String](https://leetcode.cn/problems/find-the-index-of-the-first-occurrence-in-a-string/description/)

KMP算法 -- 好难

文本串&&模式串
- 前缀表：包含首字母但不包含尾字母的所有子串
- 后缀表：包含尾字母但不包含首字母的所有子串
- 最长相等前后缀：前后缀相同的个数的数组
- 匹配过程：遇到不匹配的一项，跳到最长相等前后缀的位置重新开始匹配
- prefix/next数组（最长相等前后缀的数组），遇到冲突的地方 next数组告诉我们要回退到哪里
- [参考视频](https://www.bilibili.com/video/BV1AY4y157yL/?spm_id_from=333.337.search-card.all.click&vd_source=5adf1beea08676da3812ff25c1e41f5f)


    class Solution {
        public int strStr(String haystack, String needle) {
            int h = 0;//文本串的指针位置
            int n = 0;//模式串的指针位置
            int[] next = new int[needle.length()];//创建next表
            getNext(next, needle);//获取next表
            while (h < haystack.length()) {//遍历文本串
                while (n > 0 && haystack.charAt(h) != needle.charAt(n)) {
                    n = next[n - 1];//字符串不相同，回溯到上一次的相同位置
                };
                if (haystack.charAt(h) == needle.charAt(n)) {//两个字符相同
                    if(n == needle.length() - 1){//模式串遍历完，说明存在子串
                        return h - n;
                    }
                    n++;//没遍历完，模式串指针向后移一位
                } 
                h++;
            }
            return -1;
            
        }
        public void getNext(int[] next, String needle) {
            //初始化
            int j = 0;
            next[0] = 0;
            //j为前缀表尾部，i为后缀表尾部
            int i = 1;
            //遍历模式串
            while(i < needle.length()) {
                while (j > 0 && needle.charAt(i) != needle.charAt(j)) {
                    //如果前缀表和后缀表尾部不同，则向前推导直到前后缀表尾部相同
                    j = next[j - 1];
                }
                if (needle.charAt(i) == needle.charAt(j)) {
                    //如果后缀表尾部和前缀表尾部相同，则前缀表和后缀表都加一
                    j++;
                }
                next[i] = j;
                i++;
            }
        }
    }

- 滑动窗口法：两次for循环，时间复杂度0(n^2)


    class Solution {
        public int strStr(String haystack, String needle) {
            int hLen = haystack.length();
            int nLen = needle.length();
            // shortcut
            if (nLen == 0){
                return 0;
            }  
            if (nLen > hLen) {
                return -1;
            }
            for (int i = 0; i < hLen - nLen + 1; i++) {
                if(haystack.charAt(i) != needle.charAt(0)){
                    continue;
                }
                for (int j = 0; j < nLen; j++) {
                    if (haystack.charAt(i + j) != needle.charAt(j)) {
                        break;
                    }
                    if (j == nLen - 1) {
                        return i;
                    }
                }
            }
            return -1;
        }
    }

<hr/>

**LeetCode459：重复的子字符串**

[459. Repeated Substring Pattern](https://leetcode.cn/problems/repeated-substring-pattern/description/)

- 移动匹配：删除首末尾，然后看是否包含
- KMP：字符串的长度-最长相等前后缀对应的子串为最小重复子串；如果长度整出最小重复子串的长度，则返回true

<hr/>

**字符串回顾**

- 字符串：若干字符组成的有限序列，也可以理解为一个字符数组
- 库函数
- 双指针法
- 反转：先整体反转再局部反转
- KMP：当字符串不匹配时，可以知道一部分之前已经匹配的文本内容，利用这些信息避免从头做匹配 ！！next数组的写法

<hr/>

**双指针总结**

- 数组：移除元素，只能覆盖不能移除，用两个指针在一个循环下完成两个指针的工作
- 字符串：反转、替换空格，冗余空格
- 链表：反转、移动、快慢指针
- n数之和：left/right比较和target的大小再移动

<hr/>