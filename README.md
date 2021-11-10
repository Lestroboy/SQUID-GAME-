#include <iostream>
#include <string>
#include <cstdlib>
#include <ctime>

using namespace std;

int main()
{

                                //WELLCOMING THE PLAYER.
    
    cout<<"\t\t\t\tWELLCOME TO LESTRO WORLD.\t\t"<<endl;
    
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
    cout<<"\t\t\t\t__________________________"<<endl<<endl;
    cout<<"\t\t\t\t  WELLCOME TO FIRST GAME."<<endl<<endl;
    cout<<"\t\t\t\t__________________________"<<endl<<endl;
    
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
		    goto restart4;
		}
		
		else{
		    cout<<"YOU ARE ELIMINATED!"<<endl;
		    return 0;
		}
		
		restart4:
		
		cout<<"\t\t\t\t********************************************"<<endl;
        cout<<"\t\t\t\t*CONGRATULATION YOU MADE WITH FIRST GAME :)*"<<endl;
        cout<<"\t\t\t\t********************************************"<<endl;
        
                                //SECOUND GAME
        cout<<"\t\t\t\t____________________________"<<endl<<endl;       
        cout<<"\t\t\t\t  WELLCOME TO SECOUND GAME."<<endl<<endl;
        cout<<"\t\t\t\t____________________________"<<endl<<endl;
    
        cout<<"\t\t\t        GAME2: ROCK-PAPER-SCISSOR."<<endl<<endl;

        cout << "\t\t\tTHE RULES OF THIS GAME ARE THE FOLLOWING: " <<endl<<endl;
        cout << "\t\t\tA) THIS GAME WILL BE THE BEST OUT 5." <<endl;
        cout << "\t\t\tB) ROCK BEATS SCISSORS, BUT LOOSES AGAINST PAPER" <<endl;
        cout << "\t\t\tC) SCISSORS BEATS PAPER, BUT LOOSES AGAINST ROCK" <<endl;
        cout << "\t\t\tD) PAPER BEATS ROCK, BUT LOOSES AGAINST SCISSORS" <<endl<<endl;
    
        int compchoice, compcount (0), playercount (0);
        char pick;
        srand (time (0));
    
    do
    {
        return2:
        
        cout<<"CHOOSE THE OBJECT: r - rock\n\t\t   p - paper\n\t\t   s - scissor"<<endl;
        cin>>pick;
        
                                    //YOU CHOOSED ROCK
        
        if(pick == 'r')
        {
        cout<<"YOU CHOOSED |ROCK|"<<endl;
        compchoice = rand () % 3 + 1;
        
        if(compchoice == 1)
        {
            cout<<"COMPUTER CHOOSED |ROCK|"<<endl;
            cout<<"THIS ROUND IS A TIE."<<endl;
            cout<<endl;
        }
        
        else if(compchoice == 2)
        {
            cout<<"COMPUTER CHOOSED |PAPER|"<<endl;
            cout<<"SO, COMPUTER WIN THIS ROUND."<<endl;
            compcount++;
            cout<<"COMPUTER WON "<<compcount<<" ROUND."<<endl;
            cout<<endl;
            
            if(compcount == 4)
            {
                cout<<"SO....COMPUTER WON THIS GAME!"<<endl;
                goto restart3;
            }
        }
        
        else
        {
            cout<<"COMPUTER CHOOSED |SCISSORS|"<<endl;
            cout<<"SO, YOU WIN THIS ROUND."<<endl;
            playercount++;
            cout<<"YOU WON "<<playercount<<" ROUND."<<endl;
            cout<<endl;
            
            if(playercount == 4)
            {
                cout<<"CONGRATULATION! YOU WON THIS GAME!"<<endl;
                goto restart3;
            }
        }
        
                                    //YOU CHOOSED PAPER
        
        }
        
        else if(pick == 'p')
        {
            cout<<"YOU CHOOSED |PAPER|"<<endl;
            compchoice = rand () % 3 + 1;
        
        if(compchoice == 1)
        {
            cout<<"COMPUTER CHOOSED |ROCK|"<<endl;
            cout<<"SO, YOU WIN THIS ROUND."<<endl;
            playercount++;
            cout<<"YOU WON "<<playercount<<" ROUND."<<endl;
            cout<<endl;
            
            if(playercount == 4)
            {
                cout<<"CONGRATULATION! YOU WON THIS GAME!"<<endl;
                goto restart3;
            }
        }
        
        else if(compchoice == 2)
        {
            cout<<"COMPUTER CHOOSED |PAPER|"<<endl;
            cout<<"THIS ROUND IS A TIE."<<endl;
            cout<<endl;
        }
        
        else
        {
            cout<<"COMPUTER CHOOSED |SCISSORS|"<<endl;
            cout<<"SO, COMPUTER WIN THIS ROUND."<<endl;
            compcount++;
            cout<<"COMPUTER WON "<<compcount<<" ROUND."<<endl;
            cout<<endl;
            
            if(compcount == 4)
            {
                cout<<"SO....COMPUTER WON THIS GAME!"<<endl;
                goto restart3;
            }
        }
            
                                    //YOU CHOOSED SCISSORS
            
        }
        
        else if(pick == 's')
        {
            cout<<"YOU CHOOSED |SCISSORS|"<<endl;
            compchoice = rand () % 3 + 1;
        
        if(compchoice == 1)
        {
            cout<<"COMPUTER CHOOSED |ROCK|"<<endl;
            cout<<"SO, COMPUTER WIN THIS ROUND."<<endl;
            compcount++;
            cout<<"COMPUTER WON "<<compcount<<" ROUND."<<endl;
            cout<<endl;
            
            if(compcount == 4)
            {
                cout<<"SO....COMPUTER WON THIS GAME!"<<endl;
                goto restart3;
            }
        }
        
        else if(compchoice == 2)
        {
            cout<<"COMPUTER CHOOSED |PAPER|"<<endl;
            cout<<"SO, YOU WIN THIS ROUND."<<endl;
            playercount++;
            cout<<"YOU WON "<<playercount<<" ROUND."<<endl;
            cout<<endl;
            
            if(playercount == 4)
            {
                cout<<"CONGRATULATION! YOU WON THIS GAME!"<<endl;
                goto restart3;
            }
        }
        
        else
        {
            cout<<"COMPUTER CHOOSED |SCISSORS|"<<endl;
            cout<<"THIS ROUND IS A TIE."<<endl;
            cout<<endl;
        }
        }
        
        else
        {
            cout<<"ENTERED INPUT IS INVALID\nENTER THE CORRECT INPUT!"<<endl<<endl;
            
            goto return2;
        }
    }
    while (compcount != 4 || playercount != 4);
   
    restart3:
    
    cout<<"\t\t\t\t**************************************************"<<endl;
    cout<<"\t\t\t\t*CONGRATULATION YOU MADE WITH SECOUND GAME TOO :)*"<<endl;
    cout<<"\t\t\t\t**************************************************"<<endl;                        
        
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
