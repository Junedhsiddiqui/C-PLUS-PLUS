#include <iostream>
using namespace std;

class B
{

public:
    int k;
    void displayB()
    {
        cout << "k in B= " << k << endl;
    }
};

class C
{
public:
    int k;
    void displayc()
    {
        cout << "k in C = " << k << endl;
    }
};
class D : public B, public C
{
public:
    void displayD()
    {
        cout << "k of B and C inherited in D => " << B::k << " " << C::k << endl;
    }
};
int main()
{
    D obj;
    obj.B::k = 12;
    obj.C::k = 11;
    obj.displayD();
}