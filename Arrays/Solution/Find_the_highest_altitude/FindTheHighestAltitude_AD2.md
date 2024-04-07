```C++
class Solution {
public:
    int largestAltitude(vector<int>& gain) {
        int k=0,p=0;
        for(int i=0;i<gain.size();i++){
            p=p+gain[i];
            k=max(k,p);
        }return k;
    }
};

```