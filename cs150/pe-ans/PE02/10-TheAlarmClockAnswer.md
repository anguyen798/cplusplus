// Given as input a day of the week encoded as 0=Sun, 1=Mon, 2=Tue, ...6=Sat, and a boolean indicating if we are on vacation, print a string of the form "7:00" indicating when the alarm clock should ring. Weekdays, the alarm should be "7:00" and on the weekend it should be "10:00". Unless we are on vacation-then on weekdays it should be "10:00" and weekends it should be "off". Don't put quotes around your answer. I will do that.

// input of 1, false → "7:00"
// input of 5, false → "7:00"
// input of 0, false → "10:00"

```cpp
#include <string>
using std::string;

/**
 *  Given as input a day of the week encoded as 0=Sun,
 *  1=Mon, 2=Tue, ...6=Sat, and a boolean indicating if
 *  we are on vacation, set result to a string of the form
 *  "7:00" indicating when the alarm clock should ring.
 *
 *  Weekdays, the alarm should be "7:00" and on the weekend
 *  it should be "10:00". Unless we are on vacation-then on
 *  weekdays it should be "10:00" and weekends it should be "off".
 */
string alarm_clock(int day, bool on_vacation)
{
    string alarm;
     // Add your code here
     // Weekday
     if (day >= 1 && day <= 5)
     {
     if (on_vacation) { alarm = "10:00"; }
     else { alarm = "7:00"; }
     }
    
    // Weekend
    else
    {
    if (on_vacation) { alarm = "off"; }
    else { alarm = "10:00"; }
    }
    
    return alarm;
}
```

/*
Calling with Arguments

| |Name|Arguments|Actual|Expected|
|---|---|---|---|---|
|pass|alarm_clock|1, false|"7:00"|"7:00"|
|pass|alarm_clock|5, false|"7:00"|"7:00"|
|pass|alarm_clock|0, false|"10:00"|"10:00"|
|pass|alarm_clock|6, true|"off"|"off"|

Score

4/4

\*/

// https://codecheck.io/files/23020919239m47eg7q9jt4n5sxxjdnfsav5