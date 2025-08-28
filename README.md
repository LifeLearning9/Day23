**Day23:Given two strings s and t, determine if they are isomorphic.
Two strings are isomorphic if the characters in s can be replaced to get t, with the mapping being one-to-one and consistent.**

**Test Cases**
1. Input: egg   add
  Output: true
2. Input: foo  bar
   Output: false

**Intuition**
1. We need to ensure:
2. Every character in s always maps to the same character in t.
3. No two characters in s map to the same character in t.
4. We can track the mapping using two arrays of size 256 (since ASCII characters are enough).
   a. mapS[c1] stores which character c1 from s maps to in t.
   b. mapT[c2] stores which character c2 from t maps to in s.
5. If any inconsistency is found, the strings are not isomorphic.

**Algorithm** 
1. If the lengths of s and t differ → return false.
2. Create two arrays of size 256, initialized to -1, to store mappings.
3. Loop through both strings character by character.
4. If both mappings are unused, create a new mapping.
5. If a mapping already exists, check consistency.
6. If inconsistent → return false.
7. After loop ends → return true.
   
 **Complexity Analysis**
Time Complexity: O(n)
Space Complexity: O(1),
Time Complexity: O(n), where n = length of the strings (single pass).

Space Complexity: O(1)
