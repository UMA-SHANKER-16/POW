This is my improved solution to the house painting problem, where the goal is to paint every house with one of the available colors without painting two neighboring houses the same color — and doing it with the minimum total cost.

After trying a brute-force approach and realizing it was too slow, I applied dynamic programming.

The basic approach is to move through the houses one by one, and for each house, calculate the cheapest way to paint it based on what we’ve already decided for the previous one.

But instead of checking all colors for every house, I optimized further by only keeping track of two values from the previous step: the smallest and the second smallest costs. If we can reuse the cheapest one, we do that. If not (because of same color), we go with the second cheapest.

This greatly reduces the number of comparisons and speeds things up a lot.

Time complexity becomes O(n * k), and space stays constant since we only track a few values at each step.
