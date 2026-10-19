## 01. Spirally Traversing Matrix

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/spirally-traversing-a-matrix-1587115621/1)

### Problem Description

**Task:** Given a rectangular matrix mat[][] of size n x m, and return a 1D array containing all its elements in spiral order.Examples:Input: mat[][] = [[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12], [13, 14, 15, 16]]

#### Examples

##### Example 1

- **Output:**
```text
[32, 44, 27, 23, 62, 50, 28, 54]
```
- **Explanation:** Applying same technique as shown above, output will be [32, 44, 27, 23, 62, 50, 28, 54].Constraints:1 ≤ n, m ≤10000 ≤ mat[i][j] ≤100

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n * m)
- **Expected Auxiliary Space Complexity:** O(n * m)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-19 10:06:51
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    public ArrayList<Integer> spirallyTraverse(int[][] mat) {
        // code here
        ArrayList<Integer> ans = new ArrayList<>();
        int top = 0;
        int left = 0;
        int right = mat[0].length - 1;
        int bottom = mat.length - 1;

        while (left <= right && top <= bottom) {
            // first row
            for (int i = left; i <= right; i++) {
                ans.add(mat[top][i]);
            }
            top++;
            for (int i = top; i <= bottom; i++) {
                ans.add(mat[i][right]);
            }
            right--;
            if ( top <= bottom ) {
                for (int i = right; i >= left; i--) {
                    ans.add(mat[bottom][i]);
                }
                bottom--;
            }
            if ( left  <= right) {
                for (int i = bottom; i >= top; i--) {
                    ans.add(mat[i][left]);
                }
                left++;
            }

        }
        return ans;
    }
}
```

*Generated on: 10/19/2026, 10:07:20 AM*