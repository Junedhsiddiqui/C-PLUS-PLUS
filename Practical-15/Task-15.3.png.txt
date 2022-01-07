#include<iostream>
#include<iomanip>
#include<sstream>
#include<string>
using namespace std ;
 
 int main()
 {
	int n =70;
	cout << hex<< n<< endl;
	cout << dec<< n<< endl;	
	
	char  a,b,c;
	stringstream s("  123");
	s>>skipws>>a>>b>>c;
	cout <<a <<b<< c<<endl;
	
	stringstream p("  123");
	p>>noskipws>>a>>b>>c;
	cout <<a <<b<< c<<endl;
	
	stringstream t("  this is a string");
	string line;
	getline(t >> ws,line);
	cout << line<<endl;
 
 	
 }