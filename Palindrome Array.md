## 01. Palindrome Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/perfect-arrays4645/1?page=2&category=Arrays&difficulty=Basic&sortBy=submissions)

### Problem Description

**Task:** Given an array arr[], the task is to find whether the arr is palindrome or not. An array is said to be palindrome if its reverse array matches the original array.

#### Examples

##### Example 1

- **Input:**
```text
arr = [1, 2, 3, 2, 1]
```
- **Output:**
```text
true
```
- **Explanation:** If we reverse, we get [1, 2, 3, 2, 1] which is the same as before. So, the answer is true.

##### Example 2

- **Input:**
```text
arr = [1, 2, 3, 4, 5]
```
- **Output:**
```text
falseExplanation: If we reverse it, we get [5, 4, 3, 2, 1] which is the not same as before. So, the answer false.
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-09-23 17:46:55
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public static boolean isPalindrome(int[] arr) {
        // code here
        int i=0;
        int j=arr.length-1;
        while(i<j){
            if(arr[i]==arr[j]){
                i++;
                j--;
            }else{
                return false;
            }
        }
        return true;
    }
}
```

*Generated on: 10/16/2026, 8:16:57 PM*