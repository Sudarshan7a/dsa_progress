# Concatenation of Array

my solution

class Solution:
def getConcatenation(self, nums: List[int]) -> List[int]:
n = len(nums)
ans=[0]*(n*2)
for i in range(n):
ans[i]=nums[i]
ans[i+n]=nums[i]
return ans

other solutions

sol1. using '+' operator
return nums + nums

sol2. using extends method
nums.extend(nums)
return nums

sol3. using '\_' operator
return nums \* 2
