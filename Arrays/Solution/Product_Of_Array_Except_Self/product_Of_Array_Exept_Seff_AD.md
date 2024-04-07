```java
class Solution {
    public int[] productExceptSelf(int[] nums) {
        int p[] = new int[nums.length];
        int s[] = new int[nums.length];
        int arr[] = new int[nums.length];
        p[0] = nums[0];
        s[nums.length - 1] = nums[nums.length - 1];

        for (int i = 1; i < nums.length; i++)
        {
            p[i] = p[i - 1] * nums[i];
        }System.out.println(Arrays.toString(p));
        
        for (int i = nums.length - 2; i >= 0; i--)
        {
            s[i] = s[i + 1] * nums[i];
        }System.out.println(Arrays.toString(s));
     
        for (int i = 0; i < nums.length; i++)
        {
            if(i==0)
            {
                arr[i]=s[1];
            }
            else if(i==nums.length-1)
            {
                arr[i]=p[nums.length-2];
            }
            else if(i!=0 && i!=nums.length-1)
            {
            arr[i] = p[i-1] * s[i+1];
            }
        }
           return arr;
       
     }      
 }
 ```