```cpp
/**
 *  @author Albert Nguyen
 *  @date Summer '23
 *  @file h01.cpp
 */
#include <iostream>
#include <string>
#include <iomanip>
using namespace std;

string STUDENT = "anguyen798";
string ASSIGNMENT = "h01";
void title(string studentParam, string assignmentParam);

/**
 * Main function which runs the sub-functions, declarations before definitions after
 * @return 0 for success.
 */
int main()
{
    // Add your implementation comments here
    // Title and introduction
    title(STUDENT, ASSIGNMENT);
    int timeHours, timeMinutes, durationHours, durationMinutes;
    int timeHoursAfter, timeMinutesAfter, timeHoursBefore, timeMinutesBefore;
    char discard;
    
    // 2. Input section: prompt and input on same line
    cout << "    Time: ";
    cin >> timeHours >> discard >> timeMinutes;
    cout << "    Duration: ";
    cin >> durationHours >> discard >> durationMinutes;
    // 3. Processing section - compute the results
    timeHoursAfter = timeHours + durationHours;
    timeMinutesAfter = timeMinutes + durationMinutes;
    timeHoursBefore = timeHours - durationHours;
    timeMinutesBefore = timeMinutes - durationMinutes;
    // Convert minute surplus/defecit to  increment/decrement hour 
    if (timeMinutesAfter >= 60)
    {
        timeMinutesAfter -= 60;
        ++timeHoursAfter;
    }
    if (timeMinutesBefore < 0)
    {
        timeMinutesBefore += 60;
        --timeHoursBefore;
    }
    // Adjust time for under or over 24 hours
    if (timeHoursAfter > 24) {timeHoursAfter -= 24;}
    if (timeHoursBefore < 0) {timeHoursBefore += 24;}
    // Convert to 12 hour clock
    if (timeHoursAfter > 12) {timeHoursAfter -= 12;}
    if (timeHoursBefore > 12) {timeHoursBefore -= 12;}
    
    // 4. Output section: test data inside brackets []
    cout << durationHours << ":";
    cout << setfill('0') << setw(2) << durationMinutes << " hours after, and before, ";
    cout << timeHours << ":";
    cout << setfill('0') << setw(2) << timeMinutes << " is [";
    cout << timeHoursAfter << ":";
    cout << setfill('0') << setw(2) << timeMinutesAfter << ", ";
    cout << timeHoursBefore << ":";
    cout << setfill('0') << setw(2) << timeMinutesBefore << "]" << endl;
    return 0;
}

void title(string studentParam, string assignmentParam)
{
    cout << string(50, '-') << endl;
    cout << studentParam << "-" << assignmentParam << ": ";
    cout << "Time on My Hands" << endl;
    cout << string(50, '-') << endl;
}

```