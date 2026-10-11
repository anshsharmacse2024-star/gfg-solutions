## 01. Triplet Sum in Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/triplet-sum-in-array-1587115621/1)

### Problem Description

**Task:** Given an array arr[] and an integer target, determine if there exists a triplet in the array whose sum equals the given target.Return true if such a triplet exists, otherwise, return false.Examples: Input: arr[] = [1, 4, 45, 6, 10, 8], target = 13Output: true Explanation: The triplet {1, 4, 8} sums up to 13.Input: arr[] = [1, 2, 4, 3, 6, 7], target = 10Output: true Explanation: The triplets {1, 3, 6} and {1, 2, 7} both sum to 10. Input: arr[] = [40, 20, 10, 3, 6, 7], target = 24Output: false Explanation: No triplet in the array sums to 24.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n^2)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-10-11 06:22:23
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public boolean hasTripletSum(int arr[], int target) {
        // code Here
        // int sum=0;
        int n=arr.length;
        // for(int i=0;i<n;i++){
        //     for(int j=i+1;j<n;j++){
        //         for(int k=j+1;k<n;k++){
        //             sum=arr[i]+arr[j]+arr[k];
        //             if(sum==target){
        //                 return true;
        //             }
        //         }
        //     }
        // }
        // return false;
        Arrays.sort(arr);
        
        for(int i=0;i<n-2;i++){
            int l=i+1;
            int r=n-1;
            while(l<r){
                int sum=arr[i]+arr[l]+arr[r];
                if(sum==target){
                    return true;
                }else if(sum<target){
                    l++;
                }else{
                    r--;
                }
            }
        }
        return false;
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-10-10 15:40:39
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    public boolean hasTripletSum(int arr[], int target) {
        // code Here
        // int sum=0;
        int n=arr.length;
        // for(int i=0;i<n;i++){
        //     for(int j=i+1;j<n;j++){
        //         for(int k=j+1;k<n;k++){
        //             sum=arr[i]+arr[j]+arr[k];
        //             if(sum==target){
        //                 return true;
        //             }
        //         }
        //     }
        // }
        // return false;
        Arrays.sort(arr);
        
        for(int i=0;i<n-2;i++){
            int l=i+1;
            int r=n-1;
            while(l<r){
                int sum=arr[i]+arr[l]+arr[r];
                if(sum==target){
                    return true;
                }else if(sum<target){
                    l++;
                }else{
                    r--;
                }
            }
        }
        return false;
    }
}
```

*Generated on: 10/11/2026, 6:26:25 AM*