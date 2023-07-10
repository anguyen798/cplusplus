// Write a function named binToDec() that accepts an integer parameter whose digits are meant to represent binary (base-2) digits, and converts that integer's representation to decimal (base-10). The function should return the integer value before it was converted. For example, given this code:

// int a = 101011;
// int b = binToDec(a);
// cout << "a->" << a << ", b->" << b << endl;

// The output is: a->43, b->101011

// Constraints: Do not use a string in your solution. Also do not use any built-in base conversion functions from the system libraries. You must program this by "hand".

```cpp
int binToDec(int& a) {
    int binary {a}, decimal {0}, base {1};
    while (a)
    {
       int last_digit {a % 10};
       a /= 10;
       
       decimal += last_digit * base;
       base *= 2;
       
    }
    a = decimal;
    
    return binary;
}
```

// https://codecheck.io/files/23030319489l5tk7tcydm5ba08sbbke1tox