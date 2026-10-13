## 01. Print Solid Square

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/print-square-wall-1605682270/1)

### Problem Description

**Task:** Given an integer n, print a solid square pattern of size n × n using "* " (a star followed by exactly one space).

#### Examples

##### Example 1

- **Input:**
```text
n = 5 * * * * ** * * * ** * * * ** * * * ** * * * *
```
- **Explanation:** A solid square of size 5 × 5, with each row containing 5 stars followed by a single space.

##### Example 2

- **Input:**
```text
n = 4Output:* * * * * * * * * * * * * * * * Explanation: A solid square of size 4 × 4, with each row containing 4 stars followed by a single space.
```

#### Constraints

- **1.** `1 ≤ n ≤ 10`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-09-15 16:05:12
- **Status:** Correct
- **Marks:** 1

```java
import java.util.Scanner;

class GFG {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        for(int i=1;i<=n;i++){
            for(int j=1;j<=n;j++){
                System.out.print("*"+" ");
                
            }
            System.out.println();
        }
        
    }
}
```

*Generated on: 10/13/2026, 10:19:51 AM*