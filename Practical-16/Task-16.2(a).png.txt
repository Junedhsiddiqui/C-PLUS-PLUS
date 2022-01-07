#include <iostream>
using namespace std;

int main()
{
    int a, b;
    cout << "Enter two numbers for division \n";
    cin >> a >> b;
    try
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
    catch (runtime_error &e)
    {
        cout << e.what() << "\n";
    }
    return 0;
}
// Since no matching catch handler is found,exception is uncaught,
// and the run-time call to std::terminate is made as for uncaught exception.