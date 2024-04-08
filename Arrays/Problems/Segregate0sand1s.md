
# [Segregate 0s and 1s](https://www.geeksforgeeks.org/problems/segregate-0s-and-1s5106/1)

Given an array of length `n` consisting of only 0's and 1's in random order. Modify the array in-place to segregate 0s on the left side and 1s on the right side of the array.

## Example

```
**Input:**
n = 5
arr[] = {0, 0, 1, 1, 0}
```
```
**Output:**
{0, 0, 0, 1, 1}
```

**Explanation:**  
After segregating all 0's on the left and 1's on the right, the modified array will be {0, 0, 0, 1, 1}.


## Your Task

You don't need to read input or print anything. Your task is to complete the function `segregate0and1(arr[], n)` which takes `arr[]` and `n` as input parameters and modifies `arr[]` in-place without using any extra memory.

## Constraints

- 1 ≤ n ≤ 10^6
- 0 ≤ arr[i] ≤ 1

## Expected Time Complexity

O(n)

## Expected Auxiliary Space

O(1)
