```java
class Solution {
    public int[] productExceptSelf(int[] nums) {
        int n = nums.length;
        int pre[] = new int[n];
        int suf[] = new int[n];
        int answer[] = new int[n];
        pre[0] = nums[0];
        suf[n - 1] = nums[n - 1];

        for (int i = 1; i < n; i++)
        {
            pre[i] = pre[i - 1] * nums[i];
        }
        
        for (int i = n - 2; i >= 0; i--)
        {
            suf[i] = suf[i + 1] * nums[i];
        }

        for (int i = 0; i < n; i++)
        {
            if(i==0)
            {
               answer[i]=suf[1];
            }
            else if(i==n-1)
            {
                answer[i]=pre[n-2];
            }
            else 
            {
            answer[i] = pre[i-1] * suf[i+1];
            }
        }

        return answer;
        
    }
}
```