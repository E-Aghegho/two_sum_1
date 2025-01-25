# LeetCode Problem: Two Sum

### Problem Description

Given an input array and a target value, we are tasked with finding two numbers in the array that sum up to the target. We should return their indices.

**Example:**  
Input: `[2, 1, 5, 3]`, Target: `9`  
Output: Indices `[0, 3]` (since `2 + 7 = 9`).

We are guaranteed that exactly one solution exists, and we don’t need to worry about multiple solutions or not finding a solution.

---

### Naive Solution: Brute Force

A simple but inefficient approach is to check every combination of two numbers and see if they sum up to the target. This solution has a time complexity of O(n²).

**Steps:**

1. Start with the first element and check every combination that includes it by scanning through the rest of the array.
2. If no match is found, move to the next element and repeat.
3. Return the indices of the two numbers that sum to the target.

```python
def two_sum_bruteforce(nums, target):
    for i in range(len(nums)):
        for j in range(i + 1, len(nums)):
            if nums[i] + nums[j] == target:
                return [i, j]
            ```

