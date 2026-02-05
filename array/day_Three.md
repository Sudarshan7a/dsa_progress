# Group Anagrams

my solution
class Solution:
def groupAnagrams(self, strs: List[str]) -> List[List[str]]:
if (len(strs)==0):
return [[""]]
arrDict={}
for ele in strs:
alphabets=[0]\*26
for ch in ele:
alphabets[ord(ch)-ord("a")]+=1

            key = tuple(alphabets)
            if key not in arrDict.keys():
                arrDict[key]=[ele]
            else:
                arrDict[key].append(ele)
        return list(arrDict.values())

other solution
sor all the world in the list
next creat a dict
if a sorted word not in key create a key and add the world
if it is in key then just appened the world to the array
return the array of values
