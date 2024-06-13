class Solution:
    def climbStairs(self, n: int) -> int:
        if n == 1:
            return 1
        if n == 2:
            return 2
        x = [0]*(n+1)
        x[1] = 1
        x[2] = 2
        for i in range (3, n+1):
            x[i] = x[i - 1]+x[i - 2]
        return x[n]
