# Game-Generation
#Generation of ROCK PAPER SCISSORS Game


import random
print("Rules for ROCK-PAPER-SCISSORS Game : \n Paper vs Rock : Paper wins \n"
      "Rock vs Scissors : Rock wins \n Scissors vs Paper : Scissors wins") 
while True:
    print("Select your choice : \n 1. Rock \n 2. Paper \n 3. Scissors")
    ch=int(input("Select your choice:"))
     
    while ch >3 or ch< 1:
        ch=int(input("Select a valid choice: "))
         
    if ch==1:
        selected_ch = "Rock"
    elif ch==2:
        selected_ch ="Paper"
    else:
        selected_ch= "Scissors"
        
    print("User choice", selected_ch)
    print("Computer Turn...")
    comp_ch= random.randint(1, 3)

    while comp_ch==ch:
        comp_ch= random.randint(1, 3)
        
    if comp_ch==1:
        comp_choice ="Rock"
    elif comp_ch==2:
        comp_choice ="Paper"
    else:
        comp_choice ="Scissors"

    print("Computer choice:", comp_ch)
    print(selected_ch, 'VS', comp_choice)

    if ch==comp_ch:
        print("Its a Draw", end="")
        result= "DRAW"

    if (ch==1 and comp_ch==2):
        print('paper wins \n', end=" ")
        result ="Paper"
    elif (ch== 2 and comp_ch==1):
        print("paper wins \n", end=" ")
        result ="Paper"
    elif (ch==1 and comp_ch ==3):
        print("Rock wins \n", end=" ")
        result ="Rock"
    elif (ch ==3 and comp_ch== 1):
        print("Rock wins \n", end=" ")
        result ="Rock"
    elif (ch== 2 and comp_ch==3):
        print("Scissors wins \n", end=" ")
        result ="Scissors"
    elif(ch==3 and comp_ch==2):
        print("Scissors wins\n", end=" ")
        result="Scissors"
            
    if result =="Draw":
        print("## Its a tie ##")
    if result== comp_ch:
        print(" ##Computer wins ##")
    else:
        print(" ## User wins ##")
        print("Do you want to play again? (Yes/No)")

    again=input().lower() 
    if again =='no':
        break

print("Game is completed: Thanks for playing")


