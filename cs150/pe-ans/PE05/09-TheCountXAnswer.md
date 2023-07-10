// Given a string, compute recursively (no loops) the number of lowercase 'x' chars in the string.

// * countX("xxhixx") → 4
// * countX("xhixhix") → 3
// * countX("hi") → 0

```cpp
int countX(const string& str)
{
   if (str.empty()) return 0;
   if (str[0] == 'x') return 1 + countX(str.substr(1));
   else return countX(str.substr(1));
}
```



// https://codecheck.io/files/23030223455mzvggpsxrhp2n6sx0yctl0wj