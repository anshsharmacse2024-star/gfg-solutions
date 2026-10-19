## 01. Sum of upper and lower triangles

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/sum-of-upper-and-lower-triangles-1587115621/1)

### Problem Description

**Task:** Given a square matrix mat[][] of size n*n, return an array of two elements containing two values: the sum of Upper Triangle elements and the sum of Lower Triangle elements. Upper Triangle consists of elements on the diagonal and above it. The lower triangle consists of elements on the diagonal and below it. Examples:Input: n = 3, mat[][] = [[6, 5, 4],
[1, 2, 5],
[7, 9, 7]]

#### Examples

##### Example 1

- **Output:**
```text
[7, 8]
```
- **Explanation:** Upper triangular matrix: 1 2 4 Sum of these elements are 1 + 2 + 4 = 7. Lower triangular matrix: 1 3 4 Sum of these elements are 1 + 3 + 4 = 8.Constraints: 1 ≤ n ≤ 500¹ ≤ mat[i][j] ≤ 1000

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n^2)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-10-19 10:32:10
- **Status:** Correct
- **Marks:** 0

```java
// class Solution {
//     public ArrayList<Integer> sumTriangles(int mat[][]) {
//         // code here
//         ArrayList<Integer> ans=new ArrayList<>();
//         int c=mat[0].length;
//         int r=mat.length;
//         int upperSum=0;
//         int lowerSum=0;
//         int left=0;
//         int right=1;
//         for(int i=0;i<r;i++){
//             for(int j=left;j<c;j++){
//                 upperSum=upperSum+mat[i][j];
//             }
//             left++;
//         }
//         ans.add(upperSum);
//         for(int i=0;i<r;i++){
//             for(int j=0;j<right;j++){
//                 lowerSum=lowerSum+mat[i][j];
//             }
//             right++;
//         }
//         ans.add(lowerSum);
       
//       return ans;
//     }
// }
class Solution {
    public ArrayList<Integer> sumTriangles(int mat[][]) {
        ArrayList<Integer> ans=new ArrayList<>();
        int n=mat.length;
        int m=mat[0].length;
        int upper=0;
        int lower=0;
        for(int i=0;i<n;i++){
            for(int j=0;j<m;j++){
                if(j>=i){
                    upper=upper+mat[i][j];
                }
            }
        }
        ans.add(upper);
        for(int i=0;i<n;i++){
            for(int j=0;j<m;j++){
                if(j<=i){
                    lower=lower+mat[i][j];
                }
            }
        }
        ans.add(lower);
        return ans;
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-10-07 10:48:41
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public ArrayList<Integer> sumTriangles(int mat[][]) {
        // code here
        ArrayList<Integer> ans=new ArrayList<>();
        int c=mat[0].length;
        int r=mat.length;
        int upperSum=0;
        int lowerSum=0;
        int left=0;
        int right=1;
        for(int i=0;i<r;i++){
            for(int j=left;j<c;j++){
                upperSum=upperSum+mat[i][j];
            }
            left++;
        }
        ans.add(upperSum);
        for(int i=0;i<r;i++){
            for(int j=0;j<right;j++){
                lowerSum=lowerSum+mat[i][j];
            }
            right++;
        }
        ans.add(lowerSum);
       
       return ans;
    }
}
```

*Generated on: 10/19/2026, 10:32:43 AM*