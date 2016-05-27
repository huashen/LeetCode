# Question


Given an array of integers, return indices of the two numbers such that they add up to a specific target.

You may assume that each input would have exactly one solution.

**Example:**

`Given nums = [2, 7, 11, 15], target = 9,`

`Because nums[0] + nums[1] = 2 + 7 = 9,`

`return [0, 1].`

# My Thought

***题目的意思是***：给一个数组，有一堆数，然后再给一个数X，问你，在数组中哪个位置和哪个位置相加可以得到 这个数X。

# My Solution

```java
	public int[] twoSum(int[] nums, int target) {
			        for (int i = 0; i < nums.length - 1; i++) {
            for (int j = i + 1; j < nums.length; j++) {
                if ((nums[i] + nums[j]) == target) {
                    int sol[] = new int[2];
                    sol[0] = i;
                    sol[1] = j;
                    return sol;
                }
            }
        }
        return null;
	}
```

