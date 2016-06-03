# Question

Given two arrays, write a function to compute their intersection.

**Example:**
`Given nums1 = [1, 2, 2, 1], nums2 = [2, 2], return [2].`

### Note:

Each element in the result must be unique.
The result can be in any order.

# My Thought

题目意思：给定两个int数组，求两个数组的交集.使用了List，暂时想不到优化方案╮(╯▽╰)╭



# My Solution

```java



public int[] intersection(int[] nums1, int[] nums2) {

    List<Integer> list = new ArrayList();

    for (int i = 0; i < nums1.length; i++) {

        for (int j = 0; j < nums2.length; j++) {

            if (nums1[i] == nums2[j]) {

                if (!list.contains(nums1[i])) {

                    list.add(nums1[i]);

                }

                break;

            }

        }

    }



    int[] sol = new int[0];

    if (list != null && list.size() > 0) {

        sol = new int[list.size()];

        for (int i = 0; i < list.size(); i++) {

            sol[i] = list.get(i);

        }

    }

    return sol;

}

```
