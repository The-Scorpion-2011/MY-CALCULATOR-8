/*MY-CALCULATOR-8
It's a simple calculator only , like a first simple project for me .*/
#include<iostream>
using namespace std;
int main()
{
string name;
double num1;
double num2;
char oper;
double yn;
cout<<"****************************************"<<endl;
cout<<"*************MY CALCULATOR**************"<<endl;
cout<<"****************************************"<<endl;
cout<<"Hi user ! Enter your name :"<<endl;
cin>>name;
cout<<"Welcome to my calculator , "<<name<<" !"<<endl;
do
{
 cout<<"Choose the operator [ + , - , * , / ] :"<<endl;
 cin>>oper;
 while(!(oper=='+'||oper=='-'||oper=='*'||oper=='/'))
 {
 cout<<"Error , "<<name<<" !\nThe input '"<<oper<<"' isn't an operator !"<<endl;
 cout<<"Please try again :"<<endl;
 cin>>oper;
 }
 cout<<"Enter the first number :"<<endl;
 cin>>num1;
 cout<<"Enter the second number :"<<endl;
 cin>>num2;
 switch(oper)
 {
  case '+':
  cout<<"Solution :\n"<<num1<<" + "<<num2<<" = "<<num1+num2<<endl;
  break;
  case '-':
  cout<<"Solution :\n"<<num1<<" - "<<num2<<" = "<<num1-num2<<endl;
  break;
  case '*':
  cout<<"Solution :\n"<<num1<<" × "<<num2<<" = "<<num1*num2<<endl;
  break;
  case '/':
  cout<<"Solution :\n"<<num1<<" ÷ "<<num2<<" = "<<num1/num2<<endl;
  while(num2==0)
  {
   cout<<"Error , "<<name<<" !"<<endl;
   cout<<"it can't be divided by zero ."<<endl;
   cout<<"Please try again :"<<endl;
   cin>>num2;
   if(num2!=0)
   {
    cout<<"Solution :\n"<<num1<<" ÷ "<<num2<<" = "<<num1/num2<<endl;
   }
  }
  break;
 }
 cout<<"To calculate another operator :\n[ 0 = No , 1 = Yes ] :"<<endl;
 cin>>yn;
 while(!(yn==0||yn==1))
 {
 cout<<"Error , "<<name<<" !"<<endl;
 cout<<"You should choose 0 or 1 :"<<endl;
 cin>>yn;
 }
}while(yn==1);
if(yn==0)
{
 cout<<"Ok "<<name<<" , As you like ."<<endl;
 cout<<"Thanks for using my calculator ."<<endl;
}
cout<<"****************************************"<<endl;
cout<<"*****************THE END****************"<<endl;
cout<<"****************************************"<<endl;
return 0;
}
