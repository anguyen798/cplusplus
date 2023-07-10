// Write a function named factorCount() that accepts an integer (assumed to be positive) as its input parameter, returns a count of its positive factors in its output parameter, and returns the largest factor (not counting 1 or the number itself), via the return statement.

// For example, the eight factors of 24 are 1, 2, 3, 4, 6, 8, 12, and 24, so the call factorCount(24, fCount) should return 12 and set fCount to 8.

// If there are no factors other than 1 and the number itself (such as 3), return -1 and set fCount to 2 (1 and the number itself).

```cpp
int factorCount(int input, int& fCount)
{
   fCount = 0;
   int largest_factor {-1};
   for (int i {1}; i <= input; ++i)
   {
      if (input % i == 0)
      {
         fCount++;
         if (i != 1 && i != input) largest_factor = i;
      }
    }
    
    return largest_factor;
}
```

// https://codecheck.io/files/23030319196qf5c29rm3ycrnjpbv9z30c7v