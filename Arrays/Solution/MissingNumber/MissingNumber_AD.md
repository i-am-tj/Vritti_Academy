```java
class Solution {
    public int missingNumber(int[] nums)
    {
        int p=0;
        int n=nums.length;
        int sum=0;
        int A_sum=0;
        for(int i=0;i<n;i++)
        {
            sum+=i;
            A_sum+=nums[i];
            

        }
        return (sum+n) - A_sum;
        
    }
}
```