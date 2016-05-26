# Question

Write a function that takes a string as input and returns the string reversed.

**Example:**
`Given s = "hello", return "olleh".`

# My Thought

***题目的意思是***：反转字符串



# My Solution



```java

   public String reverseString(String s) {

        char[] ary = s.toCharArray();

        StringBuffer sb = new StringBuffer();

        for (int i = ary.length - 1; i >=0; i--) {

            sb.append(ary[i]);

        }

        return sb.toString();

}

```
