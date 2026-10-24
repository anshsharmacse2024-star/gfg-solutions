## 01. Most Frequent Character

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/maximum-occuring-character-1587115620/1)

### Problem Description

**Task:** Given a string s of lowercase alphabets. The task is to find the maximum occurring character in the string s. If more than one character occurs the maximum number of times then print the lexicographically smaller character.

#### Examples

##### Example 1

- **Input:**
```text
s = "testsample"
```
- **Output:**
```text
'e'
```
- **Explanation:** 'e' is the character which is having the highest frequency.

##### Example 2

- **Input:**
```text
s = "output"
```
- **Output:**
```text
't'
```
- **Explanation:** 't' and 'u' are the characters with the same frequency, but 't' is lexicographically smaller.

#### Constraints

- **1.** `1 ≤ |s| ≤ 100`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-24 14:14:27
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public static char getMaxOccuringChar(String s) {
        // code here
        // StringBuilder str=new StringBuilder(s);
        // int i=0;
        int[] freq=new int[26];
        for(int i=0;i<s.length();i++){
            int v=(int)(s.charAt(i)-'a');
            freq[v]++;
        }
        int max=-1;
        char ans='a';
        for(int i=0;i<freq.length;i++){
            if(freq[i]>max){
                max=freq[i];
                ans=(char)(i+'a');
            }
        }
        return ans;
        
    }
}
```

*Generated on: 10/24/2026, 2:15:37 PM*