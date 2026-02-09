# Remove Element

my solution
class Solution:
def removeElement(self, nums: List[int], val: int) -> int:
n= len(nums)
if n==0:
return 0
k=0
for ele in nums:
if ele!=val:
nums[k]=ele
k+=1

        return k
