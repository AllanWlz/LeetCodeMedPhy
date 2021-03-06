# 合并两个有序数组

## 题目
给你两个有序整数数组 nums1 和 nums2，请你将 nums2 合并到 nums1 中，使 nums1 成为一个有序数组。

**说明**:

初始化 nums1 和 nums2 的元素数量分别为 m 和 n 。
你可以假设 nums1 有足够的空间（空间大小大于或等于 m + n）来保存 nums2 中的元素。

**示例**:
```
输入:
nums1 = [1,2,3,0,0,0], m = 3
nums2 = [2,5,6],       n = 3

输出: [1,2,2,3,5,6]
```

## 解法

## 思路
这道题目有很简单的求解方法：首先将 ``nums1`` 中的有效元素复制出来，生成新的数组 ``nums1_copy``，然后将 ``nums1_copy`` 和 ``nums2`` 合并到 ``nums1`` 中。然而这个算法的时间复杂度足够的低，但是空间复杂度却相对较高，需要 ``O(n)``。

换个思路，其实这道题可以从后到前面进行排序，
