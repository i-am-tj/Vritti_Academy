```C++
class Solution {
    public boolean isMonotonic(int[] nums) {
        int n=nums.length;
        if(nums[n-1]>=nums[0]){
            for(int i=0;i<n-1;i++){
                if(nums[i+1]<nums[i]){
                    return false;
                }
            }
        }
        else if(nums[n-1]<=nums[0]){
            for(int i=0;i<n-1;i++){
                if(nums[i+1]>nums[i]){
                    return false;
                }
            }
        }
        return true;
    }
}
```