<<!-- Author : Rohith -->>

## Factorial and Combinatrics

In maths based problems like arrangements and selection, we need to calculate Ncr and factorial of a number. 
We will store the factorial of numbers in a vector of integers.
We will make a function to calculate Ncr.

### Implementation

```cpp
/* Rohith */
#include<bits/stdc++.h>
using namespace std;

int ncr(int n, int r, vector<int> &factorial, int mod){
    int numerator = factorial[n];
    int denominator = (1LL*factorial[n-r]*factorial[r])%mod;
    int ans = modular_division(numerator, denominator);
    // Please refer to modular arithmatic for the function
    return ans; 
}

int main(){
    int N = 2e5 + 10;
    int mod = 1e9 + 7;
    // Storing factorial of numbers in a vector
    vector<int> factorial(N,1);
    for(int i=2; i<N; ++i){
        factorial[i] = (1LL * factorial[i-1] * i)% mod;
    }
    int n, r;
    cin >> n >> r;
    cout << ncr(n, r, factorial, mod) << "\n";
    return 0;
}