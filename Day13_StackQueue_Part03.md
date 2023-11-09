## **代码随想录算法训练营第十三天| 239. 滑动窗口最大值, 347.前 K 个高频元素, 总结**
<hr/>

**LeetCode239. 滑动窗口最大值**

[239. Sliding Window Maximum](https://leetcode.cn/problems/sliding-window-maximum/description/)

- 单调队列（判断两侧pop和push的值于临时的队列的关系，永远保持最大值在队列首端）

<hr/>

**LeetCode347. 前 K 个高频元素**

[347. Top K Frequent Elements](https://leetcode.cn/problems/top-k-frequent-elements/description/)

- map数组存放

        class Solution {
            public int[] topKFrequent(int[] nums, int k) {
                Map<Integer, Integer> map= new HashMap<>();
                for (int num : nums) {
                    map.put(num, map.getOrDefault(num, 0) + 1);
                }
                // 将 HashMap 中的条目存储到一个列表中
                List<Map.Entry<Integer, Integer>> list = new ArrayList<>(map.entrySet());
                // 对列表中的条目根据值进行排序
                // list.sort(Map.Entry.comparingByValue());
                // 根据Map.Entry的值进行降序排序
                list.sort((a, b) -> b.getValue() - a.getValue());

                int[] result = new int[k];
                // Iterator<Integer> iterator = map.keySet().iterator();
                // int count = 0;
                // while (iterator.hasNext() && count < k) {
                //     result[count] = iterator.next();
                //     count++;
                // }
                for (int i = 0; i < k; i++) {
                    result[i] = list.get(i).getKey();
                }
                return result;
            }
        }

- 二叉树，大顶堆和小顶堆
* Comparator接口说明:
* 返回负数，形参中第一个参数排在前面；返回正数，形参中第二个参数排在前面
* 对于队列：排在前面意味着往队头靠
* 对于堆（使用PriorityQueue实现）：从队头到队尾按从小到大排就是最小堆（小顶堆）; 从队头到队尾按从大到小排就是最大堆（大顶堆）--->队头元素相当于堆的根节点

1. 大顶堆：

        public int[] topKFrequent(int[] nums, int k) {
            Map<Integer,Integer> map = new HashMap<>();//key为数组元素值,val为对应出现次数
            for(int num:nums){
                map.put(num,map.getOrDefault(num,0)+1);
            }
            //在优先队列中存储二元组(num,cnt),cnt表示元素值num在数组中的出现次数
            //出现次数按从队头到队尾的顺序是从大到小排,出现次数最多的在队头(相当于大顶堆)
            PriorityQueue<int[]> pq = new PriorityQueue<>((pair1, pair2)->pair2[1]-pair1[1]);//先定义一种排序方式
            for(Map.Entry<Integer,Integer> entry:map.entrySet()){//大顶堆需要对所有元素进行排序
                pq.add(new int[]{entry.getKey(),entry.getValue()});
            }
            int[] ans = new int[k];
            for(int i=0;i<k;i++){//依次从队头弹出k个,就是出现频率前k高的元素
                ans[i] = pq.poll()[0];//pq.poll()弹出的是Map.Entry类型
            }
            return ans;
        }

2. 小顶堆：

        public int[] topKFrequent(int[] nums, int k) {
            Map<Integer,Integer> map = new HashMap<>();//key为数组元素值,val为对应出现次数
            for(int num:nums){
                map.put(num,map.getOrDefault(num,0)+1);
            }
            //在优先队列中存储二元组(num,cnt),cnt表示元素值num在数组中的出现次数
            //出现次数按从队头到队尾的顺序是从小到大排,出现次数最低的在队头(相当于小顶堆)
            PriorityQueue<int[]> pq = new PriorityQueue<>((pair1,pair2)->pair1[1]-pair2[1]);
            for(Map.Entry<Integer,Integer> entry:map.entrySet()){//小顶堆只需要维持k个元素有序
                if(pq.size()<k){//小顶堆元素个数小于k个时直接加
                    pq.add(new int[]{entry.getKey(),entry.getValue()});
                }else{
                    if(entry.getValue()>pq.peek()[1]){//当前元素出现次数大于小顶堆的根结点(这k个元素中出现次数最少的那个)
                        pq.poll();//弹出队头(小顶堆的根结点),即把堆里出现次数最少的那个删除,留下的就是出现次数多的了
                        pq.add(new int[]{entry.getKey(),entry.getValue()});
                    }
                }
            }
            int[] ans = new int[k];
            for(int i=k-1;i>=0;i--){//依次弹出小顶堆,先弹出的是堆的根,出现次数少,后面弹出的出现次数多
                ans[i] = pq.poll()[0];
            }
            return ans;
        }

<hr/>

**总结**


