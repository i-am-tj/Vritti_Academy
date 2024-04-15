```java
class Solution
{
    long minValueToBalance(long a[] ,int n)
    {
        long first=0;
        long second=0;
        
        for(int i = 0;i<n/2;i++)
        {
            first = first + a[i];
        }
        
        for(int i = n-1;i>=n/2;i--)
        {
            second = second + a[i];
        }
        
    if(first>=second)
    {
        return first-second;
    }
    
    return second-first;

    }
}
```