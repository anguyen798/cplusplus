// Write a function named minMaxDigit() that accepts an integer as an input parameter and returns the largest and smallest digits using the two output parameters min and max. For example, the call minMaxDigit(68437, min, max) would set min to 3 and max to 8. If there is only one digit, then both min and max are set to the same value. The function returns the value of n before it was changed (68437 in this case).

```cpp
int minMaxDigit(int num, int& min, int& max)
{
    int originalNum {num};
    min = 9, max = 0;

    if(num == 0) min = max = 0; // single digit 0
    else
    {
       while(num > 0)
       {
          int digit = num % 10;
          if(digit < min) min = digit;
          if(digit > max) max = digit;
          num /= 10;
          
       }
    }
    
    return originalNum;
}
```

// https://codecheck.io/files/23030318345hna5ysfbi2esfn7q3p9eg44r