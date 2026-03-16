# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
Read number of unknowns n. Read augmented matrix A[n][n+1]. 2.For i = 0 to n-1 If A[i][i] == 0, stop (division by zero). For j = i+1 to n-1 Find ratio = A[j][i] / A[i][i] For k = 0 to n A[j][k] = A[j][k] - ratio * A[i][k] 3.Back Substitution x[n-1] = A[n-1][n] / A[n-1][n-1] For i = n-2 to 0 x[i] = A[i][n] For j = i+1 to n-1 x[i] = x[i] - A[i][j] * x[j] x[i] = x[i] / A[i][i]
Print the solution vector x[i].


## Program:
```
/*
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Ajithkumar .J
RegisterNumber: 212225040015
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0.0:
        sys.exit("Divide by zero detected!")
    for j in range(i+1,n):
        ratio =a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k] = a[j][k] - ratio * a[i][k] 
            
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i] = x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print(f"X{i} = {x[i]:.2f}", end =' ')
    
*/
```

## Output:
<img width="434" height="315" alt="image" src="https://github.com/user-attachments/assets/6e4b0b2b-a3fd-415e-ba25-584ce345f32f" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

