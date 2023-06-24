```cpp
/**
 *  @author Albert Nguyen
 *  @date Summer '23 - Tuesday 12130
 *  @file h03.cpp
 */
#include <iostream>
#include <iomanip>
#include <string>
using namespace std;

string STUDENT = "anguyen798";  // Add your Canvas login name
string ASSIGNMENT = "h03";

// Add your function declaration here
string getStatus(double gpa, int credits, int honorsCredits);

/**
 * Describe the purpose of your program here.
 * @return 0 for success.
 */
int main()
{
	// DON'T CHANGE ANYTHING IN THIS FUNCTION

    cout << STUDENT << "-" << ASSIGNMENT << "-Graduation Calculator" << endl;
	cout << "-----------------------------------------" << endl;

	cout << "Enter gpa, total credits and honors credits: ";
	double gpa;
	int credits, honorsCredits;
	cin >> gpa >> credits >> honorsCredits;

	// You will write this function
	string result = getStatus(gpa, credits, honorsCredits);

	cout << "Result is [\"" << result << "\"]" << endl;

    return 0;
}

// Implement your function here
string getStatus(double gpa, int credits, int honorsCredits)
{
    string graduationStatus;
    if (credits < 180 || gpa < 2.0) {graduationStatus = "not graduating";}
    else if (honorsCredits >= 15 && gpa >= 3.8) {graduationStatus = "summa cum laude";}
    else if (honorsCredits >= 15 && gpa >= 3.6) {graduationStatus = "magna cum laude";}
    else if (gpa >= 3.8) {graduationStatus = "magna cum laude";}
    else if (gpa >= 3.6) {graduationStatus = "cum laude";}
    else if (gpa >= 2.0) {graduationStatus = "graduating";}
    return graduationStatus;
}

```