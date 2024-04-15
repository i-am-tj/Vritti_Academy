```c++
vector<int> gradingStudents(vector<int> v) {
    for(int &i:v){
        if(i>37 && (5-i%5)<3){
            i=i+ 5-i%5;
        }
    }
    return v;
}
```