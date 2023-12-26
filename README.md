# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.first, we want to import numpy,then import sys,assume a variable  
2. for gaussion elimination method, we want to make 2nd and 3d column zero
3. for that we want to  make a range according to our program output 
4. then print the program with correct from then the output will display

## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: SHARAN.G
RegisterNumber: 23002031
'''
import sys
import numpy as np
n=int(input())
matrix=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
         matrix[i][j]=int(input())
for i in range(n):
    if matrix[i][j] == 0.0:
        sys.exit("Divide by zero error")
    for j in range(i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
            matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
x[n-1]=matrix[n-1] [n]/matrix[n-1] [n-1]
for i in range(n-2,-1,-1):
    x[i]=matrix[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-matrix[i][j]*x[j]
    x[i]=x[i]/matrix[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=" ")

```

## Output:
![Screenshot 2023-12-26 151816](https://github.com/Sharan1731/Gaussian/assets/144980172/aa21d73a-002a-4642-9849-23a11a328b11)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

