# leet-day6

_**Palindrome Number**_

Given an integer x, determine if it is a palindrome.

A palindrome is a number that reads the same backward as forward.

Example

Input: x = 121 
Output: true

Explanation: 121 is a palindrome because it reads the same from left to right and right to left.


Input: x = -121 
Output: false

Explanation: -121 is not a palindrome as it reads as -121 from left to right and 121- from right to left.


Input: x = 10  
Output: false

Explanation: 10 is not a palindrome as it reads 01 from right to left.


Input: x = 12321 
Output: true

Explanation: 12321 is a palindrome because it reads the same from left to right and right to left.


**Constraints**

The input integer x will be in the range [-231, 231 - 1].


**Approach**

To check if the number is a palindrome, we can reverse the digits of the positive number and then compare the reversed number with the original number. If they are the same, the number is a palindrome.

We need to be careful of negative numbers and numbers with trailing zeros, as they cannot be palindromes.

The C++ solution provided uses a long long data type to handle large numbers without encountering an overflow error.


_**Complexity Analysis**_

The time complexity for this approach is O(log(x)), where x is the input integer. The space complexity is O(1) as we are using a fixed amount of extra space to store the reversed number.
