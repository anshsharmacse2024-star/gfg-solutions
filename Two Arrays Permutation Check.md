## 01. Two Arrays Permutation Check

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/check-if-two-arrays-are-equal-or-not3847/1?page=1&category=Arrays&difficulty=Basic,Easy&sortBy=submissions)

### Problem Description

**Task:** Given two arrays a[] and b[] of equal size, the task is to find whether the given arrays are permutation of each other. Two arrays are said to be permutation if both contain the same set of elements, arrangements of elements may be different though.Note: If there are repetitions, then counts of repeated elements must also be the same for two arrays to be permutation.Examples:Input: a[] = [1, 2, 5, 4, 0], b[] = [2, 4, 5, 0, 1]

#### Examples

##### Example 1

- **Output:**
```text
true
```
- **Explanation:** Both arrays contain the same elements and can be rearranged to [0, 1, 2, 4, 5]. Therefore, the output is true.

##### Example 2

- **Input:**
```text
a[] = [1, 2, 5], b[] = [2, 4, 15]
```
- **Output:**
```text
false
```
- **Explanation:** a[] and b[] have only one common value, 2. All others elements are different so the arrays cannot be rearranged to become equal. Therefore, the output is false.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-16 20:20:05
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public boolean checkPermutation(int[] a, int[] b) {
        // code here
        Arrays.sort(a);
        Arrays.sort(b);
        int l=a.length;
        for(int i=0;i<l;i++){
            if(a[i]!=b[i]){
                return false;
            }
        }
        return true;
    
    }
}
```

*Generated on: 10/18/2026, 9:27:04 AM*