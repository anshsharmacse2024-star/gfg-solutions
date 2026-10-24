## 01. Search a Character in a String

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/search-a-character-in-a-string/1)

### Problem Description

**Task:** Write a program to search for a given character in a string. If the character is found, print the index/position where it first appears in the string. If the character is not found, print -1.Examples:Input: s = "geeksforgeeks" , ch = 'k'Output: 3Explanation: The character 'k' is present at index 3 and 11 in "geeksforgeeks" , so the first index is 3.Input: s = "geeksforgeeks" , ch = 'z'Output: -1Explanation: The character 'z' is not present in "geeksforgeeks".

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-24 13:40:24
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    // Function to search for a character in the string
    public int searchCharacter(String s, char ch) {
        // code here
        for(int i=0;i<s.length();i++){
            if(s.charAt(i)==ch){
                return i;
            }
        }
        return -1;
    }
}
```

*Generated on: 10/24/2026, 1:40:50 PM*