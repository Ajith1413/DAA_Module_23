# EX 5C Kadane's Algorithm
## DATE:
## AIM:
To write a python program to find the maximum contiguous subarray.


## Algorithm
1. Initialize current and max sums
2. Loop through the array starting from index 1
3. Update current sum to max of current element or current sum + element
4. Update max sum if current sum is greater
5. Return the maximum sum found  

## Program:
~~~

Developed by: AJITH KUMAR A
Register Number:212223230009

def maxSubArraySum(a,size):
    #####################  Add your Code here #############
    #Start here
    max_so_far = a[0]
    max_ending_here = 0
    for i in range(0, size):
        max_ending_here = max_ending_here + a[i]
        if max_ending_here < 0:
            max_ending_here = 0
        elif (max_so_far < max_ending_here):
            max_so_far = max_ending_here
              
    return max_so_far
    #End here
n=int(input())  
a =[] #[-2, -3, 4, -1, -2, 1, 5, -3]
for i in range(n):
    a.append(int(input()))
print("Maximum contiguous sum is", maxSubArraySum(a,n))
~~~

## Output:

![image](https://github.com/user-attachments/assets/5c400abe-6a84-4bc5-8a08-171785b2c33a)

## Result:
Thus the program was executed successfully for finding the maximum contiguous sum of subarray..
