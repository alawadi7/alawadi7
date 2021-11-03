

#include <iostream>
using namespace std;
int main()
{


   string s ; cin>> s ; 
   
   int strt=0; //start from  a // 
   int smoves=0; // all move // 
   
   
   for(int i=0 ; i<s.size();i++) // m      ap 
   {
       int index=s[i]-97 ; //----------> how many move from a to any character //   
       int walk=abs(strt-index);         // 0-12=-12 --(12). here it will move // 
       
       // check if clockwise or counterclockwise // 
       if(walk < 13)
       smoves+=walk ;                 // clockwise // 
       else 
        smoves+=26-walk; // counterclockwise // 
        
         strt=index;             // here to start when i was finish // 

   }
   cout<<smoves <<endl; 
    return 0;
}

