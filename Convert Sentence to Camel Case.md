## 01. Convert Sentence to Camel Case

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/convert-sentence-to-camel-case/1)

### Problem Description

**Task:** Given a sentence s, remove all spaces and convert it to Camel Case. In Camel Case, words are joined without spaces, the first word is converted to lowercase, and each subsequent word starts with an uppercase letter.Note: It is guaranteed that s does not contain leading or trailing spaces.Examples:Input: s = "I got intern at geeksforgeeks"Output: "iGotInternAtGeeksforgeeks"Explanation: All spaces are removed and each word starts with a capital letter, except the first word which retains its original capitalization.Input: s = "here comes the garden"Output: "hereComesTheGarden"Explanation: Spaces are removed and each word after the first is capitalized.Input: s = "coding is fun"Output: "codingIsFun"Explanation: Spaces are removed, the first word retains its original case, and each subsequent word starts with a capital letter.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-23 10:46:42
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    public String convertToCamelCase(String s) {
        // code here
        StringBuilder str=new StringBuilder();
        boolean status=true;
        for(int i=0;i<s.length();i++){
            char ch=s.charAt(i);
            if(i==0){
                str.append(ch);
            }
            else if(ch==' '){
                status=false;
            }else{
                if(status==false){
                    ch=Character.toUpperCase(ch);
                    str.append(ch);
                    status=true;
                }else{
                    str.append(ch);
                }
            }
        }
        return str.toString();
    }
}
```

*Generated on: 10/23/2026, 10:47:09 AM*