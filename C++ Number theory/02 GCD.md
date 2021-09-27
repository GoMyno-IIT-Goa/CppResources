## GCD

GCD is the greatest common divisor of two numbers. It is also the largest number that divides both numbers. For example, the GCD of $12$ and $18$ is $6$.

```cpp
    //Gcd using Euclid's algorithm
    int gcd(int a, int b) {
        if (b == 0) return a;
        return gcd(b, a % b);
    }

```
