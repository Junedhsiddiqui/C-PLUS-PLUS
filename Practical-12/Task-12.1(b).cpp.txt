#include<iostream>
using namespace std;
class A{
    private:
    int a;
    public:
    int b;
    protected:
    int c;
};
class B:public A{
   
    public:
    void display(){
        cout<<"b="<<b;
    }
};
int main(){
    B obj;
    obj.b=10;
    obj.display();
}
