```java

        int i =0;
        int j = height.length-1;
        int area=0;
        int check=0;
        while(j>i){
            area=(j-i)*Math.min(height[i],height[j]);
            check=Math.max(check,area);
            if(height[i]>height[j]){
                j--;
            }
            else{
                i++;
            }

        }
        return check;
```