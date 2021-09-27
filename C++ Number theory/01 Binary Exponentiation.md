## Binary Exponentiation

Binary exponentiation is a method of computing the power of a number by repeated squaring. It is a very efficient way to compute the power of a number. Time complexity is O(log n).

```cpp

// Calculating a^b in logarithmic time

int binary_exponentiation(int a, int b,int mod){
    int ans = 1;
    while (b)
    {
        if(b%2==1){
            ans = (ans*a)%mod;
        }
        a = (a*a)%mod;
        b = b>>1;
    }
    return ans;
}

```
