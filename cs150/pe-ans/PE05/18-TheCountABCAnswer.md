// Count recursively the total number of "abc" and "aba" substrings that appear in the given string.

// * countAbc("abc") → 1
// * countAbc("abcxxabc") → 2
// * countAbc("abaxxaba") → 2

```cpp
int countAbc(const string& str)
{
   if (str.size() < 3) return 0;
   else
   {
      if (str.substr(0, 3) == "abc" || str.substr(0, 3) == "aba") return 1 + countAbc(str.substr(1));
      else return countAbc(str.substr(1));
   }
}
```

// https://codecheck.io/files/23030223036cgwag8cl430la0adoozs7907