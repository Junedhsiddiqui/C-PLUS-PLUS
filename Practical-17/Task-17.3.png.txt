#include <bits/stdc++.h>
#include <map>
#include <algorithm>
#include <iterator>
using namespace std;

// function for printing the elements in a map
void printmap(map<int, string> v)
{
    map<int, string>::iterator it;
    for (it = v.begin(); it != v.end(); ++it)
        cout << it->first << " " << it->second << "\n";
    cout << '\n';
}
int main()
{
    map<int, string> m;
    // Inserting Elements in Random order
    m.insert(pair<int, string>(6, "Map"));
    m.insert(pair<int, string>(3, "Iterator"));
    m.insert(pair<int, string>(8, "pair"));
    m.insert(pair<int, string>(1, "coders"));
    m.insert(pair<int, string>(9, "algorithm"));
    m.insert(pair<int, string>(2, "begin"));
    m.insert(pair<int, string>(5, "end"));
    // printing map
    printmap(m);
    // 4th part of Task
    // Find an element as key from this map
    auto itr = m.find(3);
    cout << "itr is poiting to \n"
         << itr->first << " " << itr->second << " \n";
    // 5th Task Assigning one map to another
    map<int, string> copyMap = m;
    cout << "Printing copyMap :\n";
    printmap(copyMap);
    // Deleting a key from map
    cout << "Deleting a key-value from copyMap : 9 algorithm\n";
    copyMap.erase(9);
    cout << "Printing map After deleting key = 9 from it\n";
    printmap(copyMap);
    // Finding size and max size of map
    cout << "Size of the map is : " << copyMap.size() << "\t maxSize of map is : " << copyMap.max_size() << "\n";
    // Checking a map is empty or not
    cout << "Checking map is empty or not after :\n";
    if (copyMap.empty())
        cout << "Map is empty\n";
    else
        cout << "Map is not empty\n";
    // Clearing a map
    copyMap.clear();
    cout << "Printing a Map after Clearing it :\n";
    printmap(copyMap);
    return 0;
}