## 01. Selection Sort

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/selection-sort/1)

### Problem Description

**Task:** Given an array arr, use selection sort to sort arr[] in increasing order.Examples :Input: arr[] = [4, 1, 3, 9, 7]

#### Examples

##### Example 1

- **Output:**
```text
[14, 20, 30, 31, 38]
```
- **Explanation:** Maintain sorted (in bold) and unsorted subarrays. Select 1. Array becomes 1 4 3 9 7. Select 3. Array becomes 1 3 4 9 7. Select 4. Array becomes 1 3 4 9 7. Select 7. Array becomes 1 3 4 7 9. Select 9. Array becomes 1 3 4 7 9.Input: arr[] = [10, 9, 8, 7, 6, 5, 4, 3, 2, 1]

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n^2)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-14 19:00:22
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    void selectionSort(int[] arr) {
        // code here
        int k=0;
        for(int i=0;i<arr.length;i++){
            int min=Integer.MAX_VALUE;
            for(int j=i;j<arr.length;j++){
                if(arr[j]<min){
                    min=arr[j];
                    k=j;
                }
            }if(min<arr[i]){
                int temp=arr[k];
                arr[k]=arr[i];
                arr[i]=temp;
            }
        }
    }
}
```

*Generated on: 10/14/2026, 7:06:49 PM*