# 3-en-raya

Trabajo realizado por: Kelvin Andreé Caya Zeballos
Grupo 8
CCOMP1-3



def drawBoard(board):
Es el diseño del 3 en raya 

print('   |   |')
    print(' ' + board[7] + ' | ' + board[8] + ' | ' + board[9])
Con esta secuencia se crea todo el diseño del 3 en raya


def inputPlayerLetter():

    letter = ''
Esto es para que el jugador escoja su ficha, el letter con comillas sin nada es una variable vacia que toma un valor mas adelante ya se "X" o "O"

def whoGoesFirst():
    # Randomly choose the player who goes first.
Es la funcion para que ser decida aleatoriamente quien empieza primero

def makeMove(board, letter, move):
    board[move] = letter
Este es para definir el movimiento 


def isWinner(bo, le):

    return ((bo[7] == le and bo[8] == le and bo[9] == le) or 
estas son las combinaciones para que alguien gane 


def getBoardCopy(board):
Es cuando se hace un movimiento se copia de nuevo el tablero pero con la ficha ya puesta

def isSpaceFree(board, move):
 casillas  libres

def getPlayerMove(board):
Movimiento del jugador

def chooseRandomMoveFromList(board, movesList):
Almacena el nuemro de la coordenada

def getComputerMove(board, computerLetter):
Movimiento de la computadora

def isBoardFull(board):
Tablero lleno


    while gameIsPlaying:
        if turn == 'jugador':
            
            drawBoard(theBoard)
            move = getPlayerMove(theBoard)
            makeMove(theBoard, playerLetter, move)

            if isWinner(theBoard, playerLetter):
                drawBoard(theBoard)
                print('Hurraaa! Ganaste el juego!')
                gameIsPlaying = False
            else:
                if isBoardFull(theBoard):
                    drawBoard(theBoard)
                    print('Empate!')
                    break
                else:
                    turn = 'computadora'

        else:
            
            move = getComputerMove(theBoard, computerLetter)
            makeMove(theBoard, computerLetter, move)

            if isWinner(theBoard, computerLetter):
                drawBoard(theBoard)
                print('La computadora te derroto! Perdiste.')
                gameIsPlaying = False
            else:
                if isBoardFull(theBoard):
                    drawBoard(theBoard)
                    print('Empate!')
                    break
                else:
                    turn = 'jugador'

    
  Determinar si el jugar gana o pierde o si queda en empate con la computadora
