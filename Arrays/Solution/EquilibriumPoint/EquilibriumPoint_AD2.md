```c++
class Solution {
public:
    int pivotIndex(vector<int>& nums) {
        int n=nums.size();
        int sum=0, leftsum=0;
        for(int i=0;i<n;i++){
            sum=sum+nums[i];
        }
        for(int i=0;i<n;i++){
            sum=sum-nums[i];
            if(leftsum==sum){
                return i;
            }leftsum=leftsum+nums[i];

        }return -1;
    }
};
```