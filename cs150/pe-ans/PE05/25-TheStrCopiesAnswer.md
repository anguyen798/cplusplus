// Given a string and a non-empty substring sub, compute recursively if at least n copies of sub appear in the string somewhere, possibly with overlapping. N will be non-negative.

// * strCopies("catcowcat", "cat", 2) → true
// * strCopies("catcowcat", "cow", 2) → false
// * strCopies("catcowcat", "cow", 1) → true

```cpp
bool strCopies(const string& str, const string& sub, int n)
{
   size_t len {str.size()}, subLen {sub.size()};
    if (n == 0) return true;
    else if (len < subLen) return false;
    else if (str.substr(0, subLen) == sub)
    {
       return strCopies(str.substr(1), sub, n - 1);
    }
    else return strCopies(str.substr(1), sub, n);
}
```

// https://codecheck.io/files/23030222169incbam0sd6cd1724qtp3kd37