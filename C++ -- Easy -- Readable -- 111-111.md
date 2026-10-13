## 01. C++ || Easy || Readable || 111/111

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/inverted-triangle-of-stars0110/1)

### Problem Description

**Task:** Given an integer n, print an inverted isosceles triangle of stars such that the height of the triangle is n.

#### Examples

##### Example 1

- **Input:**
```text
n = 4
```
- **Output:**
```text
******* ***** *** *
```

##### Example 2

- **Input:**
```text
n = 3 ***** *** *
```

#### Constraints

- **1.** `1 ≤ n ≤ 100`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-09-16 19:52:43
- **Status:** Correct
- **Marks:** 2

```java
import java.util.Scanner;

class GFG {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int star=2*n-1, sp=0;
        for(int i=1;i<=n;i++){
            for(int j=1;j<=sp;j++){
                System.out.print(" ");
            }
            sp++;
            for(int j=1;j<=star;j++){
                System.out.print("*");
            }
            star=star-2;
            System.out.println();
        }
        
        
    }
}
```

*Generated on: 10/13/2026, 10:33:46 AM*