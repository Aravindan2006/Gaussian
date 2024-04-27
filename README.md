# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
Step1 : Import the module numpy and assign numpy as np
and import sys.

Step 2: Create an variable named 'a' and use np.zeros for the matrix values by first list as first row and so on.

Step 3: Using the for loop method to solve the program.

Step 4: Print the gaussion elimination .
## Program:
```
'''
Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: ARAVINDAN D
RegisterNumber: 212223240012
'''
import numpy as np
import sys

n= int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)

for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0.0:
        sys.exit('Divide by zero detected!')
    for j in range(i+1,n):
        ratio = a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio * a[i][k]
            
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]= x[i] - a[i][j]*x[j]
        
    x[i]= x[i]/a[i][i]
    
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]),end=' ')

```

## Output:
![Screenshot 2024-04-27 084736](https://github.com/Aravindan2006/Gaussian/assets/151760062/14bf611a-e83a-414b-9eff-be652a94c03b)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

