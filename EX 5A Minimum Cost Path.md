# EX 5A Minimum Cost Path
## DATE:
## AIM:
To write a Python program using A Naive recursive implementation of Minimum Cost Path Problem.




## Algorithm
1. Create a 2D list tc of size R x C to store the total minimum cost for each cell.
2. Assign the starting cell
3. Only one way to reach each cell in the first column 
4. Only one way to reach each cell in the first row 
5. For all other cells, choose the minimum cost from the top, left, or diagonal
 

## Program:
~~~
Developed by: AJITH KUMAR A
Register Number:  212223230009

R = int(input())
C = int(input())
def minCost(cost, m, n):
    tc = [[0 for x in range(C)] for x in range(R)]
    tc[0][0] = cost[0][0]
    for i in range(1, m+1):
        tc[i][0] = tc[i-1][0] + cost[i][0]
    for j in range(1, n+1):
        tc[0][j] = tc[0][j-1] + cost[0][j]
    for i in range(1, m+1):
        for j in range(1, n+1):
            tc[i][j] = min(tc[i-1][j-1], tc[i-1][j], tc[i][j-1]) + cost[i][j]
 
    return tc[m][n]
 
cost = [[1, 2, 3],
        [4, 8, 2],
        [1, 5, 3]]
print(minCost(cost, R-1, C-1))
~~~

## Output:
![image](https://github.com/user-attachments/assets/8232b3a0-f665-4cde-8bc3-2f725010a41c)

## Result:
Thus the above program was executed successfully for finding the minimum cost.
