# Question
Reverse digits of an integer.

**Example:**

```
x = 123, return 321

x = -123, return -321

```
**Note**:The input is assumed to be a 32-bit signed integer. Your function should return 0 when the reversed integer overflows.

***题目的意思是***：反转数字。假定输入为32位有符号整数。 当反转的整数溢出时，你的函数应该返回0。

# My Solution

```java
public class Solution {
    public int reverse(int x) {
        long temp = Math.abs(x);
        long res = 0;
        while (temp > 0) {
            res = res * 10 + temp % 10;
            temp = temp / 10;
        }

        if (res > Integer.MAX_VALUE) {
            return 0;
        }
        return (int) (x > 0 ? res : -res);
    }
}
```