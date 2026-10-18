## 01. Array Subset

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/array-subset-of-another-array2317/1?page=1&category=Arrays&difficulty=Basic,Easy&sortBy=submissions)

### Problem Description

**Task:** Given two arrays a[] and b[], your task is to determine whether b[] is a subset of a[].Examples:Input: a[] = [11, 7, 1, 13, 21, 3, 7, 3], b[] = [11, 3, 7, 1, 7]

#### Examples

##### Example 1

- **Output:**
```text
false
```
- **Explanation:** b[] is not a subset of a[]

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n + m)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-18 10:14:01
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public boolean isSubset(int a[], int b[]) {
        // code here
        int max=0;
        for(int x:a){
            max=Math.max(x, max);
        }
        for(int x:b){
            max=Math.max(x, max);
        }
        int[] freq=new int[max+1];
        for(int i=0;i<a.length;i++){
            freq[a[i]]++;
        }
        for(int i=0;i<b.length;i++){
            if(freq[b[i]]==0){
                return false;
            }
            freq[b[i]]--;
        }
        return true;
    }
}
```

*Generated on: 10/18/2026, 10:14:25 AM*