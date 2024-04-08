```c++
class Solution {
public:
    int largest(vector<int> &arr, int n) {
        if (n == 0) {
            return INT_MIN;
        }
        
        int maxElement = arr[0];
        
        for (int i = 1; i < n; ++i) {
            if (arr[i] > maxElement) {
                maxElement = arr[i];
            }
        }
        
        return maxElement;
    }
};
```