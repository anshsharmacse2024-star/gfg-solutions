## 01. Inverted Right Angle Triangle Pattern

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/inverted-right-angletriangle-1605691171--104349/1)

### Problem Description

**Task:** Given an integer n. Write a program to print the inverted "Right angle triangle" wall. The length of the perpendicular and base is n.

#### Examples

##### Example 1

- **Input:**
```text
n = 5 ************ ***
```
- **Explanation:** Length of perpendicular and base of triangle is 5.

##### Example 2

- **Input:**
```text
n = 3Output:*** ** *
```
- **Explanation:** Length of perpendicular and base of triangle is 3.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n^2)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-13 10:30:02
- **Status:** Correct
- **Marks:** 2

```java
import java.util.Scanner;

class GFG {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        // code here
        int star=n;
        for(int i=0;i<n;i++){
            for(int j=0;j<star;j++){
                System.out.print("*");
            }
            star--;
            System.out.println();
        }

        sc.close();
    }
}
```

*Generated on: 10/13/2026, 10:38:21 AM*