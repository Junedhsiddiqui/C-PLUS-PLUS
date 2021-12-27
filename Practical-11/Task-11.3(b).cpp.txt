#include <iostream>
using namespace std;
class A
{
public:
    int k;
    void displayA()
    {
        cout << "k = " << k << endl;
    }
};

class B : virtual public A
{
public:
    void displayB()
    {
        k = 10;
        cout << "k in B= " << k << endl;
    }
};

class C : virtual public A
{
public:
    void displayc()
    {
        k = 20;
        cout << "k in C = " << k << endl;
    }
};
class D : public B, public C
{
public:
    void displayD()
    {

        cout << "k in D " << k << endl;
    }
};
int main()
{
    D obj;
    obj.k=10;
    obj.displayD();
}