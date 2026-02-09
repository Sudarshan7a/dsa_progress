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

# Majority Element

my solution
class Solution:
def majorityElement(self, nums: List[int]) -> int:
hashmap={}
for ele in nums:
hashmap[ele] = hashmap.get(ele, 0)+1
max=0
eleIndex = 0
freqArr=list(hashmap.values()) # print(hashmap) # print(freqArr)
for i in range(len(freqArr)):
if freqArr[i]>max:
max=freqArr[i]
eleIndex=i

        # print(eleIndex)

        val = list(hashmap.keys())
        # print(val)
        return val[eleIndex]

other solution

sol1 By sorting
if a ele is occuring more thatn n/2 time where n is the total number of elements defenatly the val ele will be at middle after sorted
so if we sort we can get it by taking the middle element

sol2 by frequency
create a hashmap
next iterate through it like
for key,value in hashmap.items():
check if the value(frequency) of the element/value is grater than n
return the key then else 0

sol3 Moore Voting Algorithm
this algo will help to keep most occuring element in the array
we have to have a count and a candidate
me codded
class Solution:
def majorityElement(self, nums: List[int]) -> int:

        count = 0
        candidate = 0
        for ele in nums:
            if count == 0:
                candidate = ele
                count+=1
            elif ele!=candidate:
                count-=1
            else:
                count+=1
            # print(count, candidate)
        return candidate

# Design HashSet

my solution
class LinkL:
def **init**(self,key):
self.key=key
self.next=None

class MyHashSet:

    def __init__(self):
        self.hs=[LinkL(0) for i in range(10**4)]

    def add(self, key: int) -> None:
        idx = key%10**4
        cur = self.hs[idx]
        while cur.next:
            if cur.next.key==key:
                return
            cur=cur.next
        cur.next=LinkL(key)

    def remove(self, key: int) -> None:
        idx = key%10**4
        cur = self.hs[idx]
        while cur.next:
            if cur.next.key==key:
                cur.next= cur.next.next
                return
            cur = cur.next

    def contains(self, key: int) -> bool:
        idx = key%10**4
        cur = self.hs[idx]
        while cur.next:
            if cur.next.key==key:
                return True
            cur = cur.next

        return False

# Your MyHashSet object will be instantiated and called as such:

# obj = MyHashSet()

# obj.add(key)

# obj.remove(key)

# param_3 = obj.contains(key)
