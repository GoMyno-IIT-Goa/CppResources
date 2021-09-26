
## Greedy Algorithm

Greedy is an algorithmic paradigm that builds up a solution piece by piece, always choosing the next piece that offers the most obvious and immediate benefit. Greedy algorithms are used for optimization problems.

At every step, we can make a choice that looks best at the moment, and we get the optimal solution of the complete problem. 

If a Greedy Algorithm can solve a problem, then it generally becomes the best method to solve that problem as the Greedy algorithms are in general more efficient than other techniques like Dynamic Programming.

### Example - Activity Selection

Activity Selection Problem is one of the most famous Greedy problem. The problem statement
reads "Given n events with their starting and ending times, find a
schedule that includes as many events as possible. It is not possible to select an
event partially. For example, consider the following events:"

<center>

| Event | Starting Time | Ending Time |
|-------|---------------|-------------|
| A     | 1             | 3           |
| B     | 2             | 5           |
| C     | 3             | 9           |
| D     | 6             | 8           |

</center>

In this example, maximum 2 events, Event B and D can be selected.

The idea is to always select the next possible event that ends as early as
possible.

It turns out that this algorithm always produces an optimal solution. The
reason for this is that it is always an optimal choice to first select an event that
ends as early as possible. After this, it is an optimal choice to select the next
event using the same strategy, etc., until we cannot select any more events.

One way to argue that the algorithm works is to consider what happens if we
first select an event that ends later than the event that ends as early as possible.
Now, we will have at most an equal number of choices how we can select the next
event. Hence, selecting an event that ends later can never yield a better solution,
and the greedy algorithm is correct.

### Example - Counting Coins

This problem is to count to a desired value by choosing the least possible coins and the greedy approach forces the algorithm to pick the largest possible coin. If we are provided coins of ₹ 1, 2, 5 and 10 and we are asked to count ₹ 18 then the greedy procedure will be −

- **1** − Select one ₹ 10 coin, the remaining count is 8
- **2** − Then select one ₹ 5 coin, the remaining count is 3
- **3** − Then select one ₹ 2 coin, the remaining count is 1
- **4** − And finally, the selection of one ₹ 1 coins solves the problem

Though, it seems to be working fine, for this count we need to pick only 4 coins. But if we slightly change the problem then the same approach may not be able to produce the same optimum result.

For the currency system, where we have coins of 1, 7, 10 value, counting coins for value 18 will be absolutely optimum but for count like 15, it may use more coins than necessary. For example, the greedy approach will use 10 + 1 + 1 + 1 + 1 + 1, total 6 coins. Whereas the same problem could be solved by using only 3 coins (7 + 7 + 1)

Hence, we may conclude that the greedy approach picks an immediate optimized solution and may fail where global optimization is a major concern.

Most networking algorithms use the greedy approach.
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


