///JAVA SOLUTION

```java
class Solution {
   public int largestAltitude(int[] gain) {
        int a[]= new int[gain.length+1];
       a[0]=0;
       a[1]=gain[0];
       for(int i=0;i<gain.length;i++){
           a[i+1]=gain[i]+a[i];
       }

       int res=0;
       for(int i=0;i<a.length;i++){
           if(a[i]>a[res]){
               res=i;
           }
       }
       return a[res];
    }
}
```