# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import the NumPy library
2.Get the coefficient matrix and constant matrix from the user.
3.Apply Gaussian Elimination method to reduce the matrix into row echelon form and find the solution.
4.Display the values of the unknown variables as the output.
## Program:
```
/*
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Hemavarathan S
RegisterNumber: 25005365
'''

import os
os.environ["OPENBLAS_NUM_THREADS"]="1"    
n=int(input())
a=[[0.0 for _ in range(n+1)]for _ in range(n)]
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for K in range(n-1):
    for i in range(K+1,n):
        factor=a[i][K]/a[K][K]
        for j in range(K,n+1):
            a[i][j]-=factor*a[K][j]

x=[0.0]*n
x[n-1]=a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    s=0
    for j in range(i+1,n):
        s+=a[i][j]*x[j]
    x[i]=(a[i][n]-s)  /a[i][i]

for i in range(n):
    print(f"X{i} = {x[i]:.2f}", end=" ") 
*/
```

## Output:
![gaussian elimination]()


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

