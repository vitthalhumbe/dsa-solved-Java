# 1768. Merge Strings Alternately
You are given two strings word1 and word2. Merge the strings by adding letters in alternating order, starting with word1. If a string is longer than the other, append the additional letters onto the end of the merged string. Return the merged string.

 

### Example 1:

> Input: word1 = "abc", word2 = "pqr"
> 
> Output: "apbqcr"
> 
> Explanation: The merged string will be merged as so:
>
> word1:  a   b   c
>
> word2:    p   q   r
>
> merged: a p b q c r

### Example 2:

> Input: word1 = "ab", word2 = "pqrs"
>
> Output: "apbqrs"
>
> Explanation: Notice that as word2 is longer, "rs" is appended to the end.
>
> word1:  a   b 
>
> word2:    p   q   r   s
>
> merged: a p b q   r   s

# My Solution 
```java
class Solution {
    public String mergeAlternately(String word1, String word2) {
        int m = word1.length(), n = word2.length();
        String result = "";
        int i = 0;
        int j = 0;

        while (i<m || j < n) {
            if (i < m)
                result += word1.charAt(i++);
            if (j < n)
            result += word2.charAt(j++);
        }
        while (i < m) {
            result  += word1.charAt(i++);
        }
        while(j < n) {
            result += word2.charAt(j++);
        }

        return result;
    }
}
```
