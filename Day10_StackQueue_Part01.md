## **代码随想录算法训练营第十天| 理论基础，232. 用栈实现队列， 225. 用队列实现栈**
<hr/>

**理论基础**


**<hr/>**

**LeetCode 232.用栈实现队列**

[232. Implement Queue using Stacks](https://leetcode.cn/problems/implement-queue-using-stacks/description/)

- push(), pop(), empty(), peek()
- stackIn && stackOut, 两个栈

<hr/>

**LeetCode225. 用队列实现栈**

[225. Implement Stack using Queues](https://leetcode.cn/problems/implement-stack-using-queues/submissions/479584532/)

- 单队列，挤出的同时加入到最后的位置
- 双队列，Deque: ArrayList/ArrayDeque，另一个队列用来临时放置元素

        ArrayDeque: queue.add/poll/peekLast()/First();
        ArrayList: queue.add/poll/peak()

<hr/>