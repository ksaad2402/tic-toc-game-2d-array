#include<iostream>
#include<stdio.h>
#include<stdlib.h>

using namespace std;
char tictac[3][3]={{'1','2','3'},{'4','5','6'},{'7','8','9'},};
char turn = 'x';
int row, column;

void display_block(){
system("cls");
cout<<"*************************\n";
cout<<"*************************\n";
cout<<"player 1 = [x]\n";
cout<<"player 2 = [0]\n";
cout<<"\n";
cout<<"\t\t     "<<tictac[0][0]<< "   |   "<<tictac[0][1]<<"   |   "<<tictac[0][2]<<endl;
cout<<"\t\t---------|-------|------- "<<endl;
cout<<"\t\t     "<<tictac[1][0]<< "   |   "<<tictac[1][1]<<"   |   "<<tictac[1][2]<<endl;
cout<<"\t\t---------|-------|------- "<<endl;
cout<<"\t\t     "<<tictac[2][0]<< "   |   "<<tictac[2][1]<<"   |   "<<tictac[2][2]<<endl;
cout<<"\n";
cout<<"\n";
}
void player_turn(){
int num;

if(turn == 'x'){
cout<<"player 1 [x] \n";
cin>>x;
}

if(turn == '0'){
cout<<"player 2 [0] \n";
cin>>num;
}


switch(num){
case 1:row=0; column=0;break;
case 2:row=0; column=1;break;
case 3:row=0; column=2;break;
case 4:row=1; column=0;break;
case 5:row=1; column=1;break;
case 6:row=1; column=2;break;
case 7:row=2; column=0;break;
case 8:row=2; column=1;break;
case 9:row=2; column=2;break;
default:
cout<<"invalid input!";
break;
}
if(turn == 'x'){
    tictac[row][column]= 'x';
    turn='y';}
if(turn == '0'){
    tictac[row][column]= '0';
    turn='x';}

}


int main()
{

while(true)
{
display_block();
player_turn();
display_block();
}

return 0;
}
