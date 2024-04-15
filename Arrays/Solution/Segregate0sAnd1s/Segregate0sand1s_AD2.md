```c++
class Solution {
public:
    void segregate0and1(int arr[], int n) {
        int i = 0, j = n - 1;
        
        while (i < j) {
            while (arr[i] == 0 && i < j) {
                i++;
            }
            
            while (arr[j] == 1 && i < j) {
                j--;
            }
            
            if (i < j) {
                swap(arr[i], arr[j]);
                i++;
                j--;
            }
        }
    }
};
```