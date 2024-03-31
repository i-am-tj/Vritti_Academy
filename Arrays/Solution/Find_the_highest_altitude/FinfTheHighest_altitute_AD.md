```java
class Solution
 {
    public int largestAltitude(int[] gain) 
    {
        int alt[] = new int[gain.length+1];
        alt[0]=0;
        for(int i=1;i<=gain.length;i++)
            {
                alt[i]=alt[i-1]+gain[i-1];
            }
            int max=alt[0];
            for(int i=0;i<alt.length;i++)
            {
                if(max<alt[i])
                max=alt[i];
            }
       return max;
    }  
}
```