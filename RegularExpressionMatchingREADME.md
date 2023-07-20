# leet-day6

_**Regular Expression Matching**_


Given an input string s and a pattern p, this algorithm implements regular expression matching with support for '.' and '*' where:

. matches any single character.

* matches zero or more of the preceding element.

  
The goal is to determine whether the pattern p can match the entire input string s (not partial matching).


Input 

s = "aa"
p = "a*"

Output

true



Explanation: "." means "zero or more () of any character (.)".

Constraints

1 <= s.length <= 20

1 <= p.length <= 20

s contains only lowercase English letters.

p contains only lowercase English letters, '.', and '*'.

It is guaranteed that for each appearance of the character '*', there will be a previous valid character to match.


**Approach and Algorithm**

The algorithm uses dynamic programming (DP) to solve the problem efficiently. It creates a DP table to keep track of the matching status for each combination of characters in s and p. The DP table is filled based on the characters in s and p, and the patterns of '.' and '*'. By using DP, redundant computations are avoided, resulting in improved runtime.


**Time Complexity**

The time complexity of the algorithm is O(m * n), where m is the length of string s, and n is the length of pattern p.

**Space Complexity**

The space complexity is O(m * n) as well, due to the DP table.
