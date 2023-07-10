// Given a string and a non-empty substring sub, compute recursively the largest substring which starts and ends with sub and return its length.

// * strDist("catcowcat", "cat") → 9
// * strDist("catcowcat", "cow") → 3
// * strDist("cccatcowcatxx", "cat") → 9

```cpp
int strDist(const string& str, const string& sub)
{
   // Assign const string param str to new string s
   string s {str};
   int len {s.size()}, subLen {sub.size()};
   
   // Base case
   if (s.substr(0, subLen) == sub && s.substr(len - subLen) == sub) return len;
   
   // Left, discard char in s until match
   if (s.substr(0, subLen) != sub) return strDist(s.substr(1), sub);
   
   // Right, discard char in s until match
   if (s.substr(len - subLen) != sub) return strDist(s.substr(0, len - 1), sub);
   
   // If len is less than subLen
   if (len < subLen) return 0;
}
```

// https://codecheck.io/files/23030221557sc2cak7f5zze7dot4zbwix54