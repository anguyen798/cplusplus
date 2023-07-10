// We'll say that a "pair" in a string is two instances of a char separated by a char. So "AxA" the A's make a pair. Pair's can overlap, so "AxAxA" contains 3 pairs -- 2 for A and 1 for x.

// Recursively compute the number of pairs in the given string.

// countPairs("axa") → 1
// countPairs("axax") → 2
// countPairs("axbx") → 1"

```cpp
int countPairs(const string& str)
{
   if (str.size() < 3) return 0;
   else
   {
      if (str[0] == str[2]) return 1 + countPairs(str.substr(1));
      else return countPairs(str.substr(1));
   }
}
```

// https://codecheck.io/files/2303022308at4et36go59ohdbllmk8qcirb