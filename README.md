import random 
def rock_paper_scissor_Tülin_Seymenoğlu():
    print("********** Welcome to the Rock-Paper-Scissors Game **********")
    print("***************************************************************")
    print("The rules of the game are simple. Rock beats paper, scissors beats rock, paper beats rock. The player who wins two rounds wins the game. Have fun.")
    print("***************************************************************")     
    options=["rock","paper","scissors"]
    while True:
            player_victory=0
            computer_victory=0
            round=1
            while player_victory <2 and computer_victory<2:
                print(f"\n{round}.Round")
                print("If you want to exit the game, type 'exit'.")
                player_choice=input("Please make your selection(Rock-Paper-Scissors:) ").lower()
                if player_choice=="exit" :
                    print("Exiting the game.....")
                    print("***************************************************************")
                    return
                if player_choice not in options:
                    print("Please make a valid selection.")
                    continue
                computer_choice=random.choice(options)
                print(f"Selection of computer:{computer_choice}")
                if player_choice==computer_choice:
                    print("Tie!")
                    print("***************************************************************")
                elif(player_choice=="rock" and computer_choice=="scissors") or \
                    (player_choice=="scissors"and computer_choice=="paper") or \
                    (player_choice=="paper" and computer_choice=="scissors"):                       
                        print("Congratulations you won this round ☺☺☺")
                        player_victory+=1
                        print("***************************************************************")
                else:
                    print("The computer won this round.")
                    print("***************************************************************")
                    computer_victory +=1
                round +=1
            if player_victory==2:
                print("Game over!")
                print("You won ☺☺☺")
                print("***************************************************************")
                
            else:
                print("Game over!")
                print("Computer won")
            game=input("Do you want to play another game?(yes/no):").lower()
            if game!="yes":
                print("Game over..... ")
                print("Thank you ☺☺☺☺☺")
                print("***************************************************************")
                break
rock_paper_scissor_Tülin_Seymenoğlu()                
                        
            
            

