# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Start the Program
2. Use numpy and sys packages
3. Use nested loops to loop through each row and column
4. End the program

## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Prajin S
RegisterNumber: 23012918
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
    if matrix[i][i]==0.0:
        sys.exit('Divide by zero error')
    for j in range(i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
            matrix[j][k]= matrix[j][k]-ratio* matrix[i][k]
x[n-1]= matrix[n-1][n]/ matrix[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]= matrix[i][n]
    for j in range(i+1,n):
        x[i]=x[i]- matrix[i][j]*x[j]
    x[i]=x[i]/matrix[i][i]
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]),end=' ')
```

## Output:
![Screenshot 2023-12-13 181936](https://github.com/Prajin19/Gaussian/assets/144979377/e21b8843-b8e4-44cb-8ed2-62c0565abc63)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

