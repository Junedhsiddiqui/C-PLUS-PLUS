#include<iostream>
using namespace std ;
class A 
{
public :
void displayA ()
{
cout << "Class A method called " << endl ;
}
};
class B : public A 
{
public :
void displayB()
{
cout << "Called class A method from class B method" << endl ;
displayA();
}
};

int main ()
{
B obj ;
obj.displayA() ;
} 