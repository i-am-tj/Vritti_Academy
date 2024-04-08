```java
class Solution {
    int print2largest(int arr[], int n)
    {
        if(n<2)
        {
            return -1;
        }
        
        int max=arr[0];
        int second_max=Integer.MIN_VALUE;
      
        for(int i=1;i<n;i++)
        {
            if(arr[i]>max)
            max=arr[i];
        }
        for(int i=0;i<n;i++)
         {
             if (arr[i]>second_max && arr[i]<max)
             second_max=arr[i];
           
         }
         if (second_max==Integer.MIN_VALUE)
         return -1;
         else 
         return second_max;
         
     
    }
}
```