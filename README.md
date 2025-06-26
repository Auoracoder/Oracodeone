# A leet code problem (1st)
class Solution(object):
    def sortColors(self, num):
        n = len(num)
        low = 0
        mid = 0
        high = n - 1
        while mid <= high:
            if num[mid] == 0:
                num[low], num[mid] = num[mid] , num[low]
                low +=1
                mid +=1
            elif num[mid] == 1:
                mid +=1
            else:
                num[mid], num[high] = num[high] , num[mid]
                high-=1
