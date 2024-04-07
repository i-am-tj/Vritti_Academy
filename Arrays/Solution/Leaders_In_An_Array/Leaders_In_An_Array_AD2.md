```C++
class Solution{
public:
        vector<int> leaders(int a[], int n){
        vector<int> result;
        int Max = a[n - 1];
        result.push_back(Max);
        
        for(int i = n - 2; i >= 0; i--){
            if(a[i] >= Max){
                Max = a[i];
                result.push_back(Max);
            }
        }
        
        reverse(result.begin(), result.end());
        
        return result;
    }
};
```