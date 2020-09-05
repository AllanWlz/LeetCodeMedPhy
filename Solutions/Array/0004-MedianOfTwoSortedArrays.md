# 寻找两个有序数组的中位数

## 题目
给定两个大小为 m 和 n 的有序数组 nums1 和 nums2。

请你找出这两个有序数组的中位数，并且要求算法的时间复杂度为 O(log(m + n))。

你可以假设 nums1 和 nums2 不会同时为空。

**示例 1:**
```
nums1 = [1, 3]
nums2 = [2]

则中位数是 2.0
```

**示例 2：**
```
nums1 = [1, 2]
nums2 = [3, 4]

则中位数是 (2 + 3)/2 = 2.5
```

## 解法
```js
```
## 思路
这一问题的思路：
1. 最开始容易考虑到的情况是使用暴力法，首先将两个数组进行合并成一个有序数组，之后求解中位数，然而此方法的时间复杂度为*O(m+n)*，显然不符合本题的要求；
2. 采用