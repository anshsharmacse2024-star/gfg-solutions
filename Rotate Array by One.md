## 01. Rotate Array by One

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/cyclically-rotate-an-array-by-one2614/1?page=1&category=Arrays&difficulty=Basic&sortBy=submissions)

### Problem Description

**Task:** Given an array arr[], rotate the array by one position in clockwise direction.Examples:Input: arr[] = [1, 2, 3, 4, 5]

#### Examples

##### Example 1

- **Output:**
```text
[3, 9, 8, 7, 6, 4, 2, 1]Explanation: After rotating clock-wise 3 comes in first position.
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-13 20:30:21
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public void rotate(int[] arr) {
        // code here
        int l=arr.length;
        
        int temp=arr[l-1];
        for(int i=l-1;i>0;i--){
              arr[i]=arr[i-1];
        }
        arr[0]=temp;
    }
}
```

*Generated on: 10/13/2026, 8:31:04 PM*