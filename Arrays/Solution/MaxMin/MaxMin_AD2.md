```C++
class Solution
{
   public:
    int findSum(int A[], int N)
    {
    	int maxi=A[0],mini=A[0];
    	for(int i=1;i<N;i++){
    	    maxi=max(maxi,A[i]);
    	    mini=min(mini,A[i]);
    	}return maxi+mini;
    }

};
```