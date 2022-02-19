<!-- Author: Adarsh Anand -->

## C++ Searching

We can use the STL `find()` function to search for an element in a container. Linear search is a simple but inefficient algorithm.

But we can do better. Binary search is a more efficient algorithm. It is also called **sequential search**. Unlike linear search, binary search is a **logarithmic** algorithm.

Used for sorted containers, binary search is much faster than linear search.

### Implementation 

```cpp
    /*Adarsh Anand*/

    #include <iostream>
    #include <vector>
    using namespace std;
    int main()
    {
        vector<int> v = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};

        auto it = find(v.begin(), v.end(), 5);
        if (it != v.end())
            cout << "Found 5 at position " << it - v.begin() << endl;
        else
            cout << "5 not found" << endl;
        // Found 5 at position 4

        // Binary search for an element in a sorted vector
        int key = 5;
        int bin_search(vector<int> v, int key){
            int low = 0;
            int high = v.size() - 1;
            while (low <= high)
            {
                int mid = (low + high) / 2;
                if (v[mid] == key)
                {
                    cout << "Found " << key << " at position " << mid << endl;
                    break;
                }
                else if (v[mid] < key)
                    low = mid + 1;
                else
                    high = mid - 1;
            }
        }

        cout<<bin_search(v, key); // Output: Found 5 at position 5

        // Inbuilt binary search function
        int key = 5;
        cout<<binary_search(v.begin(), v.end(), key); // Output: true

        // Lower bound and upper bound
        int key = 5;
        //  Lower bound gives the first element in the sorted vector that is greater than or equal to the key.
        auto lb = lower_bound(v.begin(), v.end(), key);
        // Upper bound gives the first element in the sorted vector that is strictly greater than the key.
        auto ub = upper_bound(v.begin(), v.end(), key);

        cout << "Lower bound: " << *lb << endl;// Output: Lower bound: 5
        cout << "Upper bound: " << *ub << endl; // Output: Upper bound: 6


    }

Similar to binary search, lower_bound and upper_bound are useful for finding the first element in a sorted vector that is greater than or equal to a key and the first element in a sorted vector that is strictly greater than a key.

Similarly we can use searching in other data types such as vector<pair<int, int>> , map<int, int> and multimap<int, int> , set<int> and multiset<int> etc.

Time complexity of binary search is O(log n) and only used for sorted containers.

```
