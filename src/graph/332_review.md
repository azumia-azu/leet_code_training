# 332. Reconstruct Itinerary
根据题意,该图有多条的通路,我们使用深度优先搜索寻找该图的最后一个节点,即出度为0的节点.  
将该节点放入result的首端,并将该节点从其上一个节点的边表中剔除,此时倒数第二节点将会变为出度为0的节点,如此循环直至遍历完全图.

题目第二个要求为筛选出lexical order最小的通路,所以我们使用最小堆来维护边表.