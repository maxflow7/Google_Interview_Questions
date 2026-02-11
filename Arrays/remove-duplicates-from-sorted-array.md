
https://leetcode.com/problems/remove-duplicates-from-sorted-array/description/

```cpp
class Solution {
public:
    int removeDuplicates(vector<int>& nums) {
        int insertIndex = 1;
        for (int i = 1; i < nums.size(); i++) {
            // We skip to next index if we see a duplicate element
            if (nums[i - 1] != nums[i]) {
                // Storing the unique element at insertIndex index and
                // incrementing the insertIndex by 1
                nums[insertIndex] = nums[i];
                insertIndex++;
            }
        }
        return insertIndex;
    }
};
```

Complexity Analysis
Let N be the size of the input array.

Time Complexity: O(N), since we only have 2 pointers, and both the pointers will traverse the array at most once.

Space Complexity: O(1), since we are not using any extra space.
