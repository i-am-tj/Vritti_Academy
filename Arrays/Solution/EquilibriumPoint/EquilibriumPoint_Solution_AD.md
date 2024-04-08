```java
class Solution {

    public static int equilibriumPoint(long arr[], int n) 
    {
        if(n==0)
        {
        return -1;
        }
        int flag=0;
        long p[]= new long[n];
        long s[]=new long [n];
        p[1]= arr[1];
        s[n]=arr[n];
        for(int i=2;i<=n;i++)
        {
            p[i]=p[i-1]+arr[i];
            s[n-i-1]=s[n-i+1]+arr[n-i];
        }
        for(int i=2;i<=n-2;i++)
        {
            if(p[i-1]==s[i+1])
            flag=i;
            break;
        }
        if(flag==0)
        return -1;
        else 
        return flag;
    }
}
```
