## 01. Maximum Sum Subarray of Size K

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/max-sum-subarray-of-size-k5313/1)

### Problem Description

**Task:** Given an array of integers arr[] and a number k. Return the maximum sum of a subarray of size k.Note: A subarray is a contiguous part of any given array.Examples:Input: arr[] = [100, 200, 300, 400], k = 2

#### Examples

##### Example 1

- **Output:**
```text
400
```
- **Explanation:** arr_3 = 400, which is maximum.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (C++)

- **Submitted:** 2026-09-27 16:27:20
- **Status:** Correct
- **Marks:** 0

```cpp
class Solution {
  public:
    int maxSubarraySum(vector<int>& arr, int k) {
        // code here
        int sum=0;
        int index=0;
        for(int i=0;i<k;i++){
            sum=sum+arr[i];
        }
        int maxS=sum;
        for(int j=k;j<arr.size();j++){
            sum=sum+arr[j]-arr[index];
            maxS=max(maxS,sum);
            index++;
        }
        return maxS;
    }
};
```

#### Solution 2 (C++)

- **Submitted:** 2026-09-25 11:27:15
- **Status:** Correct
- **Marks:** 2

```cpp
// class Solution {
//     public int maxSubarraySum(int[] arr, int k) {
//         // Code here
//         int l=Integer.MIN_VALUE;
//         int sum=0;
//         int ans=0;
//         for(int i=0;i<arr.length;i++){
//             int[] temp= new int[k];
//             int z=0;
//             temp[z]=arr[i];
//             for(int j=i+1;j<arr.length;j++){
//                 if(temp.length==k){
//                     sum=0;
//                     // sum=Arrays.stream(temp).sum();
//                     for(int x=0;x<k;x++){
//                         sum=sum+temp[x];
//                     }
                    
//                     sum=Math.max(l, sum);
//                     ans=sum;
//                     break;
//                 }else{
//                     z++;
//                     temp[z]=arr[j];
//                 }
//             }
//         }
//         return ans;
        
//     }
// }
class Solution {
    public int maxSubarraySum(int[] arr, int k) {
        // Code hereint max
        int sum=0;
        int index=0;
         for(int i=0;i<k;i++){
            sum+=arr[i];
         }
         int max=sum;
         for(int j=k;j<arr.length;j++){
             sum=sum+arr[j]-arr[index];
             index++;
             max=Math.max(max,sum);
         }
         return max;
        
    }
}
```

*Generated on: 10/18/2026, 4:37:54 PM*