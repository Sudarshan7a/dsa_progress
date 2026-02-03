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

# Contains Duplicate

my solution
class Solution:
def containsDuplicate(self, nums: List[int]) -> bool:
result = set()
for i in range(len(nums)):
if nums[i] in result:
return True
else:
result.add(nums[i])
return False

other solutions
sol1. sorting
nums.sort() // this will sort the entire array and now we can check if adjacent elements are equal to find duplicates

sol2.
return True if len(set(nums) < len(nums)) else False // check the length of the set after adding all the elements from the list or convering the list, cuz set won't store duplicate elements

# Valid Anagram

my solution 1
class Solution:
def isAnagram(self, s: str, t: str) -> bool:
hashMap = {}
for ele in s:
if ele in hashMap.keys():
hashMap[ele]+=1
else:
hashMap[ele]=1 # print(hashMap)
for ele in t:
if ele in hashMap.keys():
if hashMap[ele]==0:
return False
hashMap[ele]-=1
else:
return False # print(hashMap)
for ele in hashMap.values():
if ele != 0:
return False
return True

my solution 2
alphaFeq = [0] \*26

        for ele in s:
            alphaFeq[ord(ele)-97] +=1
        for ele in t:
            alphaFeq[ord(ele)-97] -=1

        for i in alphaFeq:
            if i != 0:
                return False
        return True

other solution
return True if hashMap of s == hashMap of t else False
