## 01. Count Pairs Divisible By K

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/count-pairs-in-array-divisible-by-k/1)

### Problem Description

**Task:** Given an array arr[] and positive integer k, count total number of pairs in the array whose sum is divisible by k.

#### Examples

##### Example 1

- **Input:**
```text
arr[] = [2, 2, 1, 7, 5, 3], k = 4
```
- **Output:**
```text
5
```
- **Explanation:** There are five pairs possible whose sum is divisible by '4' i.e., (2, 2), (1, 7), (7, 5), (1, 3) and (5, 3).

##### Example 2

- **Input:**
```text
arr[] = [5, 9, 36, 74, 52, 31, 42], k = 3
```
- **Output:**
```text
7
```
- **Explanation:** There are seven pairs whose sum is divisible by 3, i.e, (9, 36), (9,42), (74, 52), (36, 42), (74, 31), (31, 5) and (5, 52).

#### Constraints

- **1.** `1 ≤ |arr| ≤ 5*10⁴ 1 ≤ arr[i] ≤ 10⁶ 1 ≤ k ≤ 5*10⁴`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(k)

### Accepted Solutions (4)

#### Solution 1 (Java)

- **Submitted:** 2026-10-18 16:09:49
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public int countKdivPairs(int[] arr, int k) {
        // code here
        // int count=0;
        // for(int i=0;i<arr.length;i++){
        //     for(int j=i+1;j<arr.length;j++){
        //     while(j<arr.length){
        //         int sum=arr[i]+arr[j];
        //         if(sum%k==0){
        //             cout++;
        //             j++;
        //         }
        //     }
        // }
        // return count;
        int n=arr.length;
        int[] freq=new int[k];
        int count=0;
        for(int i=0;i<n;i++){
            int val=arr[i]%k;
            if(val<0){
                val+=k;
            }
            int req=(k-val)%k;
            count+=freq[req];
            freq[val]++;
        }
        return count;
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-10-18 15:59:33
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public int countKdivPairs(int[] arr, int k) {
        // code here
        // int count=0;
        // for(int i=0;i<arr.length;i++){
        //     for(int j=i+1;j<arr.length;j++){
        //     while(j<arr.length){
        //         int sum=arr[i]+arr[j];
        //         if(sum%k==0){
        //             cout++;
        //             j++;
        //         }
        //     }
        // }
        // return count;
        int n=arr.length;
        int[] freq = new int[k];
                int count = 0;

                for (int i = 0; i < n; i++) {
                    int rem = arr[i] % k;

                    if (rem < 0) {
                        rem += k;
                    }

                    int need = (k - rem) % k;

                    count += freq[need];
                    freq[rem]++;
                }

                return count;
    }
}
```

#### Solution 3 (Java)

- **Submitted:** 2026-09-24 15:49:32
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public int countKdivPairs(int[] arr, int k) {
       
        
        int[] freq=new int[k];
        int count=0;
        for(int i=0;i<arr.length;i++){
            int rem=arr[i]%k;
            int req=(k-rem)%k;
            count+=freq[req];
            freq[rem]++;
        }
        return count;
    }
}
```

#### Solution 4 (Java)

- **Submitted:** 2026-09-24 15:49:01
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    public int countKdivPairs(int[] arr, int k) {
        // code here
        // int count=0;
        // for(int i=0;i<arr.length;i++){
        //     for(int j=i+1;j<arr.length;j++){
        //         int sum=arr[i]+arr[j];
        //         if(sum%k==0){
        //             count++;
        //         }
        //     }
        // }
        // return count;
        // int low=0;
        // int high=arr.length-1;
        // while(low<high){
        //     while(high>low){
        //     high=arr.length-1;
        //      int sum=arr[low]+arr[high];
        //     if(sum%k==0){
        //         count++;
        //         high--;
        //     }else{
        //         high--;
        //     }
        //     }
        //     low++;
        // }
        // return count;
        
        int[] freq=new int[k];
        int count=0;
        for(int i=0;i<arr.length;i++){
            int rem=arr[i]%k;
            int req=(k-rem)%k;
            count+=freq[req];
            freq[rem]++;
        }
        return count;
    }
}
```

*Generated on: 10/18/2026, 4:10:26 PM*