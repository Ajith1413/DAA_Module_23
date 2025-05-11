# EX 5B Coin Change Problem
## DATE:
## AIM:
To compute the fewest number of coins that we need to make up the amount given.


## Algorithm
1. Initialize a dp array 
2. Base case (0 amount needs 0 coins)
3. Loop through each coin
4. Update dp for all amounts ≥ coin 
5. Return result (or -1 if not possible)  

## Program:
~~~
Developed by: 
Register Number:


class Solution(object):
    def coinChange(self, coins, amount):
        ####################      Add your Code Here ###########
        #End here
        if amount == 0 :
            return 0
        if min(coins) > amount:
            return -1
        dp = [-1 for i in range(0, amount + 1)]
        for i in coins:
            if i > len(dp) - 1:
                continue
            dp[i] = 1
            for j in range(i + 1, amount + 1):
                if dp[j - i] == -1:
                    continue
                elif dp[j] == -1:
                    dp[j] = dp[j - i] + 1
                else:
                    dp[j] = min(dp[j], dp[j - i] + 1)
        return dp[amount]
    #End here
      
ob1 = Solution()
n=int(input())
s=[]
amt=int(input())
for i in range(n):
    s.append(int(input()))
print(ob1.coinChange(s,amt))
~~~

## Output:

![image](https://github.com/user-attachments/assets/bd74e3e4-0526-4a57-b326-40889f090c76)

## Result:
Thus the program was executed successfully for finding the minimum number of coins required to make amount.
