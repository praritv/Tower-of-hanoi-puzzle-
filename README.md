//# Tower-of-hanoi-puzzle-
//solved using recurssion in cpp
#include<iostream>
using namespace std;
void tower(int,int,int,int);
int main()
{
int n,start,end,empty;
    cout<<"In this puzzle there will be three rods 1 , 2 and 3"<<endl;
    cout<<endl<<"enter the number of disks you want to perform the puzzle with"<<endl;
	cin>>n;
	cout<<endl<<"enter the rod which contains all the disks in the start"<<endl;
	cin>>start;
	cout<<endl<<"enter the rod where you want to transfer all the disks"<<endl;
	cin>>end;
	cout<<endl<<"enter the rod which will be empty"<<endl;
	cin>>empty;
	cout<<"so the steps you need to follow to complete the puzzle are"<<endl;
	tower(n,start,end,empty);
	return 0;
}
//PART WHICH CONTAINS RECURSION:
void tower(int n,int start,int end,int empty)
{
if(n==1)
{
	cout<<"-->"<<"move disk 1 from rod "<<start<<" to rod "<<end<<endl;
	return ;
}
else
tower(n-1,start,empty,end);
cout<<"-->"<<"move disk "<<n<<" from rod "<<start<<" to rod "<<end<<endl;
tower(n-1,empty,end,start);
}
