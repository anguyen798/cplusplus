// Write a function named digitRange() that accepts an integer as an input parameter and returns the range of values of its digits in its output parameter. The function should return the original number unchanged. The range is defined as 1 more than the difference between the largest and smallest digit value. For example, the call digitRange(68437, range) would set range to 6 because the largest digit value is 8 and the smallest is 3, so 8 - 3 + 1 = 6. If the number contains only one digit, set range to 1. Solve this problem without using a string.

```cpp
int digitRange(int num, int &range)
{
    int min {9}, max {0}, digit {0}, originalNum {num};

    if(num == 0) { // single digit 0
        min = max = 0;
    } else {
        while(num > 0) {
            digit = num % 10;
            if(digit < min) min = digit;
            if(digit > max) max = digit;
            num /= 10;
        }
    }
    range = max - min + 1;
    
    return originalNum;
}
```

// https://codecheck.io/files/2303031853agynd6xav0598i79hvq1zs4l1