https://leetcode.com/problems/contains-duplicate/description/




```cpp
bool containsDuplicate(vector<int>& nums)
{
    unordered_map<int,int> mp;
    for(int i = 0; i < nums.size(); i++)
    {
        mp[nums[i]]++;
        if(mp[nums[i]] > 1)
            return true;
    }
    return false;
}
```


    There are many data structures commonly used as dynamic sets such as Binary Search Tree and Hash Table. The operations we need to support here are search() and insert(). For a self-balancing Binary Search Tree 
    (TreeSet or TreeMap in Java), search() and insert() are both O(logn) time. For a Hash Table (HashSet or HashMap in Java), search() and insert() are both O(1) on average. Therefore, by using hash table, we can 
    achieve linear time complexity for finding the duplicate in an unsorted array.

    Complexity Analysis

Time complexity: O(n).
We do search() and insert() for n times and each operation takes constant time.

Space complexity: O(n).
The space used by a hash table is linear with the number of elements in it.



