## 01. Most Frequent in Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/most-frequent-element-in-an-array/1)

### Problem Description

**Task:** You are given an integer array arr[], return the element which occurs maximum times. If multiple such elements exists return the maximum element.Example: Input: arr[] = [1, 2, 2, 2, 4, 1]Output: 2Explanation: 2 is most frequent element of this array with 3 occurrences.Input: arr[] = [1, -5, 8, 1]Output: 1Explanation: 1 is most frequent element of this array with 2 occurrences.Input: arr[] = [3, 0, 0, 3, 8]Output: 3Explanation: 0 and 3 are two most frequent elements of this array. 3 is the maximum one.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-14 12:02:41
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public int mostFreqEle(int[] arr) {
        // code here
        // int max=0;
        // int ans=-1;
        // int n=arr.length;
        // for(int i=0;i<n;i++){
        //     int count=0;
        //     for(int j=0;j<n;j++){
        //         if(arr[i]==arr[j]){
        //         count++;
        //         }
        //     }
        //     if(count==max){
        //         if(arr[i]>ans){
        //             ans=arr[i];
        //         }
        //     }
        //     if(count>max){
        //         max=count;
        //         ans=arr[i];
        //     }
            // 1,1,2,2,2,4
        // }
        // return ans;
        
        Arrays.sort(arr);
        int max=-1;
        int ans=arr[0];
        int n=arr.length;
        int count=1;
        for(int i=1;i<n;i++){
            if(arr[i]==arr[i-1]){
                count++;
            }else{
                count=1;
            }
            if(count>=max){
                max=count;
                ans=arr[i];
            }
        }
        return ans;
        
    }
}
```

*Generated on: 10/14/2026, 12:10:59 PM*