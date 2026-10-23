## 01. Sum Numbers in a String

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/sum-of-numbers-in-string-1587115621/1)

### Problem Description

**Task:** Given a string s containing alphanumeric characters. You have to calculate the sum of all the numbers present in the string.

#### Examples

##### Example 1

- **Input:**
```text
s = "1abc23"
```
- **Output:**
```text
24
```
- **Explanation:** 1 and 23 are numbers in the string which is added to get the sum as 24.

##### Example 2

- **Input:**
```text
s = "geeks4geeks"
```
- **Output:**
```text
4
```
- **Explanation:** 4 is the only number, so the sum is 4.

#### Constraints

- **1.** `1 ≤ |s|≤ 10⁵The sum of Numbers ≤ 10⁵`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-23 12:17:59
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public static int findSum(String s) {
        // code here
        boolean status=true;
        int ans=0;
        int sum=0;
        for(int i=0;i<s.length();i++){
            if(s.charAt(i)>=48 && s.charAt(i)<=57){
                status=true;
                if(status==true){
                    sum=sum*10+s.charAt(i)-48;
                }
            }else{
                status=false;
                ans=ans+sum;
                sum=0;
            }
        }
        ans=ans+sum;
        return ans;
    }
}
```

*Generated on: 10/23/2026, 3:54:35 PM*