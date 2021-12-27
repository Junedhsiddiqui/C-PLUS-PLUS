#include <iostream>
using namespace std;
class A
{
public:
    ~A()
    {
        cout << "Execution of Class A Destructor" << endl;
    }
};
class B : public A
{

public:
    ~B()
    {
        cout << "Execution of Class B Destructor" << endl;
    }
};
class C : public B
{
public:
    ~C()
    {
        cout << "Execution of Class C Destructor" << endl;
    }
};
int main()
{
    C obj;
      cout << "calling of Class A Destructor" << endl;
         obj.~A();
           cout <<endl<< "calling of Class B Destructor" << endl;
          obj.~B();
            cout<<endl << "calling of Class C Destructor" << endl;
          obj.~C();
            cout <<endl<< "Default Destructor called as Program Ends" << endl;
}