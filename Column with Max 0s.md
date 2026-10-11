## 01. Column with Max 0s

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/predict-the-column/1)

### Problem Description

**Task:** You are given a matrix mat[][] of size n × n consisting only of 0s and 1s. Your task is to find the index of the column that contains the maximum number of 0s.
If more than one column has the same maximum number of 0s, return the index of the leftmost such column.
If no column contains any 0 (i.e., all elements in the matrix are 1), return -1.

#### Examples

##### Example 1

- **Input:**
```text
mat[][] = [[0, 0, 0], [1, 0, 1], [0, 1, 1]]
```
- **Output:**
```text
0
```
- **Explanation:** Columns 0 and 1 contain the same number of 0s; however, column 0 appears first, so the answer is 0.

##### Example 2

- **Input:**
```text
mat[][] = [[1, 1, 1], [1, 1, 1], [1, 1, 1]]
```
- **Output:**
```text
-1
```
- **Explanation:** Since no column contains any 0s, the answer is -1.

#### Constraints

- **1.** `1 ≤ n ≤ 10³⁰ ≤ mat[i][j] ≤ 1`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n^2)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-06 16:28:26
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public int maxZeros(int[][] mat) {
        // code here
        int zero=0;
        int ans=-1;
        int c=mat[0].length;
        int r=mat.length;

        for(int i=0;i<c;i++){
            int count=0;
            for(int j=0;j<r;j++){
                if(mat[j][i]==0){
                    count++;
                }
                
            }
            if(zero<count){
                zero=count;
                ans=i;
                // return ans;
            }
        }
        return ans;
    }
}
```

*Generated on: 10/11/2026, 6:28:57 AM*