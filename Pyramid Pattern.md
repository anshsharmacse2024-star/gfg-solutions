## 01. Pyramid Pattern

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/pyramid-patterns/1)

### Problem Description

**Task:** Given a number n, print pyramid pattern with n lines.

#### Examples

##### Example 1

- **Input:**
```text
n = 4 Output: * *** ***** *******
```

##### Example 2

- **Input:**
```text
n = 5 Output: * *** ***** ****************
```

#### Constraints

- **1.** `1 ≤ n ≤ 100`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n^2)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-09-16 10:12:24
- **Status:** Correct
- **Marks:** 1

```java
import java.util.Scanner;

class GFG {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int a=1;
        // code here
        for(int i=1;i<=n;i++){
            for(int j=1;j<=n-i;j++){
                System.out.print(" ");
            }
            for(int j=1;j<=a;j++){
                System.out.print("*");
            }
            a=a+2;
            System.out.println();
        }

        sc.close();
    }
}
```

*Generated on: 10/13/2026, 10:18:41 AM*