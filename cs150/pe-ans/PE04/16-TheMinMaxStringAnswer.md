// Write a function named minMaxStr() that accepts a string input parameter and two integer output parameters, min and max.
// Set min the ASCII value of the smallest alphabetical character and max to the largest. Only consider alphabetical characters. The return statement should return the real ratio of min to max. Make sure that the input string is not modified.

```cpp
double minMaxStr(const string &str, int &min, int &max) {
    min = static_cast<int>('z');
    max = static_cast<int>('A');
    
    for(char c : str)
    {
       if (c >= 'A' && c <= 'Z' || c >= 'a' && c <= 'z')
        {
            int ascii {static_cast<int>(c)};
            if(ascii < min) min = ascii;
            if(ascii > max) max = ascii;
        }
    }

    return static_cast<double>(min) / max;
}
```

// https://codecheck.io/files/2303030112cv2s5h3k4oggrpdc6x14a6i3