```cpp
/**
 *  @author Albert Nguyen
 *  @date Summer '23
 *  @file h02.cpp
 */
#include <iostream>
#include <iomanip>
#include <string>
using namespace std;
using stringIn = const string&;

string STUDENT = "anguyen798";  // Add your Canvas login name
string ASSIGNMENT = "h02";

// Function Prototypes
void title(string studentParam, string assignmentParam);
void printTitle();
string getInput();
double letterToPoints(stringIn letterGrade);
void printReport(double points);

// Constants
const double INVALID_COMBINATION = -1.0;
const double INVALID_INPUT = -2.0;

/**
 * Calculates the grade points for a letter grade.
 * @return 0 for success.
 */
int main()
{
	printTitle();
	string letterGrade = getInput();
	double points = letterToPoints(letterGrade);
	printReport(points);

    return 0;
}

// Implement your functions here
void title(string studentParam, string assignmentParam)
{
    cout << string(50, '-') << endl;
    cout << studentParam << "-" << assignmentParam << ": ";
    cout << "Grade-Calculator" << endl;
    cout << string(50, '-') << endl;
}
// string STUDENT = "anguyen798";  // Add your Canvas login name
// string ASSIGNMENT = "h02";
void printTitle()
{
    cout << STUDENT << "-" << ASSIGNMENT << "-Grade Calculator\n";
    cout << string(50, '-') << endl;
}
string getInput()
{
    string result;
    cout << "Enter your letter grade: ";
    getline(cin, result);
    return result;
}
double letterToPoints(stringIn letterGrade)
{
    double result;
    if (letterGrade == "A") {result = 4.0;}
     else if (letterGrade == "A-") {result = 3.7;}
     else if (letterGrade == "B+") {result = 3.3;}
     else if (letterGrade == "B") {result = 3.0;}
     else if (letterGrade == "B-") {result = 2.7;}
     else if (letterGrade == "C+") {result = 2.3;}
     else if (letterGrade == "C") {result = 2.0;}
     else if (letterGrade == "C-") {result = 1.7;}
     else if (letterGrade == "D+") {result = 1.3;}
     else if (letterGrade == "D") {result = 1.0;}
     else if (letterGrade == "D-") {result = 0.7;}
     else if (letterGrade == "F") {result = 0.0;}
     else if (letterGrade == "A+" || letterGrade == "F+" || letterGrade == "F-" )
    {
        result = INVALID_COMBINATION;
    }
    else {result = INVALID_INPUT;}
    return result;
}

void printReport(double points)
{
    cout << "Grade value is [";
    if (points >= 0)
    {
        cout << fixed <<  setprecision(1) << points;
    }
    else if (points == INVALID_INPUT) {cout << "Invalid input";}
    else if (points == INVALID_COMBINATION) {cout << "Invalid combination";}
    cout <<  "]\n";
}

```