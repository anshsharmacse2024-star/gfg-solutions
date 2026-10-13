## 01. Half Diamond Star Pattern

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/triangle-pattern-1661718013/1)

### Problem Description

**Task:** Given an integer n, print the Half Diamond Star Pattern using * characters as shown in the examples.

#### Examples

##### Example 1

- **Input:**
```text
5 * * * * * * * * * * * * * * * * * * * * * * * * *
```

##### Example 2

- **Input:**
```text
3 * * * * * * * * *
```

#### Constraints

- **1.** `1 ≤ n ≤ 100`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n^2)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-09-16 18:12:29
- **Status:** Correct
- **Marks:** 1

```java
import java.util.Scanner;

class GFG {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int star=0;
        // code here
        for(int i=1;i<=2*n-1;i++){
            if(i<=n){
                star++;
                for(int j=1;j<=star;j++){
                    System.out.print("* ");
                    
                }
                
            }
            else{
                star--;
                for(int j=1;j<=star;j++){
                    System.out.print("* ");
                }
            }
            System.out.println();
        }
    }
}
```

*Generated on: 10/13/2026, 10:34:37 AM*