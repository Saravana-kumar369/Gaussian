# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. import the header files numpy and sys
2. get the number of input
3. get the array of input 
4. perform guassian elimination

## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by:SARAVANA KUMAR M 
RegisterNumber: 212222230133
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
    if a[i][i]==0.0:
        sys.exit
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        
        for k in range (n+1):
            a[j][k]-=ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    
    for j in range(i+1,n):
        x[i]-=a[i][j]*x[j]
        
    x[i]/=a[i][i]
    
for i in range(n):
    print('X%d = %.2f'%(i,x[i]),end=" ")
```

## Output:
![Screenshot 2023-09-19 220905](https://github.com/Saravana-kumar369/Gaussian/assets/117925254/275dd16e-f8aa-4985-9613-b8d2739667fe)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

