maps_size = 3

maps = [1, 2, 3,
        4, 5, 6,
        7, 8, 9]

def draw_maps():
    print("_" * maps_size * 4)
    for i in range(maps_size):
        print((' ' * 3 + '|') * 3)
        print("", maps[i * 3], '|', maps[1 + i * 3], '|', maps[2 + i * 3], '|')
        print(("_" * 3 + '|') * 3)
    pass

def game_step(index, char):
    if (index > 9 or index < 1 or maps[index - 1] in ("X", "O")):
        return False
    maps[index - 1] = char
    return True

def check_win():
    win = False

    win_game = [[0, 1, 2],
                [3, 4, 5],
                [6, 7, 8],
                [0, 3, 6],
                [1, 4, 7],
                [2, 5, 8],
                [0, 4, 8],
                [2, 4, 6]]

    for pos in win_game:
        if (maps[pos[0]] == maps[pos[1]] and maps[pos[1]] == maps[pos[2]]):
            win = maps[pos[0]]

    return win

def start_game():
    player = 'X'
    step = 1
    draw_maps()
    while (step < 10) and (check_win() == False):
        index = int(input("Сделайте ваш ход: "))

        if (index) == 0:
            break

        if (game_step(int(index), player)):
            print("Удачный ход")

            if (player == 'X'):
                player = 'O'
            else:
                player = 'X'

            draw_maps()
            step += 1
        else:
            print("Неверный ход, повторите!")

    if (step == 10):
        print("Ничья!")
    print("Выиграл " + check_win())


print('Добро пожаловать в игру!')
start_game()
