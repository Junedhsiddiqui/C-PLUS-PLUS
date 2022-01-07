#include<iostream>
#include<fstream>
#include<string>
using namespace std ;

int main()
{
	fstream myfile;
	myfile.open("text.txt",ios::app);
        if(!myfile)  cout<<"file not created";
        else         myfile<<"  This is appended ";
	myfile<< "this is the text written into the file";
	myfile.close();
	return 0;
}