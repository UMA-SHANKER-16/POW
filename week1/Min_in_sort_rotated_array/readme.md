This problem is about finding the smallest element in a sorted array that has been rotated at some pivot point. A rotation splits the array into two parts while keeping the overall sorted structure intact.

Example:
Original: [0, 1, 2, 4, 5, 6, 7]  
Rotated: [4, 5, 6, 7, 0, 1, 2]  
→ The minimum value here is 0.

To solve this efficiently, I used a binary search-based method. Instead of scanning the entire array, we can take advantage of the sorted order.

The idea is to compare the middle element with the rightmost one:
- If the middle value is greater than the right, it means the smallest value must be in the right half.
- If the middle value is less than or equal to the right, then the smallest could still be in the left half (including mid), so we move the right pointer.

We keep doing this until the search space is narrowed down and the minimum element is found.

Time complexity is O(log n), as we reduce the range in half with each step.  
Space complexity is O(1), since no extra space is needed beyond a few variables.
