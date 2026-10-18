## 01. Rotate Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/rotate-array-by-n-elements-1587115621/1)

### Problem Description

**Task:** Given an array arr[]. Rotate the array to the left (counter-clockwise direction) by d steps, where d is a positive integer. Do the mentioned change in the array in place.Note: Consider the array as circular.Examples :Input: arr[] = [1, 2, 3, 4, 5], d = 2

#### Examples

##### Example 1

- **Output:**
```text
[3, 9, 1, 7]
```
- **Explanation:** when we rotate 9 times, we'll get [3, 9, 1, 7] as resultant array.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-10-18 10:38:08
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public void rotateArr(int arr[], int d) {
        // code here
        // int n=arr.length;
        // d=d%n;
        // int l=0;
        // int r=n-1;
        // while(l<r){
        //     int temp=arr[r];
        //     arr[r]=arr[l];
        //     arr[l]=temp;
        //     l++;
        //     r--;
        // }
        // l=0;
        // r=n-d-1;
        // while(l<r){
        //     int temp=arr[r];
        //     arr[r]=arr[l];
        //     arr[l]=temp;
        //     l++;
        //     r--;
        // }
        // l=n-d;
        // r=n-1;
        // while(l<r){
        //     int temp=arr[r];
        //     arr[r]=arr[l];
        //     arr[l]=temp;
        //     l++;
        //     r--;
        // }
        int n=arr.length;
        d=d%n;
        reverse(arr, 0, n-1);
        reverse(arr, 0, n-d-1);
        reverse(arr, n-d, n-1);
        
    }
        void reverse(int arr[], int l, int r){
            while(l<r){
                int temp=arr[r];
                arr[r]=arr[l];
                arr[l]=temp;
                l++;
                r--;
            }
        }
        
}
//5,4,3,2,1
```

#### Solution 2 (Java)

- **Submitted:** 2026-10-18 10:34:34
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public void rotateArr(int arr[], int d) {
        // code here
        int n=arr.length;
        d=d%n;
        int l=0;
        int r=n-1;
        while(l<r){
            int temp=arr[r];
            arr[r]=arr[l];
            arr[l]=temp;
            l++;
            r--;
        }
        l=0;
        r=n-d-1;
        while(l<r){
            int temp=arr[r];
            arr[r]=arr[l];
            arr[l]=temp;
            l++;
            r--;
        }
        l=n-d;
        r=n-1;
        while(l<r){
            int temp=arr[r];
            arr[r]=arr[l];
            arr[l]=temp;
            l++;
            r--;
        }
        
    }
}
//5,4,3,2,1
```

*Generated on: 10/18/2026, 10:38:34 AM*