## Modular Arithmatic

Modular arithmatic is a technique for solving problems that involve arithmetic on numbers that are not necessarily in the range of a normal integer.
Quite often, the numbers involved are very large, and the arithmetic is done modulo a large number.

```cpp

//Modular Arithmatic functions

int modular_addition(int a, int b, int mod)
{
    int result = (a + b) % mod;
    return result;
}

int modular_subtraction(int a, int b, int mod)
{
    int result = (a - b) % mod;
    return result;
}

int modular_multiplication(int a, int b, int mod)
{
    int result = (a * b) % mod;
    return result;
}

int modular_division(int a, int b, int mod)
{
    int result = a*(pow(b, mod-2)) % mod; //a*b^(mod-2) % mod
    return result;
}

```