## 01. Smallest Greater in Whole Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/smallest-greater-elements-in-whole-array2751/1?utm_source=gfg&utm_medium=article&utm_campaign=bottom_sticky_on_article)

### Problem Description

**Task:** Given an array arr[], for each element, find the smallest element in the array that is strictly greater than it. If no such element exists, return -10000000 for that position. Return the resulting array.

#### Examples

##### Example 1

- **Input:**
```text
arr[] = [13, 6, 7, 12]
```
- **Output:**
```text
-10000000 7 12 13 Explanation: Here, at index 0, 13 is the greatest value in given array and no other array element is greater from 13. So at index 0 we fill '-10000000'.
```

##### Example 2

- **Input:**
```text
arr[] = [6, 3, 9, 8, 10, 2, 1, 15, 7]
```
- **Output:**
```text
7 6 10 9 15 3 2 -10000000 8Explanation: Here, at index 7, 15 is the greatest value in given array and no other array element is greater from 15. So at index 7 we fill '-10000000'.
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n log n)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-16 10:16:05
- **Status:** Correct
- **Marks:** 2

```java
// class Solution {

//     public ArrayList<Integer> greaterElement(int[] arr) {
//         // code here
//         ArrayList<Integer> ans=new ArrayList<>();
//         int n=arr.length;
//         for(int i=0;i<n;i++){
//             int min=Integer.MAX_VALUE;
//             for(int j=0;j<n;j++){
//                 if(arr[i]<arr[j] && arr[j]<min){
//                     min=arr[j];
//                 }
//             }if(min==Integer.MAX_VALUE){
//                 ans.add(-10000000);
//             }
//             else{
//                 ans.add(min);
//             }
//         }
        
        
//         return ans;
//     }
// }
class Solution {
    public ArrayList<Integer> greaterElement(int[] arr) {
        // code here
        ArrayList<Integer> ans=new ArrayList<>();
        int[] sort=new int[arr.length];
        for(int i=0;i<arr.length;i++){
            sort[i]=arr[i];
        }

        Arrays.sort(sort);
        for(int i=0;i<arr.length;i++){
            int large=arr[i];
            boolean found=false;
            for(int j=0;j<sort.length;j++){
                if(sort[j]>large){
                    ans.add(sort[j]);
                    found=true;
                    break;
                }
            }
            if(!found){
                ans.add(-10000000);
            }
        }
        return ans;
    }
}
```

*Generated on: 10/16/2026, 10:16:32 AM*