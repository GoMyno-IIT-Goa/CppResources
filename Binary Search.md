<!-- Author: Aniket Akshay Chaudhri -->

## Binary Search

Binary Search makes use of benefits of a sorted array. The array is sorted first and then the required element is compared with middle element.
Three cases can arise:

1. Middle element > Required element : we search for the number in the left part of the array

2. Middle element < Required element : we search for the number in the right part of the array

3. Middle element = Required element : return because element is found

The process keeps on iterating by breaking into halves and each time comparing with the middle element, until element is found. 
If we reach first/last element of array and element is not found yet, return -1 (element not found)


### Implementation

```cpp

int BinarySearch(int arr[], int left, int right, int element){
    if (left <= right){
        int mid = (left + right) / 2;
        if (arr[mid] == element) return mid;
        else if (arr[mid] > element) return BinarySearch(arr, left, mid-1, element);
        else (arr[mid] < element) return BinarySearch(arr, mid+1, right, element);
    }
    return -1;
}



```

**Complexity**

- **Time:** O(log₂ N)
- **Space:** O(1)




<!-- Question Links Yet to be updated. These are random ones -->

## Questions

|                |                                                                                                                                                            |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|Searching and Sorting|[Find a fixed point(Value equal to index) in a given array](https://practice.geeksforgeeks.org/problems/value-equal-to-index-value1330/1)                                                                                                                                                                 |
|                     |[Search in a rotated sorted array](https://leetcode.com/problems/search-in-rotated-sorted-array/)                                                                                                                                                                                |
|                     |[Square root of an integer](https://practice.geeksforgeeks.org/problems/count-squares3649/1)                                                                                                                                                                              |
|                     |[Maximum and minimum of an array using minimum number of comparisions](https://practice.geeksforgeeks.org/problems/middle-of-three2926/1)                                                                                                                                                                            |
|                     |[Optimum location of a point to minimize total distance](https://www.geeksforgeeks.org/optimum-location-point-minimize-total-distance/#:~:text=We%20need%20to%20find%20a,set%20of%20points%20is%20minimum.&text=In%20above%20figure%20optimum%20location,is%20minimum%20obtainable%20total%20distance.)|
|                     |[Find the repeating and the missing](https://practice.geeksforgeeks.org/problems/find-missing-and-repeating2512/1)                                                                                                                                                                 |
|                     |[Find the majority element](https://practice.geeksforgeeks.org/problems/majority-element/0)                                                                                                                                                                               |
|                     |[Searching in an array where adjacent differ by atmost k](https://www.geeksforgeeks.org/searching-array-adjacent-differ-k/)                                                                                                                                                                             |
|                     |[Find a pair with given difference](https://practice.geeksforgeeks.org/problems/find-pair-given-difference/0)                                                                                                                                                                     |
|                     |[Find 4 elements that sum to a given value](https://practice.geeksforgeeks.org/problems/find-all-four-sum-numbers/0)                                                                                                                                                                      |
|                     |[Maximum sum such that no 2 elements are adjacent](https://practice.geeksforgeeks.org/problems/stickler-theif/0)                                                                                                                                                                                 |
|                     |[Count triplet with sum smaller than given value](https://practice.geeksforgeeks.org/problems/count-triplets-with-sum-smaller-than-x5549/1)                                                                                                                                                     |


