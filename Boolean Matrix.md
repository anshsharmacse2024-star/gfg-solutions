## 01. Boolean Matrix

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/boolean-matrix-problem-1587115620/1)

### Problem Description

**Task:** Given a boolean matrix mat[], where each cell contains either 0 or 1, modify it such that if a matrix cell matrix[i][j] is 1 then all the cells in its i^th row and j^th column will become 1.Examples:Input: mat[][] = [[1, 0], [0, 0]]

#### Examples

##### Example 1

- **Output:**
```text
[[0, 0], [0, 0]]
```
- **Explanation:** There is no cell that contains 1, so mat[] will remain the same.Constraints:1 ≤ mat.size(), mat[0].size() ≤ 10³⁰ ≤ mat[i][j] ≤ 1

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n^2)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-20 22:13:09
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    void booleanMatrix(int mat[][]) {
        // code here
        int r=mat.length;
        int c=mat[0].length;
        int[] freqA=new int[r];
        int[] freqB=new int[c];
        for(int i=0;i<r;i++){
            for(int j=0;j<c;j++){
                if(mat[i][j]==1){
                    freqA[i]=1;
                    freqB[j]=1;
                }
            }
        }
        for(int i=0;i<r;i++){
            for(int j=0;j<c;j++){
                if(freqA[i]==1 || freqB[j]==1){
                    mat[i][j]=1;
                }
            }
        }
        
    }
}
```

*Generated on: 10/20/2026, 10:13:46 PM*