## 01. Exit Point in a Matrix

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/exit-point-in-a-matrix0905/1)

### Problem Description

**Task:** Given a matrix mat[][] of size n × m consisting of 0s and 1s. You start at the top-left cell (0, 0). Initially, you are positioned at (0, 0) and facing right (toward (0, 1)). Before each move, apply the rules based on the value of the current cell:If the current cell contains 0, continue moving in the same direction.If the current cell contains 1, change your direction to the right (clockwise turn), and update the cell value to 0.You continue this process until you move outside the boundaries of the matrix. Determine the coordinates (row and column index) of the cell from which you exit the matrix.Examples:Input: mat[][] = [[0, 1, 0],
[0, 1, 1], [0, 0, 0]]

#### Examples

##### Example 1

- **Output:**
```text
[1, 0]
```
- **Explanation:** From the image we can see that, enter the matrix at (0, 0) - > then move towards (0, 1) - > 1 is encountered - > turn right towards (1, 1) - > again 1 is encountered - > turn right again towards (1, 0) - > now, the boundary of matrix will be crossed. Hence, exit point reached at [1, 0].

##### Example 2

- **Input:**
```text
mat[][] = [[1, 1], [0, 1]]
```
- **Output:**
```text
[1, 0]Explanation:Enter the matrix at (0, 0) facing right - > 1 is encountered at (0, 0) - > turn right and move to (1, 0) - > 0 is encountered at (1, 0) - > continue moving down and cross the matrix boundary. Hence, the exit point is reached at [1, 0].Constraints:1 ≤ n, m ≤ 100
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n * m)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-20 20:33:45
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    public List<Integer> exitPoint(int[][] mat) {
        // code here
        int i = 0, j = 0;
        int dir = 0;
        int n=mat.length;
        int m=mat[0].length;
        // 0 = Right, 1 = Down, 2 = Left, 3 = Up
        while (i >= 0 && i < n && j >= 0 && j < m) {

            if (mat[i][j] == 1) {
                mat[i][j] = 0;
                dir = (dir + 1) % 4;
            }

            if (dir == 0) {
                j++;
            } else if (dir == 1) {
                i++;
            } else if (dir == 2) {
                j--;
            } else {
                i--;
            }
        }

        // Return the last valid position
        if (dir == 0) j--;
        else if (dir == 1) i--;
        else if (dir == 2) j++;
        else i++;
        List<Integer> ans=new ArrayList<>();
        ans.add(i);
        ans.add(j);
        

        return ans;
    }
}
```

*Generated on: 10/20/2026, 8:53:19 PM*