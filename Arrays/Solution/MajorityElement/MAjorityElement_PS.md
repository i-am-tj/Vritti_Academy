```java

 //moore voting algorithm
        int winner=nums[0];
        int vote=1;
        for(int i= 1;i<nums.length;i++)
        {
            if(nums[i]==winner){
                vote++;
            }
            else{
                if(vote<1){
                    winner=nums[i];
                    vote =1;
                }
                else{
                    vote--;
                }
            }
        }
        
        return winner;

```