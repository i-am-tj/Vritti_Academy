//java solution  

```java
class Solution
{ 
    public static int findSum(int A[],int N) 
    {
        //code here
        int min=A[0];
        int max=A[0];
        for(int i=0;i<N;i++)
        {
            if(A[i]>max){
                max=A[i];
            }
            
            else if(A[i]<min){
                min=A[i];
            }
        }
        
        return max+min;
    }
}
```