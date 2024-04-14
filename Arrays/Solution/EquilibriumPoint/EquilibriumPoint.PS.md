```java
class Solution {
    public int pivotIndex(int[] nums) {
        int n = nums.length;
        int preffix[]=new int [n];
        int suffix[]=new int [n];

         preffix[0]=nums[0];
         suffix[n-1]=nums[n-1];

         for(int i =1;i<n;i++)
         {
            preffix[i]=nums[i]+preffix[i-1];
         }

         for(int i =n-2;i>=0;i--)
         {
            suffix[i]=nums[i]+suffix[i+1];
         }

         for(int i= 0;i<n;i++){
            if(suffix[i]==preffix[i]){
                return i;
            }
         }
         return -1;
    }
}
```