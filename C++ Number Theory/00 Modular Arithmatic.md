## Modular Arithmatic

Modular arithmatic is a technique for solving problems that involve arithmetic on numbers that are not necessarily in the range of a normal integer.
Quite often, the numbers involved are very large, and the arithmetic is done modulo a large number.

```cpp

//Modular Arithmatic functions

#include<bits/stdc++.h>
using namespace std;

int modular_addition(int a, int b, int mod)
{
    int result = ((a%mod) + (b%mod)) % mod;
    return result;
}

int modular_subtraction(int a, int b, int mod)
{
    int result = ((a%mod) - (b%mod) + mod) % mod;
    return result;
}

int modular_multiplication(int a, int b, int mod)
{
    int result = ((a%mod) * 1LL * (b%mod)) % mod;
    // Here 1LL is multiplied to avoid overflow
    return result;
}

int modular_division(int a, int b, int mod)
{
    int result = (a%mod) * 1LL *(pow(b, mod-2)%mod) % mod;     /* You can also compute b^(mod-2) using Binary             exponentation a*b^(mod-2) % mod */
    return result;
}

int main(){
    int a, b, mod;
    cin>> a >> b >> mod;
    cout<< modular_addition(a, b, mod) << "\n";
    cout<< modular_subtraction(a, b, mod) << "\n";
    cout<< modular_multiplication(a, b, mod) << "\n";
    cout<< modular_division(a, b, mod) << "\n";
    return 0;
}

```