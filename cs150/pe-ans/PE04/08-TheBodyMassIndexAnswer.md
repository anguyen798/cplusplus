// Write a function named bmiCalc() that accepts two input parameters of type double, representing a person's height and weight (in that order). The function returns (through the return statement) the user's BMI. It also returns, through an integer output parameter, the BMI category as calculated below.

// | BMI              | Category Class |
// | below 18.5   | 1                       |
// | 18.5 - 24.9    | 2                       |
// | 25.0 - 29.9    | 3                       |
// | 30.0 and up  | 4                       |

// int bmiClass;
// double bmi = bmiCalc(70.0, 194.25, bmiClass);
// cout << "BMI " << bmi << ",  class " << bmiClass << endl;
// BMI = 27.8689, class 3

```cpp
double bmiCalc(double height, double weight, int &bmiClass)
{
    double bmi = (weight * 703) / (height * height);
    if (bmi < 18.5)
        bmiClass = 1;
    else if (bmi >= 18.5 && bmi <= 24.9)
        bmiClass = 2;
    else if (bmi >= 25.0 && bmi <= 29.9)
        bmiClass = 3;
    else
        bmiClass = 4;
        
    return bmi;
}
```

// https://codecheck.io/files/230303191229wyt0xkqhx2u3rvfjdlb0wyk