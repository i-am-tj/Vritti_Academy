```c++
class Solution {
public:
  vector<int> twoSum(vector<int>& nums, int target) {
    vector<int> numsCopy(nums.begin(), nums.end());
    sort(nums.begin(), nums.end());
    int left = 0, right = nums.size() - 1;
    while (left < right) {
      int sum = nums[left] + nums[right];
      if (sum < target) {
        left++;
      } else if (sum > target) {
        right--;
      } else {
        int index1 = -1, index2 = -1;
        for (int i = 0; i < numsCopy.size(); ++i) {
          if (numsCopy[i] == nums[left] && index1 == -1) {
            index1 = i;
          } else if (numsCopy[i] == nums[right]) {
            index2 = i;
          }
        }
        return {index1, index2};
      }
    }
    return {-1, -1};
  }
};
```