#include <iostream>
using namespace std;
class A
{
public:
    int a;
    A(int k)
    {
        a = k;
        cout << "a =" << a << endl;
    }
};
class B : public A
{

public:
    int b;
    B(int k):A(k)
    {
        b = k;
        cout << "b =" << b << endl;
    }
};
class C : public B
{
    int c;

public:
    C(int k):B(k)
    {
        c = k;
        cout << "c =" << c << endl;
    }
};
int main()
{
    C obj(16);
}