<!-- Author: Adarsh Anand -->

## C++ STL Maps

Maps are associative containers that store elements in a mapped fashion. Each element has a key value and a mapped value. No two mapped values can have same key values. Maps are implemented using hash tables. They are fast for lookup and insertion. They are slow for deletion. They are also slow for iteration. There are three types of maps: `std::map`, `std::multimap`, `std::unordered_map`.

### Implementation

```cpp
    /*Adarsh Anand*/

    #include <iostream>
    #include <vector>
    using namespace std;
    int main()
    {
        // Creating a map
        map<int,int> m;

        // Inserting elements
        m.insert(pair<int,int>(1,10));
        m.insert(pair<int,int>(2,20));
        m.insert(pair<int,int>(3,30));
        m.insert(pair<int,int>(4,40));
        m.insert(pair<int,int>(5,50));

        // Printing the elements
        for(auto i=m.begin();i!=m.end();i++)
        {
            cout<<i->first<<" "<<i->second<<endl;
        }
        //m = { {1,10}, {2,20}, {3,30}, {4,40}, {5,50} };

        // Inserting elements with same key
        m.insert(pair<int,int>(1,100));

        // Printing the elements
        for(auto i=m.begin();i!=m.end();i++)
        {
            cout<<i->first<<" "<<i->second<<endl;
        }
        //m = { {1,100}, {2,20}, {3,30}, {4,40}, {5,50} }; Value overwritten

        // Begin Iterator and End Iterator
        cout<<"Begin Iterator: "<<m.begin()->first<<" "<<m.begin()->second<<endl;// 1 100

        cout<<"End Iterator: "<<m.end()->first<<" "<<m.end()->second<<endl;//5 50

        // Erasing elements
        m.erase(m.begin());
        m.erase(m.begin());
        //m = { {3,30}, {4,40}, {5,50} };

        // Size of the map
        cout<<"Size of the map: "<<m.size()<<endl;//5

        // Check map empty or not
        if(m.empty())
        {
            cout<<"Map is empty"<<endl;
        }

        // Clearing the map
        m.clear();
        //m = {};

        // Erase an element by key
        m.erase(1);
        //m = {{2,20}, {3,30}, {4,40}, {5,50} };

        // Erase an element by key and value
        m.erase(2,20);
        //m = { {1,10}, {3,30}, {4,40}, {5,50} };

        // Map count
        cout<<"Count of key 1: "<<m.count(1)<<endl;//1

        // Map find
        cout<<"Find key 1: "<<m.find(1)->first<<" "<<m.find(1)->second<<endl;//1 10

        // Upper bound and lower bound
        cout<<"Upper bound of key 3: "<<m.upper_bound(3)->first<<" "<<m.upper_bound(3)->second<<endl;//4 40

        cout<<"Lower bound of key 3: "<<m.lower_bound(3)->first<<" "<<m.lower_bound(3)->second<<endl;//3 30

        // Compare two maps
        map<int,int> m1  = { {1,10}, {2,20}, {3,30}, {4,40}, {5,50} };
        map<int,int> m2  = { {1,10}, {2,20}, {3,30}, {4,40}, {5,60} };

        if(m1 == m2)
        {
            cout<<"Maps are equal"<<endl;
        }

        // Map swap
        m1.swap(m2);
        //m1 = { {1,10}, {2,20}, {3,30}, {4,40}, {5,60} };
        //m2 = { {1,10}, {2,20}, {3,30}, {4,40}, {5,50} };

        // Get value by key
        cout<<"Get value by key 1: "<<m1.at(1)<<endl;//10
        cout<<"Get value by key 1: "<<m1[1]<<endl;//20
    }

```
