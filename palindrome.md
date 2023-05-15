# Question

Determine whether an integer is a palindrome. Do this without extra space

# My Thought

Palindrome指的是回文，而这里需要找的是回文数，指的是1、121、34543这样从左往右看和从右往左看都相等的数。


# My Solution

  ```java
public boolean isPalindrome(int x) {
        String s = x + "";
        char[] chars = s.toCharArray();
        StringBuilder reverseSb = new StringBuilder();
        for (int i = chars.length - 1; i >=0; i--) {
            reverseSb.append(chars[i]);
        }
        if (reverseSb.toString().equals(s)) {
            return true;
        } else {
            return false;
        }
    }
  ```
