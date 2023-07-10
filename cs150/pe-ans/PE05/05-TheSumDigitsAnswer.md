// Given a non-negative int n, return the sum of its digits recursively (no loops). 

// Note that mod (%) by 10 yields the rightmost digit (126 % 10 is 6), while divide (/) by 10 removes the rightmost digit (126 / 10 is 12).
// * sumDigits(126) → 9
// * sumDigits(49) → 13
// * sumDigits(12) → 3

```cpp
int sumDigits(int n)
{
   if (n == 0) return 0;
   else return n % 10 + sumDigits(n / 10);
}
```

// https://codecheck.io/files/2303032408c7ux8fg4f8iw346eui24ktz0u