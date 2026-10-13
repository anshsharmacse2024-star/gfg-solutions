## 01. Array or List Traversal

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/array-traversal/1?page=1&category=Arrays&difficulty=Basic&sortBy=submissions)

### Problem Description

**Task:** Given an array arr[] of size n that contains integers. Print the elements of the array in a single line with a space between them.Note: Don't add a new line at the end.Examples:Input: arr[] = [54, 43, 2, 1, 5]

#### Examples

##### Example 1

- **Output:**
```text
324 5 2 2
```
- **Explanation:** Just traverse and print the numbers.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-10-13 10:40:44
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public void arrayTraversal(int[] arr) {
        // code here
        for(int i=0;i<arr.length;i++){
            System.out.print(arr[i]+" ");
        }
        
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-09-21 11:28:49
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public static void arrayTraversal(int[] arr) {
        // Code here
        for(int i=1;i<=arr.length;i++){
            System.out.print(arr[i-1]+" ");
        }
    }
}
```

*Generated on: 10/13/2026, 10:41:21 AM*