def print_board(board):
    for row in board:
        print("|".join(row))
        print("-----")
def check_winner(board):

    for row in board:
        if row.count(row[0]) == len(row) and row[0] != " ":
            return True

    for col in range(len(board[0])):
        if (
            board[0][col] == board[1][col]
            == board[2][col]
            != " "
        ):
            return True

    if (
        board[0][0] == board[1][1]
        == board[2][2]
        != " "
    ):
        return True

    if (
        board[0][2] == board[1][1]
        == board[2][0]
        != " "
    ):
        return True

    return False

def play_game():
    board = [[" " for _ in range(3)] for _ in range(3)]
    player = "X"

    while True:
        print_board(board)
        row = int(input("Введіть номер рядка (0, 1 або 2): "))
        col = int(input("Введіть номер стовпця (0, 1 або 2): "))

        if board[row][col] == " ":
            board[row][col] = player

            if check_winner(board):
                print(f"Гравець {player} виграв!")
                break

            player = "O" if player == "X" else "X"
        else:
            print("Ця клітинка уже зайнята")

play_game()
