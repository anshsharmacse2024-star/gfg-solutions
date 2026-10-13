## 01. Right-Angled Number Triangle Pattern

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/right-angled-number-triangle/1)

### Problem Description

**Task:** Given a number n. The task is to print Right-Angled Number Triangle with n lines.

> **Note:** There is a space between two adjacent number in the pattern.

#### Examples

##### Example 1

- **Input:**
```text
n = 4 1 1 2 1 2 3 1 2 3 4
```
- **Explanation:** For n = 4 there are 4 rows in the output and the number of elements increases with an increase in the row.

##### Example 2

- **Input:**
```text
n = 5 Output: 1 1 2 1 2 3 1 2 3 4 1 2 3 4 5
```
- **Explanation:** For n = 5 there are 5 rows in the output and the number of elements increases with an increase in the row.

#### Constraints

- **1.** `1 ≤ n ≤ 20`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n^2)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-09-15 16:30:14
- **Status:** Correct
- **Marks:** 0

```java
import java.util.Scanner;

class GFG {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        for(int i=1;i<=n;i++){
            for(int j=1;j<=i;j++){
                System.out.print(j+" ");
            }
            System.out.println();
        }
        

        sc.close();
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-09-15 16:21:52
- **Status:** Correct
- **Marks:** 1

```java
import java.util.Scanner;

class GFG {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        for(int i=1;i<=n;i++){
            for(int j=1;j<=i;j++){
                System.out.print(j+" ");
            }
            System.out.println();
        }
        

        sc.close();
    }
}
```

*Generated on: 10/13/2026, 10:35:28 AM*