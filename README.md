# Find-the-duplicate-number
class Solution(object):
    def findDuplicate(self, nums):
        # Phase 1: Detect cycle
        slow = nums[0]
        fast = nums[nums[0]]
        while slow != fast:
            slow = nums[slow]
            fast = nums[nums[fast]]
        slow = 0
        while slow != fast:
            slow = nums[slow]
            fast = nums[fast]

        return slow

        
