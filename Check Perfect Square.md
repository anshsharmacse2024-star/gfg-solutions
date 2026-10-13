## 01. Check Perfect Square

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/check-perfect-square5253/1)

### Problem Description

**Task:** Given a positive integer n, return true if it is a perfect square, otherwise return false. A number is called a perfect square if it can be written in the form a × a, where a is an integer.

#### Examples

##### Example 1

- **Input:**
```text
n = 35
```
- **Output:**
```text
false
```
- **Explanation:** 35 is not a perfect square.

##### Example 2

- **Input:**
```text
n = 49
```
- **Output:**
```text
true
```
- **Explanation:** 49 is a perfect square (7 * 7 = 49).

#### Constraints

- **1.** `1 ≤ n ≤ 10⁵`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-13 21:44:00
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public boolean isPerfectSquare(int num) {
        // code here
        long low=1;
        long high=num;
        if(num<=1){
            return true;
        }
        while(low<=high){
            long mid=low+(high-low)/2;
            long x=mid*mid;
            if(x==num){
                return true;
            }else if(x>num){
                high=mid-1;
            }else{
                low=mid+1;
            }
        }
        return false;
    }
}
```

*Generated on: 10/13/2026, 9:44:26 PM*