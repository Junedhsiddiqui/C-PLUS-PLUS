#include <iostream>
#include <vector>
#include <algorithm>
#include <iterator>
using namespace std;

// function for printing the elements in a vector
void printvector(vector<int> v)
{
    vector<int>::iterator it;
    for (it = v.begin(); it != v.end(); ++it)
        cout << *it << " ";
    cout << '\n';
}
int main()
{
    vector<int> v;
    int n;
    cout << "Enter the size of the vector \n";
    cin >> n;
    for (int i = 0; i < n; i++)
    {
        int ele;
        cin >> ele;
        v.push_back(ele);
    }
    printvector(v);
    // B part of Task
    cout << "Size of the vector is : " << v.size() << "\t Capacity of vector is : " << v.capacity() << "\n";
    // C part of Task
    v.resize(2 * n, 0);
    cout
        << "Printing vector after resizing and intialising after 0\n";
    printvector(v);
    // D part of Task
    cout << "Checking vector is empty or not after :\n";
    if (v.empty())
        cout << "Vector is empty\t";
    else
        cout << "Vector is not empty";
    return 0;
}