This file contains my optimized solution to the problem of finding how many continuous days of calorie burn sum up to a specific target (k).

Instead of checking every possible subarray, I used a more efficient technique based on prefix sums and a HashMap.

The key idea is to track the running total (prefix sum) as we iterate through the list. For each step, we check if (current sum - target) has already appeared. If yes, that means we found a valid streak, and we increase the count accordingly.

The HashMap keeps track of how many times each prefix sum has occurred. We also handle the special case where the streak starts from index 0 by initializing the map with sum 0 appearing once.

This approach only takes one pass over the array, so it runs in O(n) time and uses O(n) space.
