## 01. Sort Matrix

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/sorted-matrix2333/1)

### Problem Description

**Task:** Given a square matrix mat[][], sort all the elements of the matrix in non-decreasing order and return the resulting matrix.Examples:Input: mat[][] = [[10, 20, 30, 40], [15, 25, 35, 45], [27, 29, 37, 48], [32, 33, 39, 50]]Output: [[10, 15, 20, 25], [27, 29, 30, 32], [33, 35, 37, 39], [40, 45, 48, 50]]Explanation: Sorting the matrix gives this result:Input: mat[][] = [[1, 5, 3], [2, 8, 7], [4, 6, 9]]Output: [[1, 2, 3], [4, 5, 6], [7, 8, 9]]Explanation: Sorting the matrix gives this result:

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n^2 * (log n))
- **Expected Auxiliary Space Complexity:** O(n^2)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-22 17:56:35
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public int[][] sortedMatrix(int mat[][]) {
        // code here
        int n=mat.length;
        int m=mat[0].length;
        int[] arr=new int[n*m];
        int k=0;
        for(int i=0;i<n;i++){
            for(int j=0;j<m;j++){
                arr[k++]=mat[i][j];
            }
        }
       
        Arrays.sort(arr);
        k=0;
        int[][] result=new int[n][m];
        for(int i=0;i<n;i++){
            for(int j=0;j<m;j++){
                result[i][j]=arr[k++];
            }
        }
        return result;
        
    }
};
```

*Generated on: 10/22/2026, 5:57:04 PM*