## 01. Element at Index in Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/c-array-print-an-element-set-25933/1?page=1&category=Arrays&difficulty=Basic&sortBy=submissions)

### Problem Description

**Task:** Given an array arr[] of integers and an index i(0-based index). Return the element present at the index i in the array.Examples:Input: i = 2 , arr[] = [10, 20, 30, 40, 50]

#### Examples

##### Example 1

- **Output:**
```text
50Explanation: The value of the arr[4] is 50 .Constraints:1 ≤ arr.size() ≤ 10⁶⁰ ≤ i ≤ arr.size() - 11 ≤ arr[i] ≤ 10⁹
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(1)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-10-13 10:38:14
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public int findElementAtIndex(int i, int[] arr) {
        // code here
        for(int j=0;j<arr.length;j++){
            if(arr[i]==arr[j]){
                break;
            }
        }
        return arr[i];
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-09-21 11:26:41
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public int findElementAtIndex(int i, int[] arr) {
        // code here
        return arr[i];
    }
}
```

*Generated on: 10/13/2026, 10:39:53 AM*