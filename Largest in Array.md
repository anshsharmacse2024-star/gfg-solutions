## 01. Largest in Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/largest-element-in-array4009/1?page=1&category=Arrays&difficulty=Basic)

### Problem Description

**Task:** Given an array arr[]. The task is to find the largest element and return it.Examples:Input: arr[] = [1, 8, 7, 56, 90]

#### Examples

##### Example 1

- **Output:**
```text
10
```
- **Explanation:** There is only one element which is the largest.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-09-21 11:54:25
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public static int largest(int[] arr) {
        // code here
        int lar=0;
        for(int i=0;i<arr.length;i++){
            // if(arr[i]>lar){
            //     lar=arr[i];
            // }
            lar=Math.max(lar, arr[i]);
        }
        return lar;
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-09-21 11:41:28
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
  public:
    int largest(vector<int> &arr) {
        // code here
         int lar=INT_MIN;
        for(int i=0;i<arr.size();i++){
            lar=max(lar, arr[i]);
            
        }
        return lar;
    }
};
```

*Generated on: 10/13/2026, 10:47:46 AM*