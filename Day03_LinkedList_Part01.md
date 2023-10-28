## **代码随想录算法训练营第三天| 链表基础，203.移除链表元素 ，707.设计链表， 206.反转链表**
<hr/>


**链表理论基础**
- 单链表：通过指针串联起来的线性结构，数据域+指针域，指针域指向下一个节点，最后一个指向null
- 双链表：一个指向前，一个指向后
- 循环链表：首尾相连

      class ListNode {
          int item;
          ListNode next;
          ListNode() {}
          ListNode(int item, ListNode next) {this.item = item; this.next = next;}
      }
<hr/>

**LeetCode203: 删除链表元素**

[203. Remove Linked List Elements](https://leetcode.cn/problems/remove-linked-list-elements/description/)

- 原链表删除元素;
- 创建虚拟头节点，在进行遍历，注意空指针问题 

<hr/>

**LeetCode707: 设计链表**

[707. Design Linked List](https://leetcode.cn/problems/design-linked-list/)

- 单向链表：o,null  通过极端值0判断边界;
- 双向链表，prev/next -> head/tail，需要两侧搭桥进行赋值，注意赋值的先后顺序；注意size为空的情况

先newNode后curr

        newNode.next = curr.next;
        curr.next.prev = newNode;
        newNode.prev = curr;
        curr.next = newNode;

<hr/>

**LeetCode206: 反转链表**

[206. Reverse Linked List](https://leetcode.cn/problems/reverse-linked-list/)

- 双指针法 分别指向前一个prev和curr，需要临时指针temp;
- 迭代/递归 ->基于双指针法提炼 

