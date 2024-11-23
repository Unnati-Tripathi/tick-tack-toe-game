#include<bits/stdc++.h>
using namespace std;
 char pos[3][3]={{'1','2','3'} , {'4','5','6'} , {'7','8','9'}};
 int i,j;      
 //act as row and column
  string a= "";
  string b="";
  //player names..
 
 char chance='x';              //game started by cross
 bool t = 0;                        
 
 void start(){
    //Creating table...

    cout<< "   |    |    \n ";
    cout<<""<<pos[0][0]<<" | "<<" "<<pos[0][1]<<" | "<<pos[0][2] <<"\n";
    cout<< "   |    |    \n ";
    cout<< "_|_|__\n";
    cout<< "   |    |   \n ";
     cout<<""<<pos[1][0]<<" | "<<" "<<pos[1][1]<<" | "<<pos[1][2] <<"\n";
    cout<< "   |    |   \n ";
    cout<< "_|_|__\n";
    cout<< "   |    |   \n ";
   cout<<""<<pos[2][0]<<" | "<<" "<<pos[2][1]<<" | "<<pos[2][2] <<"\n";
    cout<< "   |    |   \n ";
 }
 
void functions(){
        int digit;
        if(chance=='x'){
            cout<<a<<" enter your turn  :";
            cin>>digit;}
         if(chance=='0'){
            cout<<b<<" enter your turn  :";
            cin>>digit;}
        if(digit==1){             //conditions for differnt inputs
            i=0,j=0;
        }
        if(digit==2){
            i=0,j=1;
        }
        if(digit==3){
            i=0,j=2;
        }
        if(digit==4){
            i=1,j=0;
        }
        if(digit==5){
            i=1,j=1;
        }
        if(digit==6){
            i=1,j=2;
        }
        if(digit==7){
            i=2,j=0;
        }
        if(digit==8){
            i=2,j=1;
        }
        if(digit==9){
            i=2, j=2;
        }
        else if(digit<0||digit>8){
            cout<<"invalid \n";
        }
        
       
        
        
        if(chance=='x' && pos[i][j] !='x' && pos[i][j]!='0'){
        
            pos[i][j]='x';
            chance='0';
        }
        else if(chance=='0' && pos[i][j] !='x' && pos[i][j]!='0'){
        
            pos[i][j]='0';
            chance='x';
            
        }
        
         else{
            cout<<"Warning!!please enter any valid value.. space filled \n";
            functions();}
       start() ;
    }
    
    
    
    bool goingon(){
        
        for(int k=0;k<3;k++){
            if(pos[k][0]==pos[k][1]&& pos[k][1]==pos[k][2] ){
                return true;
            }
            else if( pos[0][k]==pos[1][k] && pos[1][k] ==pos[2][k]){
                return true;
            
            }
            
        }
        if(pos[0][0]==pos[1][1] && pos[1][1] ==pos[2][2] ||pos[0][2]==pos[1][1] && pos[1][1] ==pos[2][0]){
            return true;
            
        }
        for(int k=0;k<3;k++){
            for( int l=0;l<3;l++){
                if(pos[k][l] != 'x' && pos[k][l] != '0'){
                    return 0;
                }
            }
             
        }
        t=true;
        return 0;
    }
    
    int main(){
        cout<<"                     WELCOME         \n";
        cout<<"   *** Its a Tick-Tac-Toe GAME ***\n";
        
        cout<<"First player's Name \n";
        getline(cin,a );
        cout<<"Second player's Name \n";
        getline(cin,b );
        cout<<"Chance for 1st player:   \n";
        cout<<"Chance for 2st player:   \n";

         while(!goingon()){
             

             start();
             functions();
             goingon();
         }
         if(chance =='0' && t == false){
             cout<<"congracts!!!"<<" "<<a<<" you win..."<<endl;
         }
         else if(chance =='x' && t == false){
             cout<<"congracts!!!"<<" "<<b<<" you win..."<<endl;
         }
         else{
             cout<<"The game is Draw...\n";
    }
    }
