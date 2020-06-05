# Arrays

+ [Two Sum](#two-sum)
+ [3Sum](#3sum)
+ [Subarray Sum Equals k](#subarray-sum-equals-k)

## Two Sum

https://leetcode.com/problems/two-sum/

```python

```

## 3Sum

https://leetcode.com/problems/3sum/

```python
def threeSum(self, nums: List[int]) -> List[List[int]]:
    result = []
    nums.sort()
    for i in range(len(nums)):
        if (i != 0) and (nums[i] == nums[i - 1]):
            continue
        left = i + 1
        right = len(nums) - 1
        while (left < right):
            if not (nums[i] + nums[left] + nums[right]):
                result.append([nums[i], nums[left], nums[right]])
                left += 1
                while (left < right) and (nums[left] == nums[right]):
                    left += 1
            elif (nums[i] + nums[left] + nums[right] < 0):
                left += 1
            else:
                right -= 1

    n = []
    for i in result:
        if not n or i != n[-1]:
            n.append(i)
    return n

```

## Subarray Sum Equals k

https://leetcode.com/problems/subarray-sum-equals-k/

```python
def subarraySum(self, nums: List[int], k: int) -> int:
    hash_sum = {}
    index_sum = 0
    count = 0
    for i in nums:
        index_sum += i
        check_sum = index_sum - k
        if index_sum == k:
            count += 1
        if check_sum in hash_sum:
            count += hash_sum[check_sum]
        if index_sum not in hash_sum:
            hash_sum[index_sum] = 1
        else:
            hash_sum[index_sum] += 1
    return count

```
