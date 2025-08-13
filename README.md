
 
# 🚀 3Sum Closest

**LeetCode Problem:** [3Sum Closest](https://leetcode.com/problems/3sum-closest/)  
**Difficulty:** Medium  
**Language:** Python  
**Approach:** Sorting + Two Pointers

---

## 🧠 Problem Statement

Given an integer array `nums` and an integer `target`, find three integers in `nums` such that the sum is closest to `target`.  
Return the sum of the three integers.  
You may assume that each input would have exactly one solution.

---

## 🧪 Example

```python
Input: nums = [-1, 2, 1, -4], target = 1  
Output: 2  
Explanation: The sum that is closest to the target is 2 (-1 + 2 + 1 = 2).
```
## 🧮 Algorithm
1. Sort the array `nums` to enable two-pointer traversal.
2. Initialize a variable `closest` to store the closest sum found so far.
3. Loop through each index `i` from `0` to `len(nums) - 3`:
   - Set two pointers: `left = i + 1` and `right = len(nums) - 1`.
   - While `left < right`:
     - Calculate `total = nums[i] + nums[left] + nums[right]`.
     - If `abs(total - target) < abs(closest - target)`, update `closest = total`.
     - If `total < target`, increment `left`.
     - If `total > target`, decrement `right`.
     - If `total == target`, return `target` immediately (exact match).
4. After all iterations, return the value of `closest`.

## Complexity
Time Complexity: O(n²)
- Sorting takes O(n log n)
- Outer loop runs O(n) times
- Inner loop (two pointers) runs O(n) times per iteration

Space Complexity: O(1)
- No extra space used beyond a few variables

