<!-- Author : Rohith -->
## GCD

GCD is the greatest common divisor of two numbers. It is also the largest number that divides both numbers. For example, the GCD of $12$ and $18$ is $6$.

```cpp
    /* Rohith */
    #include<bits/stdc++.h>
    using namespace std;

    //Gcd using Euclid's algorithm
    int gcd_using_Euclid_Algorithm(int a, int b) {
        if (b == 0) return a;
        return gcd(b, a % b);
    }

    // We can also compute GCD of 2 numbers using in-built     function
    int gcd_using_in_built_function(int a, int b){
        int ans = __gcd(a, b);
        return ans;
    }

    int main(){
        int a, b;
        cin >> a >> b;
        cout << gcd_using_Euclid_Algorithm(a, b);
        cout << gcd_using_in_built_function(a, b);
        return 0;
    }

```
