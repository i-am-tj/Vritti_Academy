```C++
class Solution {
public:
  bool arraySortedOrNot(int arr[], int n) {
    bool k=true;
    for(int i=1;i<n;i++){
      if(arr[i]<arr[i-1])
        k= false;
    }
    return k;
  }
};
```