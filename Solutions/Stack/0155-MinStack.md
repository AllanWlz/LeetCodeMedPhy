# 最小栈
By JC

## 题目
设计一个支持 push，pop，top 操作，并能在常数时间内检索到最小元素的栈。

- ``push(x)`` -- 将元素 x 推入栈中。
- ``pop()`` -- 删除栈顶的元素。
- ``top()`` -- 获取栈顶元素。
- ``getMin()`` -- 检索栈中的最小元素。

示例:
```
MinStack minStack = new MinStack();
minStack.push(-2);
minStack.push(0);
minStack.push(-3);
minStack.getMin();   // 返回 -3.
minStack.pop();
minStack.top();      // 返回 0.
minStack.getMin();   // 返回 -2.
```

## 解法代码
```js
/**
 * initialize your data structure here.
 */
let MinStack = function() {
    this.arr = [];
    this.minArr = [];
    this.minVal = Infinity;
};

/** 
 * @param {number} x
 * @return {void}
 */
MinStack.prototype.push = function(x) {
    if (x <= this.minVal) {
        this.minVal = x;
        this.minArr.push(this.minVal);
        this.arr.push(x);
    } else {
        this.arr.push(x);
    }
};

/**
 * @return {void}
 */
MinStack.prototype.pop = function() {
    let popVal = this.arr.pop();
    if (popVal === this.minArr[this.minArr.length - 1]) {
        this.minArr.pop();
        if (this.minArr.length) {
            this.minVal = this.minArr[this.minArr.length - 1];
        } else {
            // 需要考虑边界情况，当this.minArr清空的时候
            // this.minVal需要初始化为Infinity
            this.minVal = Infinity;
        }
    }
};

/**
 * @return {number}
 */
MinStack.prototype.top = function() {
    return this.arr[this.arr.length - 1];
};

/**
 * @return {number}
 */
MinStack.prototype.getMin = function() {
    return this.minArr[this.minArr.length - 1];
};
```

## 解题思路

最开始的思路是：

在栈的内部设置一个``minVal``变量，在每次``push(x)``操作的时候将``x``值和``minVal``值进行对比，当``x``更小时更新``minVal``值。

