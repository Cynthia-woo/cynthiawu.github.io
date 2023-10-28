## **代码随想录算法训练营第四天| 24. 两两交换链表中的节点, 19.删除链表的倒数第N个节点, 面试题 02.07. 链表相交, 142.环形链表II, 总结**
<hr/>



**LeetCode24: 两两交换链表中的节点**

[24. Swap Nodes in Pairs](https://leetcode.cn/problems/swap-nodes-in-pairs/description/)

- 双指针法，while循环
- 迭代法： 注意放迭代的位置

        ListNode newNode = swapPairs(currNext.next);

<hr/>

**LeetCode19: 删除链表的第N个节点**

[19. Remove Nth Node From End of List](https://leetcode.cn/problems/remove-nth-node-from-end-of-list/description/)

- 快慢指针法-> 先让快指针走（n+1）步，在让快慢指针一起走到快指针走向null，慢指针指向倒数（n+1）步，是的slow.next = slow.next.next;

<hr/>

**LeetCode160/面试题02.07: 链表相交**

[面试题 02.07. Intersection of Two Linked Lists LCCI](https://leetcode.cn/problems/intersection-of-two-linked-lists-lcci/description/)

- 虚拟指针，获取链表长度，两链表等长，筛选（不要忘记获取长度之后的重新初始化）

<hr/>

**LeetCode142: 环形链表 II**

[142. Linked List Cycle II](https://leetcode.cn/problems/linked-list-cycle-ii/description/)

- fast先进环（a = 2）, slow后进环（a = 1）,若fast能追上slow，则为环形列表
- x = n * (y + z) - y; x = z; 下一次相遇的点就可以算出x的位置，记得画图进行分析！
- 初始判断是否为空

<hr/>



**链表总结**
- 分类：单链表、双链表、循环链表
- 存储方式：分散的、通过指针连在一起
- 功能：增删改查
