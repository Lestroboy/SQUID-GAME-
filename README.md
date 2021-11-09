#include <iostream>
#include <string>
#include <cstdlib>
#include <ctime>

using namespace std;

int main()
{

                                //WELLCOMING THE PLAYER.
    
    cout<<"\t\t\t\tWELLCOME TO PROGU WORLD.\t\t"<<endl;
    
    cout<<"PRESS ENTER TO START."<<endl;
    getchar();
    
    string name;
    
    cout<<"ENTER YOUR NAME :";
    cin>>name;
    cout<<endl;
    
    cout<<"NICE TO MEET YOU "<<name<<"!"<<endl;
    
    int choice;
    
                                //ASKING TO PLAY THE GAME.
    
    restart1:
    cout<<"ENTER 1 TO START SQUID GAME :)"<<endl;
    cout<<"ENTER 0 TO LEAVE."<<endl;
    cin>>choice;
    cout<<endl;
    
                                //WILLING TO PLAY THE GAME.
    
    if(choice == 1)
    {
    cout<<"\t\t\t\tWELLCOME TO SQUID GAME :)\t\t"<<endl;
    
                                //FIRST GAME.
        
    cout<<"\t\t\t\tWELLCOME TO FIRST GAME."<<endl<<endl;
    
    cout<<"\t\t\t     GAME1: RED LIGHT - GREEN LIGHT."<<endl<<endl;
    
    cout<<"\t\t\tHI PLAYER I HAVE SET A NUMBER IN MY MIND\n\t\t\tBETWEEN 1 TO 100.YOU HAVE 8 CHANCE TO GUESS\n\t\t\tMY NUMBER.BUT IF YOU DIDN'T GUESSED THE NUMBER\n\t\t\tWITHIN 8 CHANCE,YOU WILL BE ELIMINATED FROM THE GAME!"<<endl;
    
    int num, guess, tries = 0;
    
    srand(time(0));
    num = rand() % 100 + 2;
    
    cout<<"GAME STARTS NOW :)\n"<<endl;
 
    do
	{
		cout << "GUESS MY NUMBER : ";
		cin >> guess;
		tries++;

		if(guess > num)
			cout<<"INCORRECT: GUESS THE NUMBER LITTLE SMALL.\n\n";
			
		else if(guess < num)
			cout<<"INCORRECT: GUESS THE NUMBER LITTLE BIG.\n\n";
			
		else
			cout<<"\nYOU TOOKED "<<tries<<" TRIES TO GUESSES.\n"<<endl;
			
    	} while(guess != num);
			
		if(tries <= 8)
		{
		    cout<<"CONGRATULATIONS YOU GUESSED IN "<<tries<<" TRIES!"<<endl;
		}
		
		else{
		    cout<<"YOU ARE ELIMINATED!"<<endl;
		    return 0;
		}
    }
    
                            //NOT WILLING TO PLAY THE GAME.
    
    else if(choice == 0)
    {
        cout<<"\t\t\t\tI THINK YOU ARE AFRAID TO PLAY\t\t"<<endl;
        cout<<"\t\t\t\t            BYE               \t\t"<<endl;
        cout<<"\t\t\t\t             :)               \t\t"<<endl;
        return 0;
    }
    
                            //WRONG INPUT TO PLAY THE GAME
    
    else
    {
        cout<<"ENTERED INPUT IS INCORRECT."<<endl;
        cout<<endl;
        goto restart1;
    }
    
    
    
    
    return 0;
}
