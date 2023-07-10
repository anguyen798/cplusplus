// We have a number of bunnies and each bunny has two big floppy ears. We want to compute the total number of ears across all the bunnies recursively (without loops or multiplication).

// * bunnyEars(0) → 0
// * bunnyEars(1) → 2
// * bunnyEars(2) → 4

```cpp
int bunnyEars(int n)
{
   if (n == 0) return 0;
   else return 2 + bunnyEars(n - 1);
}
```

// https://codecheck.io/files/2303032421ckb4b3i3tre83rf5u49tde5wz