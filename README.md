#include <iostream>
#include <string>
#include <cstdlib>
#include <ctime>

using namespace std;

int main()
{

                                //WELLCOMING THE PLAYER.
    
    cout<<"\t\t\t\t***************************"<<endl;
    cout<<"\t\t\t\t*WELLCOME TO LESTRO WORLD.*\t\t"<<endl;
    cout<<"\t\t\t\t***************************"<<endl;
    
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
    cout<<"\t\t\t    WELLCOME TO SQUID GAME "<<name<<" :)\t\t"<<endl;
    
    cout<<"\t\t\t    ALLTOGETHER THEIR ARE 4 GAMES."<<endl<<endl;
    
                                //FIRST GAME.
                                
    restart24:
                                
    cout<<"\t\t\t\t__________________________"<<endl<<endl;
    cout<<"\t\t\t\t  WELLCOME TO FIRST GAME."<<endl<<endl;
    cout<<"\t\t\t\t__________________________"<<endl<<endl;
    
    cout<<"\t\t\t     GAME1: RED LIGHT - GREEN LIGHT."<<endl<<endl;
    
    cout<<"\t\t\tHI "<<name<<"! I HAVE SET A NUMBER IN MY MIND\n\t\t\tBETWEEN 1 TO 100.YOU HAVE 8 CHANCE TO GUESS\n\t\t\tMY NUMBER.BUT IF YOU DIDN'T GUESSED THE NUMBER\n\t\t\tWITHIN 8 CHANCE,YOU WILL BE ELIMINATED FROM THE GAME!"<<endl;
    
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
		    cout<<"CONGRATULATIONS YOU GUESSED IN "<<tries<<" TRIES!"<<endl<<endl;
		    goto restart4;
		}
		
		else{
		    cout<<name<<" YOU ARE ELIMINATED!"<<endl;
		    
		    restart23:
                
                char  yono;
                
                cout<<"STILL WANT TO PLAY?"<<endl;
                cin>>yono;
                
                if(yono == 'y' || yono == 'Y')
                {
                    goto restart24; 
                }
                
                else if(yono == 'n' || yono == 'N')
                {
                    return 0;
                }
                
                else
                {
                    cout<<"ENTER THE CORRECT INPUT"<<endl;
                    cout<<endl;
                    goto restart23;
                }
		}
		
		restart4:
		
		cout<<"\t\t\t********************************************"<<endl;
        cout<<"\t\t\t*CONGRATULATION YOU MADE WITH FIRST GAME :)*"<<endl;
        cout<<"\t\t\t********************************************"<<endl;
        
        
                                //SECOUND GAME
                                
        restart19:
        
        cout<<"\t\t\t\t____________________________"<<endl<<endl;       
        cout<<"\t\t\t\t  WELLCOME TO SECOUND GAME."<<endl<<endl;
        cout<<"\t\t\t\t____________________________"<<endl<<endl;
    
        cout<<"\t\t\t        GAME2: ROCK-PAPER-SCISSOR."<<endl<<endl;

        cout << "\t\t\tTHE RULES OF THIS GAME ARE THE FOLLOWING: " <<endl<<endl;
        cout << "\t\t\tA) THIS GAME WILL BE THE BEST OUT 4." <<endl;
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
                cout<<"\t\t\t\t"<<name<<" YOU ARE ELIMINATED!"<<endl;
                
                restart22:
                
                char  yono;
                
                cout<<"STILL WANT TO PLAY?"<<endl;
                cin>>yono;
                
                if(yono == 'y' || yono == 'Y')
                {
                    goto restart19; 
                }
                
                else if(yono == 'n' || yono == 'N')
                {
                    return 0;
                }
                
                else
                {
                    cout<<"ENTER THE CORRECT INPUT"<<endl;
                    cout<<endl;
                    goto restart22;
                }
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
                cout<<"CONGRATULATION "<<name<<"! YOU WON THIS GAME!"<<endl;
                goto restart3;
                cout<<endl<<endl;
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
                cout<<"CONGRATULATION "<<name<<"! YOU WON THIS GAME!"<<endl;
                goto restart3;
                cout<<endl<<endl;
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
                cout<<"\t\t\t\t "<<name<<" YOU ARE ELIMINATED!"<<endl;
                
                restart20:
                
                char yono;
                
                cout<<"STILL WANT TO PLAY?"<<endl;
                cin>>yono;
                
                if(yono == 'y' || yono == 'Y')
                {
                    goto restart19; 
                }
                
                else if(yono == 'n' || yono == 'N')
                {
                    return 0;
                }
                
                else
                {
                    cout<<"ENTER THE CORRECT INPUT"<<endl;
                    cout<<endl;
                    goto restart20;
                }
            }
        }
            
                                    //YOU CHOOSED SCISSORS
            
        }
        
        else if(pick == 's')
        {
            cout<<"YOU CHOOSED |SCISSORS|"<<endl;
            compchoice = rand () % 3 + 3;
        
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
                cout<<"\t\t\t\t "<<name<<" YOU ARE ELIMINATED!"<<endl;
               
                restart21:
                
                char yono;
                
                cout<<"STILL WANT TO PLAY?"<<endl;
                cin>>yono;
                
                if(yono == 'y' || yono == 'Y')
                {
                    goto restart19; 
                }
                
                else if(yono == 'n' || yono == 'N')
                {
                    return 0;
                }
                
                else
                {
                    cout<<"ENTER THE CORRECT INPUT"<<endl;
                    cout<<endl;
                    goto restart21;
                }
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
                cout<<"CONGRATULATION "<<name<<"! YOU WON THIS GAME!"<<endl;
                goto restart3;
                cout<<endl<<endl;
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
    
    cout<<endl;
    cout<<"\t\t\t**************************************************"<<endl;
    cout<<"\t\t\t*CONGRATULATION YOU MADE WITH SECOUND GAME TOO :)*"<<endl;
    cout<<"\t\t\t**************************************************"<<endl; 
    
                                //THIRD GAME
    
    cout<<"\t\t\t\t____________________________"<<endl<<endl;
    cout<<"\t\t\t\t   WELLCOME TO THIRD GAME.  "<<endl<<endl;
    cout<<"\t\t\t\t____________________________"<<endl<<endl;
    
    cout<<"\t\t         GAME3: GLASS STEPPING STONE BRIDGE"<<endl<<endl;
    
    cout << "\t\t\tTHE RULES OF THIS GAME ARE THE FOLLOWING: " <<endl<<endl;
    cout << "\t\t\tA) THIS GAME HAS GLASSES OF 2 ROW'S." <<endl;
    cout << "\t\t\tB) EACH COLUMN HAS 2 GLASS WITH 7 COLUMNS." <<endl;
    cout << "\t\t\tC) ALTERNATELY ONE OF THEM IS TEMPERED GLASS AND REGULAR GLASS." <<endl;
    cout << "\t\t\tD) IF YOU STEPED ON REGULAR GLASS YOU WILL BE ELIMINATED." <<endl<<endl;
    
    int glass, side, glasscount (0), columncount (0);
    srand(time(0));
    
    restart7:
    
    restart8:
    
    restart11:
    
                                //CHOOSE THE GLASS
    
    columncount++;
    cout<<"CHANCE NO : "<<columncount<<endl;
    cout<<"CHOOSE THE GLASS TO STEP : 1 - RIGHT GLASS."<<endl;
    cout<<"                           2 - LEFT GLASS."<<endl;
    
    cin>>glass;
    
                                //RIGHT GLASS CHOOSED
    
    if(glass == 1)
    {
        cout<<"YOU CHOOSED |RIGHT SIDE GLASS|"<<endl;
        side = rand() % 2 ;
        cout<<endl;
        
        if(side == 1)
        {
            cout<<"YOU STEPED ON TEMPERED GLASS."<<endl;
            glasscount++;
            cout<<"GOOD! YOU PASSED "<<glasscount<<" CLOUMN GLASS."<<endl;
            cout<<endl;
            
            if(glasscount == 7)
            {
                cout<<"CONGRATULATIONS! YOU PASSED ALL 7 COLUMNS GLASS."<<endl;
                goto restart6;
            }
            
            goto restart7;
            
        }
        
        else
        {
            cout<<"OPS....YOU STEPED ON REGULAR GLASS."<<endl;
            cout<<"YOU ARE ELIMINATED!"<<endl;
            cout<<endl;
            
            restart9:
            
            cout<<"STILL YOU WANT TO CONTINUE THE GAME."<<endl;
            cout<<"ENTER : y-YES OR n-NO."<<endl;
            
            char yeno;
            
            cin>>yeno;
            
            if(yeno == 'y' || yeno == 'Y')
            {
                goto restart8;
                cout<<endl;
            }
            
            else if(yeno == 'n' || yeno == 'N')
            {
                return 0;
            }
            
            else
            {
                cout<<"ENTER THE CORRECT INPUT."<<endl;
                goto restart9;
            }
           
        }
    }
    
                                //LEFT GLASS CHOOSED
    
    else if(glass == 2)
    {
        cout<<"YOU CHOOSED |LEFT SIDE GLASS|"<<endl;
        side = rand() % 2 ;
        cout<<endl;
        
        if(side == 1)
        {
            cout<<"YOU STEPED ON TEMPERED GLASS."<<endl;
            glasscount++;
            cout<<"GOOD! YOU PASSED "<<glasscount<<" CLOUMN GLASS."<<endl;
            cout<<endl;
            
            if(glasscount == 7)
            {
                cout<<"CONGRATULATIONS! YOU PASSED ALL 7 COLUMNS GLASS."<<endl;
                goto restart6;
            }
            
            goto restart7;
            cout<<endl;
            
        }
        
        else
        {
            cout<<"OPS....YOU STEPED ON REGULAR GLASS."<<endl;
            cout<<"YOU ARE ELIMINATED!"<<endl;
            cout<<endl;
            
            restart10:
            
            cout<<"STILL YOU WANT TO CONTINUE THE GAME."<<endl;
            cout<<"ENTER : y-YES OR n-NO."<<endl;
            
            char yeno;
            
            cin>>yeno;
            
            if(yeno == 'y' || yeno == 'Y')
            {
                goto restart8;
                cout<<endl;
            }
            
            else if(yeno == 'n' || yeno == 'N')
            {
                return 0;
            }
            
            else
            {
                cout<<"ENTER THE CORRECT INPUT."<<endl;
                goto restart10;
            }
        }
        
    }
    
    else
    {
        cout<<"ENTERED INPUT IS INCORRECT\nRE-ENTER."<<endl;
        goto restart11;
    }
    
        restart6:
        
        cout<<"\t\t\t***********************************************"<<endl;
        cout<<"\t\t\t*CONGRATULATION YOU MADE WITH THIRD GAME TOO:)*"<<endl;
        cout<<"\t\t\t***********************************************"<<endl;
        
        
        
                                //FOURTH GAME.
                    
                    
        restart26:                         
                                
        cout<<"\t\t\t\t____________________________"<<endl<<endl;       
        cout<<"\t\t\t\t  WELLCOME TO FOURTH GAME."<<endl<<endl;
        cout<<"\t\t\t\t____________________________"<<endl<<endl;
    
        cout<<"\t\t\t\t       GAME4: MARBLES."<<endl<<endl;

        cout << "\t\t\tTHE RULES OF THIS GAME ARE THE FOLLOWING: " <<endl<<endl;
        cout << "\t\t\tA) YOU WILL HAVE 10 MARBELS WITH YOU." <<endl;
        cout << "\t\t\tB) COMPUTER(HIS NAME IS -PROGU) WILL HAVE 10 MARBELS WITH HIM TOO." <<endl;
        cout << "\t\t\tC) YOU WILL KEEP SOME NUMBERS OF MARBLES IN YOUR HAND CLOSED." <<endl;
        cout << "\t\t\tD) THEN PROGU WILL GUESS IF THE MARBLE NUMBERS ARE EVEN OR ODD." <<endl;
        cout << "\t\t\tE) IF HE GUESS IT CORRECT YOU HAVE TO GIVE HIM THE MARBLES YOU HAVE. " <<endl;
        cout << "\t\t\tG) THIS WILL CONTINUE UNTIL ONE OF THE PLAYER WILL BE OUT OF MARBLES. " <<endl<<endl;
    
    
        int pleftmarble, cleftmarble;
        int pmarblenum, cmarblenum; 
        int compchoices;
        srand(time(0));
        
        cout<<"PLEASE ENTER 10 : ";
        cin>>pleftmarble;
        cout<<endl;
        
        cleftmarble = pleftmarble;
        
        cout<<"YOU HAVE "<<pleftmarble<<" MARBLES WITH YOU."<<endl;
        cout<<endl;
        
        
        restart13:
        
        restart14:
        
        restart16:
        
                                //ASKING FOR HOLDING THE MARBLE
        
        cout<<"HOW MUCH MARBLE YOU WANT IN YOUR HAND?"<<endl;
        cin>>pmarblenum;
        cout<<endl;
        
                                //DON'T HAVE MARBLE
        
        if(pmarblenum > pleftmarble)
        {
            cout<<"YOU DON'T HAVE THIS MUCH MARBLE."<<endl;
            cout<<"RE-ENTER"<<endl<<endl;
            goto restart13;
        }
        
                                //DON'T HAVE MARBLE
        
        else if(pmarblenum < 1)
        {
            cout<<"YOU CAN'T PLAY EMPTY HAND."<<endl;
            cout<<endl;
            goto restart14;
        }
        
                                //HAVE MARBLES
        
        else if(pmarblenum <= pleftmarble && pmarblenum >= 1)
        {
            pleftmarble = pleftmarble - pmarblenum;
            
            cout<<"YOU HOLD "<<pmarblenum<<" MARBLE WITH YOU."<<endl;
            
            restart18:
            
            cmarblenum = rand() % 10;
            
            if(cmarblenum > cleftmarble)
            {
                goto restart18;
            }
            
            else if(cmarblenum < 1)
            {
                goto restart18;
            }
            
            else{
            
            cleftmarble = cleftmarble - cmarblenum;
            
            cout<<"PROGU HOLD SOME MARBLE IN HIS HAND."<<endl;
            cout<<endl;
            
            compchoices = rand() % 2;
            
                                //COMPUTER CHOOSED EVEN NUMBER
            
            if(compchoice == 1)
            {
                cout<<"PROGU CHOOSED EVEN NUMBER."<<endl;
                cout<<endl;
                
                                //MY NUMBER IS EVEN
                
                if(pmarblenum % 2 == 0)
                {
                    cout<<"PROGU IS HOLDING "<<cmarblenum<<" MARBLE WITH HIM."<<endl;
                    cout<<endl;
                    
                    cout<<"YOUR NUMBER IS EVEN."<<endl<<endl;
                    
                    cout<<"PROGU WIN THIS ROUND."<<endl;
                    cout<<endl;
                    
                    cleftmarble = cleftmarble + cmarblenum + pmarblenum;
                    
                    cout<<"NOW PROGU HAVE "<<cleftmarble<<" MARBLE WITH HIM."<<endl;
                    
                    pleftmarble = pmarblenum + pleftmarble - pmarblenum;
                    
                    cout<<"NOW YOU HAVE "<<pleftmarble<<" MARBLE WITH YOU."<<endl;
                    
                                //COMPUTER OUT OF MARBLE
                    
                    if(cleftmarble < 1)
                    {
                        cout<<"PROGU HAS BEEN ELIMINATED."<<endl;
                        cout<<endl;
                        
                        goto restart17;
                    }
                    
                                //COMPUTER WIN 
                    
                    else if(cleftmarble == 20)
                    {
                        cout<<endl;
                        cout<<"PROGU WON THIS GAME!"<<endl<<endl;
                        cout<<"YOU HAS BEEN ELIMINATED."<<endl;
                        
                        restart25:
                
                        char  yono;
                        
                        cout<<"STILL WANT TO PLAY?"<<endl;
                        cin>>yono;
                        
                        if(yono == 'y' || yono == 'Y')
                        {
                            goto restart26; 
                        }
                        
                        else if(yono == 'n' || yono == 'N')
                        {
                            return 0;
                        }
                        
                        else
                        {
                            cout<<"ENTER THE CORRECT INPUT"<<endl;
                            cout<<endl;
                            goto restart25;
                        }
                    }
                    
                                //PLAY AGAIN
                    
                    else
                    {
                        cout<<"\t\t\t\t____________________________"<<endl<<endl;       
                        cout<<"\t\t\t\t  NO ONE WIN - NEXT ROUND."<<endl<<endl;
                        cout<<"\t\t\t\t____________________________"<<endl<<endl;
                        cout<<endl;
                        goto restart16;
                    }
                    
                    
                    
                                //I AM OUT OF MARBLE
                    
                    if(pleftmarble < 1)
                    {
                        cout<<"YOU ARE ELIMINATED."<<endl;
                        cout<<endl;
                        
                        restart27:
                
                        char  yono;
                        
                        cout<<"STILL WANT TO PLAY?"<<endl;
                        cin>>yono;
                        
                        if(yono == 'y' || yono == 'Y')
                        {
                            goto restart26; 
                        }
                        
                        else if(yono == 'n' || yono == 'N')
                        {
                            return 0;
                        }
                        
                        else
                        {
                            cout<<"ENTER THE CORRECT INPUT"<<endl;
                            cout<<endl;
                            goto restart27;
                        }
                    }
                    
                                //I  WIN 
                    
                    else if(pleftmarble == 20)
                    {
                        cout<<endl;
                        goto restart17;
                    }
                    
                                //PLAY AGAIN
                    
                    else
                    {
                        cout<<"\t\t\t\t____________________________"<<endl<<endl;       
                        cout<<"\t\t\t\t  NO ONE WIN - NEXT ROUND."<<endl<<endl;
                        cout<<"\t\t\t\t____________________________"<<endl<<endl;
                        cout<<endl;
                        goto restart16;
                    }
                    
                }
                
                            //MY NUMBER IS ODD
                
                else{
                    cout<<"PROGU IS HOLDING "<<cmarblenum<<" MARBLE WITH HIM."<<endl;
                    cout<<endl;
                    
                    cout<<"YOUR NUMBER IS ODD."<<endl<<endl;
                    
                    cout<<"YOU WIN THIS ROUND."<<endl;
                    cout<<endl;
                    
                    pleftmarble = pmarblenum + pleftmarble + cmarblenum;
                    
                    cout<<"NOW YOU HAVE "<<pleftmarble<<" MARBLE WITH YOU."<<endl;
                    
                    cleftmarble = cmarblenum + cleftmarble - cmarblenum;
                    
                    cout<<"NOW PROGU HAVE "<<cleftmarble<<" MARBLE WITH HIM."<<endl;
                    
                    
                                //I AM OUT OF MARBLE
                    
                    if(pleftmarble < 1)
                    {
                        cout<<"YOU ARE ELIMINATED."<<endl;
                        cout<<endl;
                        
                        restart28:
                
                        char  yono;
                        
                        cout<<"STILL WANT TO PLAY?"<<endl;
                        cin>>yono;
                        
                        if(yono == 'y' || yono == 'Y')
                        {
                            goto restart26; 
                        }
                        
                        else if(yono == 'n' || yono == 'N')
                        {
                            return 0;
                        }
                        
                        else
                        {
                            cout<<"ENTER THE CORRECT INPUT"<<endl;
                            cout<<endl;
                            goto restart28;
                        }
                    }
                    
                                //I  WIN 
                    
                    else if(pleftmarble == 20)
                    {
                        cout<<endl;
                        goto restart17;
                    }
                    
                                //PLAY AGAIN
                    
                    else
                    {
                        cout<<"\t\t\t\t____________________________"<<endl<<endl;       
                        cout<<"\t\t\t\t  NO ONE WIN - NEXT ROUND."<<endl<<endl;
                        cout<<"\t\t\t\t____________________________"<<endl<<endl;
                        cout<<endl;
                        goto restart16;
                    }
                    
                    
                                //COMPUTER OUT OF MARBLE
                    
                    if(cleftmarble < 1)
                    {
                        cout<<"PROGU HAS BEEN ELIMINATED."<<endl;
                        cout<<endl;
    
                        goto restart17;
                    }
                    
                                //COMPUTER WIN 
                    
                    else if(cleftmarble == 20)
                    {
                        cout<<endl;
                        cout<<"PROGU WON THIS GAME!"<<endl<<endl;
                        cout<<"YOU HAS BEEN ELIMINATED."<<endl;
                        
                        restart29:
                
                        char  yono;
                        
                        cout<<"STILL WANT TO PLAY?"<<endl;
                        cin>>yono;
                        
                        if(yono == 'y' || yono == 'Y')
                        {
                            goto restart26; 
                        }
                        
                        else if(yono == 'n' || yono == 'N')
                        {
                            return 0;
                        }
                        
                        else
                        {
                            cout<<"ENTER THE CORRECT INPUT"<<endl;
                            cout<<endl;
                            goto restart29;
                        }
                    }
                    
                                //PLAY AGAIN
                    
                    else
                    {
                        cout<<"\t\t\t\t____________________________"<<endl<<endl;       
                        cout<<"\t\t\t\t  NO ONE WIN - NEXT ROUND."<<endl<<endl;
                        cout<<"\t\t\t\t____________________________"<<endl<<endl;
                        cout<<endl;
                        goto restart16;
                    }
                }
            }
            
                                //COMPUTER CHOOSED ODD NUMBER
            
            else
            {
                cout<<"PROGU CHOOSED ODD NUMBER."<<endl;
                cout<<endl;
                
                                //MY NUMBER IS EVEN
                
                if(pmarblenum % 2 == 0)
                {
                    cout<<"PROGU IS HOLDING "<<cmarblenum<<" MARBLE WITH HIM."<<endl;
                    cout<<endl;
                    
                    cout<<"YOUR NUMBER IS EVEN."<<endl<<endl;
                    
                    cout<<"YOU WIN THIS ROUND."<<endl;
                    cout<<endl;
                    
                    pleftmarble = pmarblenum + pleftmarble + cmarblenum;
                    
                    cout<<"NOW YOU HAVE "<<pleftmarble<<" MARBLE WITH YOU."<<endl;
                    
                    cleftmarble = cmarblenum + cleftmarble - cmarblenum;
                    
                    cout<<"NOW PROGU HAVE "<<cleftmarble<<" MARBLE WITH HIM."<<endl;
                    
                                //I AM OUT OF MARBLE
                    
                    if(pleftmarble < 1)
                    {
                        cout<<"YOU ARE ELIMINATED."<<endl;
                        cout<<endl;
                        
                        restart30:
                
                        char  yono;
                        
                        cout<<"STILL WANT TO PLAY?"<<endl;
                        cin>>yono;
                        
                        if(yono == 'y' || yono == 'Y')
                        {
                            goto restart26; 
                        }
                        
                        else if(yono == 'n' || yono == 'N')
                        {
                            return 0;
                        }
                        
                        else
                        {
                            cout<<"ENTER THE CORRECT INPUT"<<endl;
                            cout<<endl;
                            goto restart30;
                        }
                    }
                    
                                //I  WIN 
                    
                    else if(pleftmarble == 20)
                    {
                        cout<<endl;
                        goto restart17;
                    }
                    
                                //PLAY AGAIN
                    
                    else
                    {
                        cout<<"\t\t\t\t____________________________"<<endl<<endl;       
                        cout<<"\t\t\t\t  NO ONE WIN - NEXT ROUND."<<endl<<endl;
                        cout<<"\t\t\t\t____________________________"<<endl<<endl;
                        cout<<endl;
                        goto restart16;
                    }
                    
                    
                    
                                //COMPUTER OUT OF MARBLE
                    
                    if(cleftmarble < 1)
                    {
                        cout<<"PROGU HAS BEEN ELIMINATED."<<endl;
                        cout<<endl;
                        
                        goto restart17;
                    }
                    
                                //COMPUTER WIN 
                    
                    else if(cleftmarble == 20)
                    {
                        cout<<endl;
                        cout<<endl;
                        cout<<"PROGU WON THIS GAME!"<<endl<<endl;
                        cout<<"YOU HAS BEEN ELIMINATED."<<endl;
                        
                        restart31:
                
                        char  yono;
                        
                        cout<<"STILL WANT TO PLAY?"<<endl;
                        cin>>yono;
                        
                        if(yono == 'y' || yono == 'Y')
                        {
                            goto restart26; 
                        }
                        
                        else if(yono == 'n' || yono == 'N')
                        {
                            return 0;
                        }
                        
                        else
                        {
                            cout<<"ENTER THE CORRECT INPUT"<<endl;
                            cout<<endl;
                            goto restart31;
                        }
                    }
                    
                                //PLAY AGAIN
                    
                    else
                    {
                        cout<<"\t\t\t\t____________________________"<<endl<<endl;       
                        cout<<"\t\t\t\t  NO ONE WIN - NEXT ROUND."<<endl<<endl;
                        cout<<"\t\t\t\t____________________________"<<endl<<endl;
                        cout<<endl;
                        goto restart16;
                    }
                    
                }
                
                                //MY NUMBER IS ODD
                
                else{
                    cout<<"PROGU IS HOLDING "<<cmarblenum<<" MARBLE WITH HIM."<<endl;
                    cout<<endl;
                    
                    cout<<"YOUR NUMBER IS ODD."<<endl<<endl;
                    
                    cout<<"PROGU WIN THIS ROUND."<<endl;
                    cout<<endl;
                    
                    cleftmarble = cleftmarble + cmarblenum + pmarblenum;
                    
                    cout<<"NOW PROGU HAVE "<<cleftmarble<<" MARBLE WITH HIM."<<endl;
                    
                    pleftmarble = pmarblenum + pleftmarble - pmarblenum;
                    
                    cout<<"NOW YOU HAVE "<<pleftmarble<<" MARBLE WITH YOU."<<endl;
                    
                                //COMPUTER OUT OF MARBLE
                    
                    if(cleftmarble < 1)
                    {
                        cout<<"PROGU HAS BEEN ELIMINATED."<<endl;
                        cout<<endl;
                        
                        goto restart17;
                    }
                    
                                //COMPUTER WIN 
                    
                    else if(cleftmarble == 20)
                    {
                        cout<<endl;
                        cout<<"PROGU WON THIS GAME!"<<endl<<endl;
                        cout<<"YOU HAS BEEN ELIMINATED."<<endl;
                        
                        restart32:
                
                        char  yono;
                        
                        cout<<"STILL WANT TO PLAY?"<<endl;
                        cin>>yono;
                        
                        if(yono == 'y' || yono == 'Y')
                        {
                            goto restart26; 
                        }
                        
                        else if(yono == 'n' || yono == 'N')
                        {
                            return 0;
                        }
                        
                        else
                        {
                            cout<<"ENTER THE CORRECT INPUT"<<endl;
                            cout<<endl;
                            goto restart32;
                        }
                    }
                    
                                //PLAY AGAIN
                    
                    else
                    {
                        cout<<"\t\t\t\t____________________________"<<endl<<endl;       
                        cout<<"\t\t\t\t  NO ONE WIN - NEXT ROUND."<<endl<<endl;
                        cout<<"\t\t\t\t____________________________"<<endl<<endl;
                        cout<<endl;
                        goto restart16;
                    }
                    
                    
                    
                                //I AM OUT OF MARBLE
                    
                    if(pleftmarble < 1)
                    {
                        cout<<"YOU ARE ELIMINATED."<<endl;
                        
                        restart33:
                
                        char  yono;
                        
                        cout<<"STILL WANT TO PLAY?"<<endl;
                        cin>>yono;
                        
                        if(yono == 'y' || yono == 'Y')
                        {
                            goto restart26; 
                        }
                        
                        else if(yono == 'n' || yono == 'N')
                        {
                            return 0;
                        }
                        
                        else
                        {
                            cout<<"ENTER THE CORRECT INPUT"<<endl;
                            cout<<endl;
                            goto restart33;
                        }
                        
                        return 0;
                    }
                    
                                //I  WIN 
                    
                    else if(pleftmarble == 20)
                    {
                        cout<<endl;
                        goto restart17;
                    }
                    
                                //PLAY AGAIN
                    
                    else
                    {
                        cout<<"\t\t\t\t____________________________"<<endl<<endl;       
                        cout<<"\t\t\t\t  NO ONE WIN - NEXT ROUND."<<endl<<endl;
                        cout<<"\t\t\t\t____________________________"<<endl<<endl;
                        cout<<endl;
                        goto restart16;
                    }
                    
                }
            }
            
            
            
        }
        
         restart17:
         
        cout<<"\t\t\t************************************************"<<endl;
        cout<<"\t\t\t*CONGRATULATION YOU MADE WITH FOURTH GAME TOO:)*"<<endl;
        cout<<"\t\t\t************************************************"<<endl;
        
    }
    
                            //NOT WILLING TO PLAY THE GAME.
    
    else if(choice == 0)
    {
        cout<<"\t\t\t\tI THINK YOU ARE AFRAID TO PLAY\t\t"<<endl;
        cout<<"\t\t\t\t            BYE\t\t"<<endl;
        cout<<"\t\t\t\t        "<<name<<"            \t\t"<<endl;
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
}
