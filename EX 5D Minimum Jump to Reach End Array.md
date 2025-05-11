# EX 5D Minimum Jump to Reach End Array
## DATE:
## AIM:
To write a python program for finding the minimum number of jumps needed to reach end of the array using Dynamic Programming.


## Algorithm
1. Initialize DP array with infinity except first index
2. Loop through the array from start to second last index
3. Check reachable positions from current index
4. Update minimum jumps to reach position j
5. Return minimum jumps to reach the last index   

## Program:
~~~
Developed by: AJITH KUMAR A
Register Number: 212223230009

def minJumps(arr, n):
    ##########  Add your code here ##############
    #Start here
    jumps = [0 for i in range(n)]
    if (n == 0) or (arr[0] == 0):
        return float('inf')
    jumps[0] = 0
    for i in range(1, n):
        jumps[i] = float('inf')
        for j in range(i):
            if (i <= j + arr[j]) and (jumps[j] != float('inf')):
                jumps[i] = min(jumps[i], jumps[j] + 1)
                break
    return jumps[n-1]
    #End here
arr = []
n = int(input()) #len(arr)
for i in range(n):
    arr.append(int(input()))
print('Minimum number of jumps to reach','end is', minJumps(arr,n))
 
 
~~~

## Output:

![image](https://github.com/user-attachments/assets/8bd04026-dd46-45e0-8075-20bac88c435c)

## Result:
Thus the program was executed successfully for finding the minimum number of jumps to reach end.
