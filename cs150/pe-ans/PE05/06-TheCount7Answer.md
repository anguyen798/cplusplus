// Given a non-negative int n, return the count of the occurrences of 7 as a digit, so for example 717 yields 2. (no loops).

// Note that mod (%) by 10 yields the rightmost digit (126 % 10 is 6), while divide (/) by 10 removes the rightmost digit (126 / 10 is 12).

// * count7(717) → 2
// * count7(7) → 1
// * count7(123) → 0

```cpp
int count7(int n)
{
    if (n == 0) return 0;
    else if (n % 10 == 7) return 1 + count7(n / 10);
    else return count7(n / 10);
}
```

// https://codecheck.io/files/23030324043msv42pnq0h36zky379o9ou5g