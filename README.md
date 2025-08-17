# Leetcode-9.-Palindrome-Number
# Description
Given an integer x, return true if x is a palindrome, and false otherwise.

# Solution
 A palindrome is a number that reads the same forward and backward
 
Example: 121 -> palindrome, 123 -> not palindrome.

Approach:
1. If x is negative, return False (since negative numbers can't be palindromes).
2. Convert the number into a string and check if it equals its reverse.
3. Alternatively, reverse the integer mathematically without converting to string.
# Algorithm
1. First, check if the number is negative. If it is negative, directly say it’s not a palindrome
2. Keep a copy of the original number, because later you’ll need to compare it with the reversed one.
3. Now, start reversing the number:
4. Take the last digit of the number.
5. Add this digit to a new number (rev) in reverse order.
6. Keep removing digits from the original number one by one (by dividing it by 10).
7. After reversing the entire number, compare it with the original number.
8. If both are the same, the number is a palindrome. Otherwise, it is not a palindrome.
# Code
class Solution:

    def isPalindrome(self, x: int) -> bool:
        reverse =0
        temp =x
        while temp>0:
            remainder = temp % 10
            reverse = (reverse *10) + remainder
            temp = temp // 10
        if x == reverse:
            return True
        else:
            return False

