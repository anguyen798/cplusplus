```cpp
/**
 *  @author Albert Nguyen
 *  @date Summer '23 - Tuesday 12130
 *  @file h00.cpp
 */
#include <iostream>
#include <string>
// using namespace std;  // Commenting out for explicit namespace qualification

std::string STUDENT = "anguyen798";  // Add your Canvas login name
extern std::string ASSIGNMENT; // For explicit namespace, had to prefix std::

/**
 * Reads input in ounces per box of cereal, outputs weight in metric tons and boxes per ton
 * @return 0 for success.
 */
int main()
{
    // Using explicit namespace qualification to practice remembering libraries
    std::cout << STUDENT << "-" << ASSIGNMENT << ": ";
    std::cout << "Cereal Box Calculator" << std::endl;
    std::cout << std::string(50, '-') << std::endl;

    // Add your implementation comments here
    // Input: weight of box of cereal in ounces
    // Output: weight of box in metic tons, boxes per ton.
    // Given: metric ton is 35, 273.92 ounces
    // Calculation: weight tons <- weight in oz divided by oz per metric ton.
    // Calculation: boxes <- 1 divided by weight of boxes in tons.

    // Input
    std::cout << "Enter ounces per box of cereal: ";  // prompt for ounces
    double ouncesPerBox;  // store input as float
    std::cin >> ouncesPerBox;  // read input
    double TONS_PER_OUNCES;  // store constant as float
    TONS_PER_OUNCES = 35273.92;  // constant for ounces per ton
    std::cout << "Weight in metric tons, boxes per ton: ["
    << ouncesPerBox / TONS_PER_OUNCES << ", "
    << TONS_PER_OUNCES / ouncesPerBox << "]" << std::endl;
    return 0;
}