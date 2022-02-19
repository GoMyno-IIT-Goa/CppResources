<!-- Author: Adarsh Anand -->

## C++ STL Vectors

Vectors are same as dynamic arrays with the ability to resize itself automatically when an element is inserted or deleted, with their storage being handled automatically by the container.

### Implementation

```cpp
    /*Adarsh Anand*/

    #include <iostream>
    #include <vector>
    using namespace std;
    int main()
    {
        // Create a vector of integers
        vector<int> v;
        v.push_back(1);
        v.push_back(2);
        v.push_back(3);
        v.push_back(4);
        v.push_back(5);

        // Prints 1 2 3 4 5
        for(int i=0; i<v.size(); i++)
        {
            cout<<v[i]<<" ";
        }

        //Size of vector
        cout<<"\nSize of vector: "<<v.size()<<endl; // 5

        //Begin and end of vector
        auto it = v.begin();
        cout<<"Begin of vector: "<<*it<<endl; // 1
        it = v.end();
        cout<<"End of vector: "<<*(--it)<<endl; // 5

        /*Note - v.end() returns an iterator pointing next to the last element of the vector.*/

        //Inserting an element at the end of vector
        v.push_back(6);
        // v = {1, 2, 3, 4, 5, 6}

        //Inserting an element at the beginning of vector
        v.insert(v.begin(), 0);
        // v = {0, 1, 2, 3, 4, 5, 6}

        //Inserting an element at the given index
        v.insert(v.begin()+2, 7);
        // v = {0, 1, 7, 2, 3, 4, 5, 6}

        //Delete an element from the end of vector
        v.pop_back();
        // v = {1, 2, 3, 4, 5}

        // Sort the vector
        sort(v.begin(), v.end());
        // v = {1, 2, 3, 4, 5}

        //Sort the vector in descending order
        sort(v.begin(), v.end(), greater<int>());
        // v = {5, 4, 3, 2, 1}

        //Access front element
        cout<<"Front element: "<<v.front()<<endl; // 1

        //Access back element
        cout<<"Back element: "<<v.back()<<endl; // 5

        //Access element at index 2
        cout<<"Element at index 2: "<<v[2]<<endl; // 3

        //Erase element at index 2
        v.erase(v.begin()+2);
        // v = {1, 2, 4, 5}

        //Clear vector
        v.clear();
        // v = {}

        //swap two vectors
        vector<int> v1 = {1, 2, 3, 4, 5};
        vector<int> v2 = {6, 7, 8, 9, 10};
        v1.swap(v2);
        // v1 = {6, 7, 8, 9, 10}
        // v2 = {1, 2, 3, 4, 5}

        //Check if vector is empty
        if(v1.empty())
        {
            cout<<"Vector is empty"<<endl;
        }

```
