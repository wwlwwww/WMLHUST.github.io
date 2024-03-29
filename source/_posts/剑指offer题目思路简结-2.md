---
title: 剑指offer题目思路简结-2
tags: [leetcode]
categories: []
comments: true
date: 2020-06-22 21:43:53
updated: 2020-06-22 21:43:53
description: 剑指offer 24-50 题，思路简结
---

<!-- TOC -->

1. [剑指 Offer 26. 树的子结构](#剑指-offer-26-树的子结构)
2. [剑指 Offer 27. 二叉树的镜像](#剑指-offer-27-二叉树的镜像)
3. [剑指 Offer 28. 对称的二叉树](#剑指-offer-28-对称的二叉树)
4. [剑指 Offer 29. 顺时针打印矩阵](#剑指-offer-29-顺时针打印矩阵)
5. [剑指 Offer 30. 包含min函数的栈](#剑指-offer-30-包含min函数的栈)
6. [剑指 Offer 31. 栈的压入、弹出序列](#剑指-offer-31-栈的压入弹出序列)
7. [剑指 Offer 32 - I. 从上到下打印二叉树](#剑指-offer-32---i-从上到下打印二叉树)
8. [剑指 Offer 32 - II. 从上到下打印二叉树 II](#剑指-offer-32---ii-从上到下打印二叉树-ii)
9. [剑指 Offer 32 - III. 从上到下打印二叉树 III](#剑指-offer-32---iii-从上到下打印二叉树-iii)
10. [剑指 Offer 33. 二叉搜索树的后序遍历序列](#剑指-offer-33-二叉搜索树的后序遍历序列)
11. [剑指 Offer 34. 二叉树中和为某一值的路径](#剑指-offer-34-二叉树中和为某一值的路径)
12. [剑指 Offer 35. 复杂链表的复制](#剑指-offer-35-复杂链表的复制)
13. [剑指 Offer 36. 二叉搜索树与双向链表](#剑指-offer-36-二叉搜索树与双向链表)
14. [剑指 Offer 37. 序列化二叉树](#剑指-offer-37-序列化二叉树)
15. [剑指 Offer 38. 字符串的排列](#剑指-offer-38-字符串的排列)
16. [剑指 Offer 39. 数组中出现次数超过一半的数字](#剑指-offer-39-数组中出现次数超过一半的数字)
17. [剑指 Offer 40. 最小的k个数](#剑指-offer-40-最小的k个数)
18. [剑指 Offer 41. 数据流中的中位数](#剑指-offer-41-数据流中的中位数)
19. [剑指 Offer 42. 连续子数组的最大和](#剑指-offer-42-连续子数组的最大和)
20. [剑指 Offer 43. 1～n整数中1出现的次数](#剑指-offer-43-1n整数中1出现的次数)
21. [剑指 Offer 44. 数字序列中某一位的数字](#剑指-offer-44-数字序列中某一位的数字)
22. [剑指 Offer 45. 把数组排成最小的数](#剑指-offer-45-把数组排成最小的数)
23. [剑指 Offer 46. 把数字翻译成字符串](#剑指-offer-46-把数字翻译成字符串)
24. [剑指 Offer 47. 礼物的最大价值](#剑指-offer-47-礼物的最大价值)
25. [剑指 Offer 48. 最长不含重复字符的子字符串](#剑指-offer-48-最长不含重复字符的子字符串)
26. [剑指 Offer 49. 丑数](#剑指-offer-49-丑数)

<!-- /TOC -->

## 剑指 Offer 26. 树的子结构
DFS判断各个子树，是否满足子树条件即可。   
**树的结构，天生适合递归。**

## 剑指 Offer 27. 二叉树的镜像
递归交换左右子树的左右节点。

## 剑指 Offer 28. 对称的二叉树
递归判断左右子树的左右节点。

## 剑指 Offer 29. 顺时针打印矩阵
像洋葱一样，一层一层剥离打印。注意一些特殊情况，比如矩阵只有一行、一列的情况

## 剑指 Offer 30. 包含min函数的栈
关键在于min的复杂度要求O(1)。这里需要用一个单调递减的栈，辅助实现。   
**单调栈、单调队列在处理一些栈、队列最大值、最小值上很有用。**

## 剑指 Offer 31. 栈的压入、弹出序列
用一个栈去模拟压入、弹出过程，每当pop[0]==stack[-1]时，stack就弹出。   
如果模拟完后，stack里还有数，则说明序列不对。

## 剑指 Offer 32 - I. 从上到下打印二叉树
类似BFS，使用一个队列保存当前level的节点，之后依次遍历。   

## 剑指 Offer 32 - II. 从上到下打印二叉树 II
类似 [剑指 Offer 32 - I. 从上到下打印二叉树](#剑指-offer-32---i-从上到下打印二叉树)，每层的结果单独保存即可。

## 剑指 Offer 32 - III. 从上到下打印二叉树 III
类似 [剑指 Offer 32 - I. 从上到下打印二叉树](#剑指-offer-32---i-从上到下打印二叉树)，每层的结果单独保存即可。使用一个flag来判断顺序还是逆序。

## 剑指 Offer 33. 二叉搜索树的后序遍历序列
根据root节点，划分左右子树，递归判对即可。

## 剑指 Offer 34. 二叉树中和为某一值的路径
递归DFS

## 剑指 Offer 35. 复杂链表的复制
这题有意思，难得见到一个有意思的链表类的题。思路步骤：   
1. 复制：对每个节点都复制一个节点，并添加在其后面
2. 拆分：对复制后的链表进行拆分，由于已知每个节点后面跟的，都是其复制节点，因此只需将复制节点的指向，也指向对应节点的复制节点，即可。

## 剑指 Offer 36. 二叉搜索树与双向链表
对二叉搜索树模拟中序遍历，用一个指针记录遍历过程中的pre节点，最后将首尾相连，即可。

## 剑指 Offer 37. 序列化二叉树
这题标记为hard，但实际上应该只算得上middle。   
1. 序列化：类似层次遍历，与 [剑指 Offer 32 - I. 从上到下打印二叉树](#剑指-offer-32---i-从上到下打印二叉树) 相似。   
2. 反序列化：还是模拟层次遍历的过程

## 剑指 Offer 38. 字符串的排列
这种排列组合、枚举类题，都可以用回溯思想来解决。和DFS类似，其实DFS是回溯思想在树、图之类的特殊场景里的一种表现。同DFS，回溯的常见实现方式也是递归。   
**递归的时候，要小心大量的重复计算。（动态规划的递归实现中也存在）** 通常要进行剪枝操作。因此也和动态规划的实现类似，可以使用备忘录法，或自底向上法。自底向上法效率最高，因为常常可以用循环迭代方式实现，减少递归调用。
```python
class Solution:
    # 递归回溯，执行时间700ms
    def permutation1(self, s: str) -> List[str]:
        if len(s) == 0:
            return ['']

        res = set()
        for i in range(0, len(s)):
            child_res = self.permutation1(s[:i] + s[i + 1:])
            for v in child_res:
                res.add(s[i] + v)

        return list(res)

    # 备忘录，执行时间120ms
    def permutation2(self, s: str) -> List[str]:
        seen = {}
        def perm(s2):
            if len(s2) == 0:
                return ['']

            if s2 in seen:
                return seen[s2]

            # 递归过程不变
            res = set()
            for i in range(0, len(s2)):
                child_res = perm(s2[:i] + s2[i + 1:])
                for v in child_res:
                    res.add(s2[i:i + 1] + v)

            seen[s2] = list(res)
            return list(res)

        sorted_s = ''.join(sorted(s))
        return perm(sorted_s)

    # 自底向上，执行时间80ms
    def permutation3(self, s: str) -> List[str]:
        if len(s) == 0:
            return ['']

        res = set(s[0])
        for c in s[1:]:
            new_set = set()
            for item in res:
                for i in range(0, len(item)+1):
                    new_item = item[0:i] + c + item[i:]
                    new_set.add(new_item)
            res = new_set

        return list(res)

```

## 剑指 Offer 39. 数组中出现次数超过一半的数字
遍历一遍数组，记录一个数x，及其出现次数，遇见相同的数，次数加一，遇见不同的数，次数减一。如果次数减到0，则x=新的数。遍历完成后，x即为次数超过一半的数字。

## 剑指 Offer 40. 最小的k个数
经典题目，两种解法：
1. 利用容量为K的大顶堆，遍历一遍即可，比堆顶元素小的入堆，容量超过K时出堆
2. 利用快排的二分思路，每次可以排除一批不满足条件的数，从而快速缩小查找范围   

解法的关键思想在于，**找最小的k个数，但是这k个数互相是不必排序的，因此尽力减少这部分比较操作**。堆就减少了内部各个元素互相排序的操作。同样快排的二分思想，也可以一下子找到最大的m个数，m取决于所选的pivot。但是这m个数只需跟pivot比较，相互之间无需比较。

## 剑指 Offer 41. 数据流中的中位数
这个有点妙。   
1. 使用两个堆，一个使用小顶堆，保存较大的一半数字；一个使用大顶堆，保存较小的一半数字。同时保持两个堆的元素数量相对平衡 `0 <= (大堆-小堆) < 1`。此时两个堆的堆顶元素，就是数据流中间的两个数。
2. 在push时，将其和堆顶元素比较选一个堆加入。如果加入后，两个堆失去平衡，则进行调整
3. 取中位数时，根据两个堆元素数是否相等可知，一共有奇数或偶数个数字。从而根据堆顶元素，计算中位数。

## 剑指 Offer 42. 连续子数组的最大和
对于每一个元素，有两个选择，与前一个数字组成子数组，或重新开始计算子数组。   
记录遍历过程中的最大值。

## 剑指 Offer 43. 1～n整数中1出现的次数
按个位、十位、百位...考虑，比如：输入314，分析过程如下   
1. 个位4，>1，高位为31，受此影响，有 32 * 1 = 32 种可能
2. 十位1，=1，高位为3，低位为4，受此影响，有 3*10 + 5 = 35 种可能
3. 百位3，>1，高位为0，受此影响，有 1*100 = 100 种可能   

因此一共 32 + 35 + 100 = 167个。关键在于梳理清各种情况下1的个数。   
比如十位为1时，那么有01x/11x/21x，以及310~314，这么多种，也就是 3*10+5 = 35种。   
对于百位，当百位为1时，有1xx这么多种情况，所以就是 1 * 100种。

## 剑指 Offer 44. 数字序列中某一位的数字 
和 [剑指 Offer 43. 1～n整数中1出现的次数](#剑指-offer-43-1n整数中1出现的次数) 类似，关键在于找规律。可以发现:   
忽略0   
数字为1位的，从 1 开始，一共 9 个，1 - 9    
数字为2位的，从 10 开始，一共 90 个，10 - 99    
数字为3位的，从 100 开始，一共 900 个，100 - 999   
...   
依此可确定，第n位所在的区间，在取模可得到具体是哪个数字。大致思想如上，实现细节不再赘述。

## 剑指 Offer 45. 把数组排成最小的数
一个取巧的办法，对数组进行自定义排序，从小到大。对于a、b两数的比较规则是，如果ab>ba，则a>b，否则a<b。   

## 剑指 Offer 46. 把数字翻译成字符串
按动态规划的方式比较好理解：
1. 划分子问题：每一位数字，既可以单独表示一个字母，也可以与后面数字组合，共同表示一个字母，如果<26的话。
2. 状态转移公式：F(s) = F(s[1:]) + F(s[2:])
3. 边界条件：len(s)<=1时，F(s) = 1; 为什么 s 是空字符串时，F(s)也=1呢，s为空字符串，表示刚好划分完，仅此一种。比如12，F(12) = F(2) + F("")，F("")表示，12作为一个整体解释。

## 剑指 Offer 47. 礼物的最大价值
很基础的动态规划题：   
按动态规划的方式比较好理解：
1. 划分子问题：每一个格子可以分为，从上边格子和左边格子过来两种情况
2. 状态转移公式：dp[i][j] = max(dp[i-1][j]+grid[i][j], dp[i][j-1]+grid[i][j])
3. 边界条件：第一行和第一列，单独处理   

另外可以发现，dp[i][j]只和上一行有关，因此为了降低空间复杂度，可以只用一行空间即可。对 M*N 的格子，空间复杂度可以从 O(M * N) 降低至 O(M) 或 O(N)

## 剑指 Offer 48. 最长不含重复字符的子字符串
使用两个指针 i, j，分别表示起始和结束。同时记录、更新某字符上次出现的位置。   
如果 j 指向的当前字符，上次出现的位置 k > i，表示重复出现，则 i 更新为 k + 1。此时得到一个最长不重复子字符串，长度为 j-i。

## 剑指 Offer 49. 丑数
下一个丑数为，当前丑数序列 * 2、3、5，得到的丑数中，最小的那个。   
为了避免重复计算，可以使用三个数，分别记录上一个乘以2、3、5后，就大于最新丑数的位置。

```python
class Solution:
    def nthUglyNumber(self, n: int) -> int:
        if n == 1:
            return 1
        dp = [0] * n
        dp[0] = 1
        a, b, c = 0, 0, 0
        for i in range(1, n):
            # 计算下一个丑数
            aN, bN, cN = dp[a] * 2, dp[b] * 3, dp[c] * 5
            # 选最小的
            next = min(aN, bN, cN)
            dp[i] = next
            
            if next == aN:
                a += 1

            if next == bN:
                b += 1
            if next == cN:
                c += 1

        return dp[-1]
```





