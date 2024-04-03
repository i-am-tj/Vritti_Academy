```c++
class Solution {
public:
  void reverseNums(vector<int>& nums, int start, int end){
    if (nums.empty() || start < 0 || end >= nums.size() || start >= end)
      return;
    while(start<end){
      int temp = nums[end];
      nums[end] = nums[start];
      nums[start] = temp;
      start++;
      end--;
    }
  }

  void rotate(vector<int>& nums, int k) {
    int n = nums.size();
    k %= n;
    reverseNums(nums, 0, n - k - 1);
    reverseNums(nums, n - k, n - 1);
    reverseNums(nums, 0, n - 1);
  }

};
```