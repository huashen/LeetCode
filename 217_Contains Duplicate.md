# Question
Given an array of integers, find if the array contains any duplicates. Your function should return true if any value appears at least twice in the array, and it should return false if every element is distinct.


***题目的意思是***：给定整数数组，查找数组是否包含任何重复项。 如果数组中的任何值至少出现两次，则函数应返回true，如果每个元素都不同，则返回false。

# My Solution

```java
public class Solution {
    public boolean containsDuplicate(int[] nums) {
        Set<Integer> set = new HashSet();
        for (int i = 0; i < nums.length;i++) {
            if (!set.add(nums[i])) {
                return true;
            }
        }
        return false;
    }
}
```