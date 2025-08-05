class Solution:
    def subsets(self, nums: list[int]) -> list[list[int]]:
        n = len(nums)
        total_subsets = 1 << n
        ans = []
        for val in range(total_subsets):
            subset = []
            for i in range(n):
                if val & (1 << i):
                    subset.append(nums[i])
            ans.append(subset)
        return ans
