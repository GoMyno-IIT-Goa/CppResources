<<!-- Author : Rohith -- >>

## Binary Exponentiation

Binary exponentiation is a method of computing the power of a number by repeated squaring. It is a very efficient way to compute the power of a number. Time complexity is O(log n).

```cpp
/* Rohith */

#include<bits/stdc++.h>
using namespace std;

// Calculating a^b in logarithmic time

int binary_exponentiation(int a, int b,int mod){
    int ans = 1;
    while (b)
    {
        if(b%2==1){
            ans = (ans * 1LL * a)%mod;
        }
        a = (a * 1LL * a)%mod;
        b = b>>1;
    }
    return ans;
}

int main(){
    int a, b;
    cin >> a >> b;
    cout << binary_exponentiation(a, b) << "\n";
    return 0;
}

```
