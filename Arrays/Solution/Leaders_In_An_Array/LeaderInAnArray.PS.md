```java
class Solution{
    //Function to find the leaders in the array.
    static ArrayList<Integer> leaders(int arr[], int n){
        // Your code here
        ArrayList<Integer> result = new ArrayList<Integer>();
        
        int current_leader=arr[n-1];
        
        result.add(current_leader);
        
        for(int i = n-2;i>=0;i--)
        {
            if(arr[i]>=current_leader)
            {
                current_leader=arr[i];
                result.add(current_leader);
            }
        }
        
        
         ArrayList<Integer> revArrayList = new ArrayList<Integer>();
        for (int i = result.size() - 1; i >= 0; i--) 
        {
                revArrayList.add(result.get(i));
        }
        
        return  revArrayList;
        
    }
}
```