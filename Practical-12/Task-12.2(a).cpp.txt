#include <iostream>
using namespace std;
class A
{
public:
    A()
    {
        cout << "Execution of Class A Constructor" << endl;
    }
};
class B : public A
{

public:
    B()
    {
        cout << "Execution of Class B Constructor" << endl;
    }
};
class C : public B
{

public:
    C()
    {
        cout << "Execution of Class C Constructor" << endl;
    }
};
int main()
{
    cout << "Called Constructor of C" << endl
         << "............." << endl;
    C obj;
}