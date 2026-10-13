## 01. Diamond Shape Pattern

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/pattern/1)

### Problem Description

**Task:** Given a number n, print a diamond-shaped star pattern with 2n rows, where the number of stars first increases and then decreases to form the diamond.

#### Examples

##### Example 1

- **Input:**
```text
n = 5Output:
```

##### Example 2

- **Input:**
```text
n = 3Output: * * ** * ** * * * * *
```

#### Constraints

- **1.** `1 ≤ n ≤ 100`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n^2)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-09-16 10:49:17
- **Status:** Correct
- **Marks:** 0

```java
import java.util.Scanner;

class GFG {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        // code here
        int a=1;
        for(int i=1;i<=n;i++){
            for(int j=1;j<=n-i;j++){
                System.out.print(" ");
            }
            for(int j=1;j<=a;j++){
                System.out.print("* ");
            }
            a++;
            System.out.println();
            
        }
        int str=n;
        for(int i=1;i<=n;i++){
            for(int j=1;j<=i-1;j++){
                System.out.print(" ");
            }
            for(int j=1;j<=str;j++){
                System.out.print("* ");
            }
            str--;
            System.out.println();
        }
        
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-09-16 10:42:50
- **Status:** Correct
- **Marks:** 1

```java
import java.util.Scanner;

class GFG {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        // code here
        int a=1;
        for(int i=1;i<=n;i++){
            for(int j=1;j<=n-i;j++){
                System.out.print(" ");
            }
            for(int j=1;j<=a;j++){
                System.out.print("* ");
            }
            a++;
            System.out.println();
            
        }
        int str=n;
        for(int i=1;i<=n;i++){
            for(int j=1;j<=i-1;j++){
                System.out.print(" ");
            }
            for(int j=1;j<=str;j++){
                System.out.print("* ");
            }
            str--;
            System.out.println();
        }
        
    }
}
```

*Generated on: 10/13/2026, 10:32:26 AM*