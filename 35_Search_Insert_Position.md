# Question
Given a sorted array and a target value, return the index if the target is found. If not, return the index where it would be if it were inserted in order.

You may assume no duplicates in the array.

**Example:**

```
[1,3,5,6], 5 → 2
[1,3,5,6], 2 → 1
[1,3,5,6], 7 → 4
[1,3,5,6], 0 → 0
```

***题目的意思是***：给定一个从小到大排序的数组和一个目标值。若在该数组能找到目标值，则返回数组索引。 如果没有，则返回目标值按顺序插入数组的位置。

# My Solution

```java
    public class Solution {
    public int searchInsert(int[] nums, int target) {
        int index = Arrays.binarySearch(nums, target);
        if (index >= 0) {
            return index;
        }

        int targetIndex = 0;
        int low = 0;
        int high = nums.length - 1;

        while (low <= high) {
            int mid = (low + high) >>> 1;
            int midVal = nums[mid];


            if (midVal < target) {
                low = mid + 1;
                targetIndex = low;
            }
            else if (midVal > target) {
                high = mid - 1;
                targetIndex =  mid;
            }
        }

        return targetIndex;
    }
}
```
