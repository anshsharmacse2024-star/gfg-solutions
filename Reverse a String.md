## 01. Reverse a String

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/reverse-a-string/1)

### Problem Description

**Task:** Given a string s, reverse the string.Examples:Input: s = "Geeks"

#### Examples

##### Example 1

- **Output:**
```text
"skeeG"
```

##### Example 2

- **Input:**
```text
s = "for"
```
- **Output:**
```text
"a"
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-10-23 10:19:57
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public static String reverseString(String s) {
        // code here
    //     String ans="";
    // for(int i=s.length()-1;i>=0;i--){
    //     ans+=s.charAt(i);
    // }
    // return ans;
     
             StringBuilder ans = new StringBuilder();
             for (int i = 0; i < s.length(); i++) {
                 ans.insert(0, s.charAt(i));
             }
             return ans.toString();
    }
    
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-10-23 10:18:18
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public static String reverseString(String s) {
        // code here
        String ans="";
    //   StringBuilder ans=new StringBuilder();
    for(int i=s.length()-1;i>=0;i--){
        ans+=s.charAt(i);
    }
    return ans;
    }
}
```

*Generated on: 10/23/2026, 10:47:42 AM*