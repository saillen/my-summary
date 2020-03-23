# LeetCode 每日一题 ：最大子序和

## 题目（easy）

给定一个整数数组 `nums` ，找到一个具有最大和的连续子数组（子数组最少包含一个元素），返回其最大和。

**示例:**

```
输入: [-2,1,-3,4,-1,2,1,-5,4],
输出: 6
解释: 连续子数组 [4,-1,2,1] 的和最大，为 6。
```

**进阶:**

如果你已经实现复杂度为 O(*n*) 的解法，尝试使用更为精妙的分治法求解。

## 分类

- 分类：动态规划、分治算法、贪心算法
- 难度：easy
- 细节：最终结果是输出子序列的和，不是子序列；

### 思路一：贪心算法  --  假设当前序列即为最优解逐步扩大到最后

- 算法设计：
  - 假设当前序列即为最优解，计算当序列值 `curSum` ；
  - 将下一个元素纳入到当前序列中，计算纳入后的值 `curSum + sum[i]` 和 前序 `curSum` 哪个更优秀；
  - 记录全局最优解 `maxSum` ，如果当前轮次解大于历史最优解则替换 `maxSum`；
- 算法实现：
  - 建立两个临时变量：`curSum` 和 `maxSum`
  - 选择起始解：`curSum` = `maxSum` = `nums[0]`
  - 建立循环以此扩大子问题 `for(int i = 0 ; i < nums.length)`
  - 扩大时的对比：`curSum = Math.max(nums[i],curSum + nums[i])`
- 时间复杂度 ：O(n)
- 空间复杂度：O(1)

#### 难点：

> `curSum = Math.max(nums[i],curSum + nums[i])` 寻找的是扩大后的序列和前序的最优解；
>
> 对于 [-2, 1, -3, 4, -1, 2, 1, -5, 4] 这个序列来说：
>
> - 起始解序列：[-2]；
> - 第一次扩大问题后序列：[1]
> - 第二次扩大问题后序列：[1,-3] 
> - 第三次扩大问题：[4] 

#### Java 答案

``````java
class Solution {
    public int maxSubArray(int[] nums) {
       int maxSum = nums[0], curSum = nums[0];
       int length = nums.length;
       for(int i = 1 ; i < length; i++){
           curSum = Math.max(nums[i],curSum + nums[i]);
           maxSum = Math.max(maxSum,curSum);
       }
       return maxSum;
    }
}
``````



## 思路二：