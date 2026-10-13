## 01. Count Odd and Even

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/count-odd-even/1?page=1&category=Arrays&difficulty=Basic&sortBy=submissions)

### Problem Description

**Task:** Given an array arr[] of positive integers. The task is to return the count of the number of odd and even elements in the array.

> **Note:** Return two elements where the first one in the count of odd & second one is the count of even.

#### Examples

##### Example 1

- **Input:**
```text
arr[] = [1, 2, 3, 4, 5]
```
- **Output:**
```text
3 2
```
- **Explanation:** There are 3 odd elements (1, 3, 5) and 2 even elements (2 and 4).

##### Example 2

- **Input:**
```text
arr[] = [1, 1]
```
- **Output:**
```text
2 0Explanation: There are 2 odd elements (1, 1) and no even elements.
```

#### Constraints

- **1.** `1 <= arr.size <= 10⁶`
- **2.** `1 <= arr[i] <= 10⁶`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (3)

#### Solution 1 (Java)

- **Submitted:** 2026-09-21 12:12:24
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public int[] countOddEven(int[] arr) {
        // Code here
        int even=0;
        int odd=0;
        for(int i=0;i<arr.length;i++){
        // for(int i:arr){
            if(arr[i]%2==0){
                even++;
            }
            else{
                odd++;
            }
        }
        // int[] arr2 = new int [2]; 
        // arr2[0] = odd;             
        // arr2[1] = even; 
        // return arr2;
        return new int[]{odd,even};
        

    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-09-21 12:07:08
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public int[] countOddEven(int[] arr) {
        // Code here
        int even=0;
        int odd=0;
        for(int i=0;i<arr.length;i++){
            if(arr[i]%2==0){
                even++;
            }
            else{
                odd++;
            }
        }
        // int[] arr2 = new int [2]; 
        // arr2[0] = odd;             
        // arr2[1] = even; 
        // return arr2;
        return new int[]{odd,even};
        

    }
}
```

#### Solution 3 (Java)

- **Submitted:** 2026-09-21 12:05:41
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public int[] countOddEven(int[] arr) {
        // Code here
        int even=0;
        int odd=0;
        for(int i=0;i<arr.length;i++){
            if(arr[i]%2==0){
                even++;
            }
            else{
                odd++;
            }
        }
        int[] arr2 = new int [2]; 
        arr2[0] = odd;             
        arr2[1] = even; 
        return arr2;
        

    }
}
```

*Generated on: 10/13/2026, 10:49:50 AM*