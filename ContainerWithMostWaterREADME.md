# leet-day6

_**LeetCode Problem: Container With Most Water**_


**Problem Description**

You are given an integer array height of length n. There are n vertical lines drawn such that the two endpoints of the ith line are (i, 0) and (i, height[i]).

Your task is to find two lines that together with the x-axis form a container, such that the container contains the most water. Return the maximum amount of water the container can store.

Note: You may not slant the container.

Example

Input: height = [1,8,6,2,5,4,8,3,7] 
Output: 49 

Explanation: The above vertical lines are represented by the array [1,8,6,2,5,4,8,3,7]. In this case, the max area of water (blue section) the container can contain is 49.


**Constraints**

n == height.length

2 <= n <= 10^5

0 <= height[i] <= 10^4

**Approach**

We can use the two-pointer approach to find the maximum area. The idea is to start with two pointers, one at the beginning and one at the end of the array. Calculate the area between the two pointers, which is the minimum of the heights multiplied by the distance between the pointers. Move the pointer with the smaller height towards the center, as that could potentially lead to a larger area. Keep updating the maximum area until the pointers meet.

The two-pointer approach ensures that we explore all possible containers without missing any, and the algorithm runs in linear time complexity O(n).

**Steps**

Initialize two pointers left at the beginning of the array and right at the end of the array.

Initialize a variable maxWater to store the maximum area.

While left is less than right, do the following:

a. Calculate the height of the container as the minimum of height[left] and height[right].

b. Calculate the width of the container as right - left.

c. Calculate the area of the container as height * width.

d. Update maxWater to the maximum of maxWater and the current area.

e. If height[left] is less than height[right], increment left by 1; otherwise, decrement right by 1.

Return maxWater as the maximum amount of water the container can store.

_**Complexity Analysis**_

The time complexity of this approach is O(n) as we perform a single pass through the array with the two pointers. The space complexity is O(1) as we use only a constant amount of additional space.

_**Summary**_

The two-pointer approach efficiently finds the maximum area of water that a container can hold, and it is an optimal solution with linear time complexity and constant space complexity.
