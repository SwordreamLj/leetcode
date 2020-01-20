class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        mp = dict()
        for i, num in enumerate(nums):
            sub_num = target - num
            if mp.get(sub_num, None) != None:
                return [mp[sub_num], i]
            mp[num] = i
        return []