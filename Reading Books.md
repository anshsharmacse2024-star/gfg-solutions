## 01. Reading Books

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/reading-books3803/1?page=5&category=Arrays&difficulty=Basic&sortBy=submissions)

### Problem Description

**Task:** Given two arrays arr1[] and arr2[], and an integer k, where arr1[i] represents the time required to read a book of kind i once and arr2[i] represents the points earned after reading it once.
Geek has k minutes and can choose exactly one kind of book. He may read the chosen book repeatedly within the available time, but cannot read books of different kinds.
Return the maximum possible points Geek can earn.

#### Examples

##### Example 1

- **Input:**
```text
k = 10, arr1[] = [3, 4, 5], arr2[] = [4, 4, 5]
```
- **Output:**
```text
12
```
- **Explanation:** Choosing the first kind allows Geek to read it ⌊10 / 3⌋ = 3 times and earn 3 × 4 = 12 points. Choosing the second kind allows Geek to read it ⌊10 / 4⌋ = 2 times and earn 2 × 4 = 8 points. Choosing the third kind allows Geek to read it ⌊10 / 5⌋ = 2 times and earn 2 × 5 = 10 points. Therefore, the maximum points Geek can earn is 12.

##### Example 2

- **Input:**
```text
k = 12, arr1 = [8, 5], arr2 = [100, 5]
```
- **Output:**
```text
100
```
- **Explanation:** Choosing the first kind allows Geek to read it ⌊12 / 8⌋ = 1 time and earn 1 × 100 = 100 points. Choosing the second kind allows Geek to read it ⌊12 / 5⌋ = 2 times and earn 2 × 5 = 10 points. Therefore, the maximum points Geek can earn is 100.

#### Constraints

- **1.** `1 ≤ arr.size() ≤ 10⁵¹ ≤ k, arr1[i]_ ≤ 10⁴⁰ ≤ arr2[i] ≤ 10⁴^`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-09-27 18:48:06
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public int maxPoint(int k, int[] arr1, int[] arr2) {
        // code
        int time=0;
        int point=0;
        for(int i=0;i<arr1.length;i++){
            time=k/arr1[i];
            int cur_point=time*arr2[i];
            point=Math.max(point,cur_point);
        }
        return point;
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-09-27 17:25:32
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public int maxPoint(int k, int[] arr1, int[] arr2) {
        // code
        int time=0;
        int point=0;
        for(int i=0;i<arr1.length;i++){
            time=k/arr1[i];
            int cur_point=time*arr2[i];
            point=Math.max(point,cur_point);
        }
        return point;
    }
}
```

*Generated on: 10/18/2026, 4:33:10 PM*