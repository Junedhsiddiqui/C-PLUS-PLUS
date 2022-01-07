#include <iostream>
#include <string>
using namespace std;
class base
{
public:
    base()
    {
        cout << "BC" << endl;
    }
    ~base()
    {
        cout << "BD" << endl;
    }
};
class child : public base
{
public:
    child()
    {
        cout << "CC" << endl;
    }
    ~child()
    {
        cout << "CD" << endl;
    }
};
int main()
{
    base *p;
    child c;
    p = &c;
    delete p;         // BC CC BD
    // p->~base();    BC CC BD CD BD  
    // p->~child();  error: the type being destroyed is 'base', but the destructor refers to 'child'
}