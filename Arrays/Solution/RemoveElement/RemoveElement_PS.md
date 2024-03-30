JAVA SOLUTION

class Solution {
    public int removeElement(int[] nums, int val) {
        int A[]=new int[nums.length];
        int k = 0;

        for(int i = 0;i<nums.length;i++)
        {
            if(val!=nums[i])
            {
              A[k]=nums[i];
              k++;
            }

        }

        for(int i = 0;i<nums.length;i++){
            nums[i]=0;
        }

        for(int i = 0;i<k;i++){
            nums[i]=A[i];
        }


        return k;
    }
}