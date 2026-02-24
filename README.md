# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. import numpy 
2. import sys
3. solve using for loop
4. print the output

## Program:
```python
*/
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: D.sanjutha
RegisterNumber: 212225240136




import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0:
        sys.exit('Divide by zero detected!')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]), end=' ')
```*/

## Output:

<img width="1195" height="828" alt="Screenshot 2026-02-24 221157" src="https://github.com/user-attachments/assets/d6d706f4-37a7-41ae-bdf0-b4b2c103372d" />

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

