# convert-from-decimal-to-binary
section team
----------------------------
#include <iostream>
#include <vector>

using namespace std;

vector<int> convertDecimalToBinary(int decimalNumber)
{
    vector<int> binaryNumber;

    while (decimalNumber > 0)
    {
        binaryNumber.push_back(decimalNumber % 2);
        decimalNumber /= 2;
    }

    // Reverse the binary number vector
    reverse(binaryNumber.begin(), binaryNumber.end());

    return binaryNumber;
}

int main()
{
    int decimalNumber;

    cout << "Enter a decimal number: ";
    cin >> decimalNumber;

    vector<int> binaryNumber = convertDecimalToBinary(decimalNumber);

    cout << decimalNumber << " in binary = ";

    for (int digit : binaryNumber) // ranged loop 
    {
        cout << digit;
    }

    cout << endl;

    return 0;
}
