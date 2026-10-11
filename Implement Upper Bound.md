## 01. Implement Upper Bound

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/implement-upper-bound/1)

### Problem Description

**Task:** Given a sorted array arr[] and a number target, the task is to find the upper bound of the target in this given array.The upper bound is the smallest index in the sorted array where the element is greater than the given target. If all the elements in the given array are smaller than or equal to the target, the upper bound will be the length of the array.Examples :Input: arr[] = [2, 3, 7, 10, 11, 11, 25], target = 9

#### Examples

##### Example 1

- **Output:**
```text
7
```
- **Explanation:** As no element in arr[] is greater than 100, return the length of array.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-09-28 18:53:41
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    int upperBound(int[] arr, int t) {
        // code here
        int low=0;
        int high=arr.length-1;
        int index=0;
        int ans=0;
        while(low<=high){
            int mid=low+(high-low)/2;
            if(arr[mid]>t){
                // ans=mid;
                // index=Math.max(ans, index);
                high=mid-1;
            }else{
                ans=mid+1;
                index=Math.max(ans, index);
                low=mid+1;
            }
        }
        return index;
    }
}
```

*Generated on: 10/11/2026, 6:31:08 AM*