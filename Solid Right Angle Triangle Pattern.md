## 01. Solid Right Angle Triangle Pattern

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/right-angle-triangle-1605685807/1)

### Problem Description

**Task:** Given an integer n. Write a program to print the Right angle triangle wall. The length of perpendicular and base is s. Note: Print exactly single " " after "*". Print a new line after printing the triangle.Example:Input: n = 4

#### Examples

##### Example 1

- **Explanation:** * * * * * * * * * * Explanation: Length of perpendicular and base of triangle is 4 .Input: n = 3 * * * * * * Explanation: Length of perpendicular and base of triangle is 3 .

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n^2)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-09-15 16:28:45
- **Status:** Correct
- **Marks:** 0

```java
import java.util.Scanner;

class GFG {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        // code here
        for(int i=1;i<=n;i++){
            for(int j=1;j<=i;j++){
                System.out.print("* ");
            }
            System.out.println();
        }

        sc.close();
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-09-15 16:26:30
- **Status:** Correct
- **Marks:** 2

```java
import java.util.Scanner;

class GFG {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        // code here
        for(int i=1;i<=n;i++){
            for(int j=1;j<=i;j++){
                System.out.print("* ");
            }
            System.out.println();
        }

        sc.close();
    }
}
```

*Generated on: 10/13/2026, 10:23:25 AM*