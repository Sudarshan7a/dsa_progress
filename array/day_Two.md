# Longest Common Prefix

my solution
class Solution:
def longestCommonPrefix(self, strs: List[str]) -> str:
if len(strs) == 0:
return ""

        prefix = strs[0]
        pre_len= len(prefix)

        for i in range(1,len(strs)):
            while strs[i].find(prefix)!=0:
                pre_len-=1
                prefix=prefix[0:pre_len]
                if prefix=="":
                    return ""
        return prefix

other solution
Approach 2: Vertical scanning
Algorithm
Imagine a very short string is the common prefix at the end of the array. The above approach will still do S comparisons. One way to optimize this case is to do vertical scanning. We compare characters from top to bottom on the same column (same character index of the strings) before moving on to the next column.

Implementation
class Solution:
def longestCommonPrefix(self, strs: List[str]) -> str:
if strs == None or len(strs) == 0:
return ""
for i in range(len(strs[0])):
c = strs[0][i]
for j in range(1, len(strs)):
if i == len(strs[j]) or strs[j][i] != c:
return strs[0][0:i]
return strs[0]
