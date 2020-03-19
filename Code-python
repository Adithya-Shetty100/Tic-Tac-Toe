#To create a tic tac toe game
# Done by Adithya(Roll no.18/ SRN:PES1UG19EC009)

from random import *
from time import *


#To create and show board
board=['1','2','3',
       '4','5','6',
       '7','8','9']
 
def show():
    print (board[0],'|',board[1],'|',board[2])
    print("-----------")
    print (board[3],'|',board[4],'|',board[5])
    print("-----------")
    print (board[6],'|',board[7],'|',board[8])

print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~   Welcome to the TIC-TAC-TOE game !!!   ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
print()
show()
win=True
n1,name1,name2,n=' '*4

def computer():
    global n1,name1,n
    
    name1=input("Enter your name:")
    letter=int(input("Do you want 'X' or 'O'? \nEnter '1' for 'X' \nEnter '2' for 'O'\n"))
    if letter==1:
        n='X'
        n1='O'
    else:
        n='O'
        n1='X'
    print()
    print("The numbers on the board indicate the positions from 1-9\nEnjoy the GAME!!")
    show()
    print('You will be making the FIRST move!!\n\nIt is your turn!!')
    
    while win:

            p=int(input("Enter the position: "))
            if p<=9 and board[p-1]!='X' and board[p-1]!='O':
                board[p-1]=n
            else:
                 print("Sorry!! Invalid number ! Please Try again ! ")
                 continue
            show()
            print()
            winner()
            if win==False:
                break

            print("Now it is the computer's turn")
            sleep(2)
            comp=True
            while comp:
                p1=randint(0,8)
                if board[p1]!='X' and board[p1]!='O':
                    board[p1]=n1
                    comp=False
            print()
            
            show()
            winner()
            if win==False:
                break


def opponent():
    global n1,n,name1,name2
    
    print("Player1 will be making the FIRST move so enter accordingly")
    name1=input("Enter the name of player1:")
    name2=input("Enter the name of player2:")
    print()
    print("Since Player1 will be making the first move, Player2 gets chance for choosing the letter")
    print("So",name2,", do you want 'X' or 'O'? \nEnter '1' for 'X' \nEnter '2' for 'O'")
    letter=int(input())
    if letter==1:
        n1='X'
        n='O'
    else:
        n1='O'
        n='X'

    print("The numbers on the board indicate the positions from 1-9\nEnjoy the GAME!!")
    show()
    print()
    
    while win:

            p=int(input("Enter the position: "))
            if p<=9 and board[p-1]!='X' and board[p-1]!='O': 
                board[p-1]=n
            else:
                 print("Sorry!! Invalid number ! Please Try again ! ")
                 continue
            show()
            print()
            winner()
            if win==False:
                break

            
            p2=True
            while p2:
                p=int(input("Enter the position: "))
                if p<=9 and board[p-1]!='X' and board[p-1]!='O' :
                    board[p-1]=n1
                    p2=False
                else:
                     print("Sorry!! Invalid number ! Please Try again ! ")
            show()
            print()
            winner()
            if win==False:
                break


def winner():
    global win
    print()
    
    if (board[0]==board[1]==board[2]==n or board[3]==board[4]==board[5]==n or board[6]==board[7]==board[8]==n
    or board[0]==board[3]==board[6]==n or board[1]==board[4]==board[7]==n or board[2]==board[5]==board[8]==n 
    or board[0]==board[4]==board[8]==n or board[2]==board[4]==board[6]==n):
        if no_of_players==1:
            print(name1,"is the winner\n~~~~~~~~~~ CONGRATULATIONS!! ~~~~~~~~~~")
        else:
            print(name1," is the winner\n~~~~~~~~~~ CONGRATULATIONS!! ~~~~~~~~~~~") 
        win=False

    elif(board[0]==board[1]==board[2]==n1 or board[3]==board[4]==board[5]==n1 or board[6]==board[7]==board[8]==n1
    or board[0]==board[3]==board[6]==n1 or board[1]==board[4]==board[7]==n1 or board[2]==board[5]==board[8]==n1 
    or board[0]==board[4]==board[8]==n1 or board[2]==board[4]==board[6]==n1):
        if no_of_players==1:
            print("COMPUTER is the winner\n~~~~~~~~~~ YOU LOST!! Better Luck next time!! ~~~~~~~~~~")
        else:
            print(name2," is the winner\n~~~~~~~~~~ CONGRATULATIONS!! ~~~~~~~~~~~") 
        win=False

    elif(board[0]!='1' and board[1]!='2' and board[2]!='3' and board[3]!='4' and board[4]!='5' and board[5]!='6'
    and board[6]!='7' and board[7]!='8' and board[8]!='9'):
        print("The match is a draw\n~~~~~~~ WELL PLAYED!!! ~~~~~~~~")
        win=False


while True:
    print()
    no_of_players=int(input("Whom do you want to play against?\nEnter '1' for Computer\nEnter '2' for Player2\n"))
    if no_of_players==1 or  no_of_players==2:
        break
    else:
        print('Please enter a valid number!!')

if no_of_players==1:
    computer()
else:
    opponent()


