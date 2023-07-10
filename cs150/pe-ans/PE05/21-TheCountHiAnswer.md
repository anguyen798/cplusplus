// Given a string, compute recursively the number of times lowercase "hi" appears in the string, however do not count "hi" that have an 'x' immediately before them.

// * countHi2("ahixhi") → 1
// * countHi2("ahibhi") → 2
// * countHi2("xhixhi") → 0

```cpp
int countHi2(const string& str)
{
   int counter {0};
   if (str.size() < 2) return counter;
   if (str.substr(0, 2) == "hi") counter += 1 + countHi2(str.substr(1));
   else if (str.substr(0, 2) == "xh") counter += countHi2(str.substr(2));
   else if (str.substr(0, 2) != "hi") counter += countHi2(str.substr(1));
   
   return counter;
}
```

// https://codecheck.io/files/23030222432lf5bkby08sd36vk4mxinpttd