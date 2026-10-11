## 01. Matrix Boundary Traversal

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/boundary-traversal-of-matrix-1587115620/1)

### Problem Description

**Task:** You are given a matrix mat[][] . Return the boundary traversal on the matrix in a clockwise manner starting from the first row of the matrix. Examples:

#### Examples

##### Example 1

- **Input:**
```text
mat[][] = [[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12], [13, 14, 15,16]]
```
- **Output:**
```text
[1, 2, 3, 4, 8, 12, 16, 15, 14, 13, 9, 5]
```
- **Explanation:** The boundary traversal is: [1, 2, 3, 4, 8, 12, 16, 15, 14, 13, 9, 5]

##### Example 2

- **Input:**
```text
mat[][] = [[12, 11, 10, 9], [8, 7, 6, 5], [4, 3, 2, 1]]
```
- **Output:**
```text
[12, 11, 10, 9, 5, 1, 2, 3, 4, 8]Explanation: The boundary traversal is: [12, 11, 10, 9, 5, 1, 2, 3, 4, 8]
```

##### Example 3

- **Input:**
```text
mat[][] = [[12, 11], [4, 3]] Output: [12, 11, 3, 4]Explanation: The boundary traversal is: [12, 11, 3, 4]
```

#### Constraints

- **1.** `1 ≤ mat.size()≤ 10001 ≤ mat[0].size() ≤ 10000 ≤ mat[i][j] ≤ 1000`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-10-06 15:17:15
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public ArrayList<Integer> boundaryTraversal(int mat[][]) {
        // code here
        ArrayList<Integer> ans=new ArrayList<>();
        int r=mat.length;
        int c=mat[0].length;
        for(int i=0;i<c;i++){
            ans.add(mat[0][i]);
        }
        for(int i=1;i<r;i++){
            ans.add(mat[i][c-1]);
        }
        if(r>1){
        for(int i=c-2;i>=0;i--){
            ans.add(mat[r-1][i]);
        }
        }
        if(c>1){
        for(int i=r-2;i>=1;i--){
            ans.add(mat[i][0]);
        }
        }
        return ans;
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-10-06 15:16:34
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public ArrayList<Integer> boundaryTraversal(int mat[][]) {
        // code here
        ArrayList<Integer> ans=new ArrayList<>();
        int r=mat.length;
        int c=mat[0].length;
        for(int i=0;i<c;i++){
            ans.add(mat[0][i]);
        }
        for(int i=1;i<r;i++){
            ans.add(mat[i][c-1]);
        }
        if(r>1){
        for(int i=c-2;i>=0;i--){
            ans.add(mat[r-1][i]);
        }
        }
        if(c>1){
        for(int i=r-2;i>=1;i--){
            ans.add(mat[i][0]);
        }
        }
        return ans;
    }
}
```

*Generated on: 10/11/2026, 6:30:11 AM*