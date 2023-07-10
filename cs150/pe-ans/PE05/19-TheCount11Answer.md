// Given a string, compute recursively (no loops) the number of "11" substrings in the string. The "11" substrings should not overlap.

// * count11("11abc11") → 2
// * count11("abc11x11x11") → 3
// * count11("111") → 1

```cpp
int count11(const string& str)
{
   if (str.size() < 2) return 0;
   else
   {
      if (str.substr(0, 2) == "11") return 1 + count11(str.substr(2));
      else return count11(str.substr(1));
   }
}
```

// https://codecheck.io/files/2303022259y48v91mg1n3ifkcl787765kq