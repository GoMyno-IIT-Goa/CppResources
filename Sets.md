<!-- Author: Adarsh Anand -->

## C++ STL Sets

Sets are a type of associative containers in C++ STL Library. Set assures that the elements are unique. Also all the elements in the set are in sorted order.

### Implementation

```cpp
    /*Adarsh Anand*/

    #include <iostream>
    #include <vector>
    using namespace std;
    int main()
    {
        // Creating a set
        set<int> s;

        // Inserting elements in the set
        s.insert(10);
        s.insert(20);
        s.insert(30);
        s.insert(40);
        s.insert(50);

        // Printing the elements of the set (Range bassed for loop)
        for(auto i: s)
            cout << i << " "; // 10 20 30 40 50

        // or 
        for(auto itr = s.begin(); itr != s.end(); itr++) // Iterator
            cout << *itr << " "; // 10 20 30 40 50

        //Accessing first element
        cout << "\nFirst element: " << *s.begin() << endl;// 10

        //Accessing last element
        cout << "Last element: " << *(--s.end()) << endl; // 50

        /*Note s.end() returns an iterator pointing next to the last element of the set.*/

        //Accessing element at index i
        cout << "Element at index i: " << *(s.begin()+i-1) << endl;

        // Size of the set
        cout << "Size of the set: " << s.size() << endl; // 5

        // Checking if the set is empty
        if(s.empty())
            cout << "Set is empty" << endl; // Set is empty
        
        // Checking if the set contains an element
        if(s.find(30) != s.end())
            cout << "Set contains 30" << endl; // Set contains 30

        // Removing an element
        s.erase(30);// Removing 30
        //s = {10, 20, 40, 50}

        // Removing all elements
        s.clear(); // Removing all elements
        //s = {}

        //Upper bound
        cout << "Upper bound: " << *s.upper_bound(30) << endl; // 40

        //Lower bound
        cout << "Lower bound: " << *s.lower_bound(30) << endl; // 10

        //Sort a set in descending order
        reverse(s.begin(), s.end());
        //s = {50, 40, 30, 20, 10}

        

    }

```
