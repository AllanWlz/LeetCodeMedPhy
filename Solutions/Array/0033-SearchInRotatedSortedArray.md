# 搜索旋转排序数组

## 题目
假设按照升序排序的数组在预先未知的某个点上进行了旋转。

( 例如，数组 ``[0,1,2,4,5,6,7]`` 可能变为 ``[4,5,6,7,0,1,2]`` )。

搜索一个给定的目标值，如果数组中存在这个目标值，则返回它的索引，否则返回 ``-1`` 。

你可以假设数组中不存在重复的元素。

你的算法时间复杂度必须是 ``O(log n)`` 级别。

**示例 1：**
```
输入: nums = [4,5,6,7,0,1,2], target = 0
输出: 4
```
**示例 2：**
``
输入: nums = [4,5,6,7,0,1,2], target = 3
输出: -1
``

## 解法
```js

```
## 思路
这个问题很有意思，由于将时间复杂度限制在了 ``O(log(n))``，因此表明我们必须使用类似*二分法*这样的方法进行搜索，然而由于该有序数组事先通过每个点进行了旋转，因此常规二分法肯定无法适用。

我们换一个思路，我们将该旋转后的数组看作是一个首尾相连的环，再来看这个问题。

