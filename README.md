# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. input matrix dimensions and initialize the argumented matrix and solution vector.
2. populate the argumented matrix with the user inputs.
3. Back substitute to compute solution values for the variables.
4. print the solution vector formatter to two decimal places.

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Abdul Rahim M
RegisterNumber: 25015778
*/
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Abdul Rahim M
RegisterNumber: 25015778
'''
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i] 
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio * a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-1,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print("X%d = %0.2f"%(i,x[i]), end=' ')

## Output:

<img width="1484" height="824" alt="image" src="https://github.com/user-attachments/assets/0a06ce30-837d-44bd-bdeb-3b93856b2bb6" />


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

