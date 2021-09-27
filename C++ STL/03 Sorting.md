<!-- Author: Adarsh Anand -->
```cpp
## C++ Sorting

We can sort the elements of an vector using the following algorithms:

a. Selection sort

- The selection sort algorithm is a simple sorting algorithm that works by repeatedly finding the minimum element (considering ascending order) from unsorted part and putting it at the beginning.

b. Bubble sort

- The bubble sort algorithm is a simple sorting algorithm that works by repeatedly swapping the adjacent elements if they are in wrong order.

c. Generic Sort STL

- The generic sort STL algorithm is a sorting algorithm that uses a comparison predicate to compare two elements.

Sort in : ascending order, descending order,custom order

### Implementation

```cpp
    /*Adarsh Anand*/

    #include <iostream>
    #include <vector>
    using namespace std;
    int main()
    {
        vector<int> v;
        v.push_back(5);
        v.push_back(1);
        v.push_back(2);
        v.push_back(6);
        v.push_back(4);
        v.push_back(3);

        // v= {5,1,2,6,4,3}

        // Bubble Sort
        for(int i=0;i<v.size();i++)
        {
            for(int j=0;j<v.size()-i-1;j++)
            {
                if(v[j]>v[j+1])
                {
                    int temp=v[j];
                    v[j]=v[j+1];
                    v[j+1]=temp;
                }
            }
        }

        // v= {1,2,3,4,5,6}

        // Selection Sort
        for(int i=0;i<v.size();i++)
        {
            int min=i;
            for(int j=i+1;j<v.size();j++)
            {
                if(v[j]<v[min])
                {
                    min=j;
                }
            }
        }

        // v= {1,2,3,4,5,6}

        // General sorting using STL
        sort(v.begin(),v.end());

        // v= {1,2,3,4,5,6}

        // General sorting using STL in reverse order
        sort(v.begin(),v.end(),greater<int>());

        // v= {6,5,4,3,2,1}

        vector<pair<int,int>> vp;
        vp.push_back(make_pair(5,1));
        vp.push_back(make_pair(1,2));
        vp.push_back(make_pair(2,3));
        vp.push_back(make_pair(6,4));
        vp.push_back(make_pair(4,5));

        // vp= {{5,1},{1,2},{2,3},{6,4},{4,5}}

        // General sorting using STL
        sort(vp.begin(),vp.end());

        // vp= {{1,2},{2,3},{4,5},{5,1},{6,4}}

        // General sorting using STL in reverse order
        sort(vp.begin(),vp.end(),greater<pair<int,int>>());

        // vp= {{6,4},{5,1},{4,5},{2,3},{1,2}}


        // Sorting using custom function
        bool cmp(pair<int,int> a,pair<int,int> b)
        {
            return a.first<b.first;
        }
        sort(vp.begin(),vp.end(),cmp});

        // vp= {{1,2},{2,3},{4,5},{5,1},{6,4}}

    }

STL sort() function is a sorting algorithm that uses a comparison predicate to compare two elements.

Time Complexity: O(n log n) 
Most sorting algorithms are O(n log n) in the worst case.

Similarly we can use Sorting algorithms in other data types such as vector<pair<int, int>> , map<int, int> and multimap<int, int> , set<int> and multiset<int> etc.
```
