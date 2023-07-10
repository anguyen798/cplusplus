// Given base and n that are both 1 or more, compute recursively (no loops) the value of base to the n power, so powerN(3, 2) is 9 (3 squared).

// * powerN(3, 1) → 3
// * powerN(3, 2) → 9
// * powerN(3, 3) → 27

```cpp
int powerN(int n, int exponent)
{
    if (exponent == 0) return 1;
    else return n * powerN(n, exponent - 1);
}
```

// https://codecheck.io/files/23030223495soztkuhr36giv9xe2rnw7j68