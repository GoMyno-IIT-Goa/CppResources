<<!-- Author : Rohith -->>

## Sieve Technique

Sieve is a technique used to find all the prime in numbers upto 10^7 in O(log(logN)) Time complexity.

It is not only used for finding whether a number is prime, but also to find the lowest prime factor prime factor of a number and much more

### Implementation

```cpp
/* Rohith */
#include<bits/stdc++.h>
using namespace std;
const int N = 2e5+10;
vector<bool> sieve(N,true);
vector<int> lowest_prime_factor(N);
int main(){
    sieve[0] = sieve[1] = false;
    for(int i=2;i*i<N;++i){
        if(sieve[i]){
            for(int j=i*i;j<N;j+=i){
                sieve[j] = false;
            }
        }
    }
    
// The above vector will contain lowest prime factor of the number
for(int i=0;i<N;++i){
    lowest_prime_factor[i] = i;
}
for(int i=2;i*i<N;++i){
    if(lowest_prime_factor[i]==i){
        for(int j=i*i;j<N;j+=i){
            lowest_prime_factor[j] = i;
        }
    }
}
    return 0;
}

