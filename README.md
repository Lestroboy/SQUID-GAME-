#include<iostream>
#include<string>

using namespace std;

int main()
{
    cout<<"\t\t\t\tWELLCOME TO PROGU WORLD.\t\t"<<endl;
    
    cout<<"PRESS ENTER TO START."<<endl;
    getchar();
    
    string name;
    
    cout<<"ENTER YOUR NAME :";
    cin>>name;
    cout<<endl;
    
    cout<<"NICE TO MEET YOU "<<name<<"!"<<endl;
    
    int choice;
    
    restart1:
    cout<<"ENTER 1 TO START SQUID GAME :)"<<endl;
    cout<<"ENTER 0 TO LEAVE."<<endl;
    cin>>choice;
    cout<<endl;
    
    if(choice == 1)
    {
        cout<<"\t\t\t\tWELLCOME TO SQUID GAME :)\t\t"<<endl;
    }
    
    else if(choice == 0)
    {
        cout<<"\t\t\t\tI THINK YOU ARE AFRAID TO PLAY\t\t"<<endl;
        cout<<"\t\t\t\t            BYE               \t\t"<<endl;
        cout<<"\t\t\t\t             :)               \t\t"<<endl;
        return 0;
    }
    
    else
    {
        cout<<"ENTERED INPUT IS INCORRECT."<<endl;
        cout<<endl;
        goto restart1;
    }
    
    
    
    
    
    
    
    
    
    
    
    return 0;
}
