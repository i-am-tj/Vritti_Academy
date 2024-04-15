```java
class Solution {
    int print2largest(int arr[], int n) {
        // code here
        int first = Integer. MIN_VALUE;
        int second =Integer. MIN_VALUE;
        
        for(int i = 0;i<n;i++)
        {
            if(arr[i]>first)
            {
                second = first;
                first=arr[i];
            }
            else if((arr[i] > second && arr[i] != first))
            {
                
                    second = arr[i];
                
            }
        }
        
        if (second==Integer. MIN_VALUE){
            return -1;
        }
        return second;
    }
}
```