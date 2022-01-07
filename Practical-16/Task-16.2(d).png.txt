#include <iostream>
using namespace std;

void divide(int a, int b)
{
    if (b == 0)
    {
        throw runtime_error("Denominator cannot be 0\nTry something else...!!\n");
    }
    else
    {
        cout << "Result is " << a / b << "\n";
    }
}

int main()
{
    int a, b;
    cout << "Enter two numbers for division \n";
    cin >> a >> b;
    try
    {
        divide(a, b);
    }
    catch (runtime_error &e) 
    {
        cout << e.what() << "\n"; 
    }
    return 0;
}