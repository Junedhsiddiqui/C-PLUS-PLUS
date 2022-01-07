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
    virtual ~base()
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
    delete p;
}