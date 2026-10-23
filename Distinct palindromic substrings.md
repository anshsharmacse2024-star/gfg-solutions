## 01. Distinct palindromic substrings

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/distinct-palindromic-substrings5141/1)

### Problem Description

**Task:** Given a string s of lowercase English letters. The task is to find all the distinct continuous palindromic sub-strings which are present in the string s.

> **Note:** You can return the Palindromic sub-strings in any order but the driver code will print the result in sorted order.

#### Examples

##### Example 1

- **Input:**
```text
s = "abaaa"
```
- **Output:**
```text
["a", "aa", "aaa", "aba", "b"]
```
- **Explanation:** All 5 distinct continuous palindromic sub-strings are listed above.

##### Example 2

- **Input:**
```text
s = "geek"
```
- **Output:**
```text
["e", "ee", "g", "k"]
```
- **Explanation:** All 4 distinct continuous palindromic sub-strings are listed above.

#### Constraints

- **1.** `1 ≤ s.length() ≤ 10⁴`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n^2)
- **Expected Auxiliary Space Complexity:** O(n^2)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-23 11:32:30
- **Status:** Correct
- **Marks:** 8

```java
class Solution {
    public ArrayList<String> palindromicSubstr(String s) {
        // code here
        ArrayList<String> ans=new ArrayList<>();
        for(int i=0;i<s.length();i++){
            check(s,i,i,ans);
            check(s,i,i+1,ans);
            
        }
        return ans;
    }
    public void check(String s, int left, int right, ArrayList<String> ans){
        while(left>=0 && right<s.length() && s.charAt(left)==s.charAt(right)){
            String sub=s.substring(left,right+1);
            if(!ans.contains(sub)){
                ans.add(sub);
            }
            left--;
            right++;
        }
    }
}
```

*Generated on: 10/23/2026, 11:32:58 AM*