// Given a string and a non-empty substring sub, compute recursively the number of times that sub appears in the string, without the sub strings overlapping.

// * strCount("catcowcat", "cat") → 2
// * strCount("catcowcat", "cow") → 1
// * strCount("catcowcat", "dog") → 0

```cpp
int strCount(const string& str, const string& sub)
{
   int count {0};
   size_t len {str.size()}, subLen {sub.size()};
   if (len < subLen) return count;
   else if (str.substr(0, subLen) == sub)
   {
      count += 1 + strCount(str.substr(subLen), sub);
   }
   else count += strCount(str.substr(1), sub);
   
   return count;
}
```

// https://codecheck.io/files/2303022223cnfut8un1giatlbfh2xt2gby0