## 01. Max Consecutive Bit

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/max-consecutive-one/1)

### Problem Description

**Task:** Given an array arr[] consisting of only 0’s and 1’s, return count of the maximum number of consecutive 1’s or 0’s present in the array.

#### Examples

##### Example 1

- **Input:**
```text
arr[] = [0, 1, 0, 1, 1, 1, 1]Output: 4Explanation: The maximum number of consecutive 1’s in the array is 4 from index 3-6.
```

##### Example 2

- **Input:**
```text
arr[] = [0, 0, 1, 0, 1, 0]Output: 2Explanation: The maximum number of consecutive 0’s in the array is 2 from index 0-1.
```

##### Example 3

- **Input:**
```text
arr[] = [0, 0, 0, 0]Output: 4Explanation: The maximum number of consecutive 0’s in the array is 4.
```

#### Constraints

- **1.** `1 ≤ arr.size() ≤ 10⁵⁰ ≤ arr[i] ≤ 1`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-09-25 11:41:41
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public int maxConsecBits(int[] arr) {
        // code here
        int count_zero=0;
             int count_one=0;
             int max_zero=Integer.MIN_VALUE;
             int max_one=Integer.MIN_VALUE;
             int ans=0;
             for(int i=0;i<arr.length;i++){
                 if(arr[i]==0){
                     count_zero++;
                     max_zero=Math.max(count_zero, max_zero);
                     count_one=0;
                 }else{
                     count_one++;
                     max_one=Math.max(count_one, max_one);
                     count_zero=0;
                 }
             }

            ans=Math.max(max_zero, max_one);
            return ans;
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-09-25 11:39:21
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public int maxConsecBits(int[] arr) {
        // code here
        int count_zero=0;
                 int count_one=0;
                 int max_zero=Integer.MIN_VALUE;
                 int max_one=Integer.MIN_VALUE;
                 int ans=Integer.MIN_VALUE;
                 for(int i=0;i<arr.length;i++){
                     if(arr[i]==0){
                         count_zero++;
                         max_zero=Math.max(count_zero, max_zero);
                         count_one=0;
                     }else{
                         count_one++;
                         max_one=Math.max(count_one, max_one);
                         count_zero=0;
                     }
                 }

                ans=Math.max(max_zero, max_one);
                return ans;
    }
}
```

*Generated on: 10/18/2026, 4:38:27 PM*