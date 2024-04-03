```c++
vector<int> gradingStudents(vector<int> grades) {
    for(int &grade:grades){
        if(grade>37 && (5-grade%5)<3){
            grade+= 5-grade%5;
        }
    }
    return grades;
}
```