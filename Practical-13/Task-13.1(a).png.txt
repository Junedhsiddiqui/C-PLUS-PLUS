#include <iostream>
#include <string>
using namespace std;
class base
{
public:
    int add(int a, int b)
    {
        return a + b;
    }
    float add(float a, float b)
    {
        return a + b;
    }
    string add(char a, char b)
    {
        string sum;
        sum = sum + a;
        sum = sum + b;
        return sum;
    }
};
class child : public base
{
public:
    int add(int a, int b)
    {
        return a + b + 1;
    }
};
int main()
{
    base obj1;
    child obj2;
    int ans1 = obj1.add(1, 2);
    int ans2 = obj2.add(1, 2);
    cout << "Overriding func called from base class" << ans1 << endl
         << "overriding fun called from child class" << ans2;
}