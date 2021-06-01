def solution(n=int, r=list, c=list):
    my_table = [[0 for row in range(n)] for column in range(n)]
    bombs_array = list()
    for num in range(len(r)):
        x = c[num]
        y = r[num]
        my_table[y][x] = 'B'
        bombs_array.append((y, x))

        # center right
        if (0 <= x <= n - 2) and (0 <= y <= n - 1):
            if my_table[y][x + 1] != 'B':
                my_table[y][x + 1] += 1

        # center left
        if (1 <= x <= n - 1) and (0 <= y <= n - 1):
            if my_table[y][x - 1] != 'B':
                my_table[y][x - 1] += 1

        # top left
        if (1 <= x <= n - 1) and (1 <= y <= n - 1):
            if my_table[y - 1][x - 1] != 'B':
                my_table[y - 1][x - 1] += 1

        # top right
        if (0 <= x <= n - 2) and (1 <= y <= n - 1):
            if my_table[y - 1][x + 1] != 'B':
                my_table[y - 1][x + 1] += 1

        # top center
        if (0 <= x <= n - 1) and (1 <= y <= n - 1):
            if my_table[y - 1][x] != 'B':
                my_table[y - 1][x] += 1

        # bottom right
        if (0 <= x <= n - 2) and (0 <= y <= n - 2):
            if my_table[y + 1][x + 1] != 'B':
                my_table[y + 1][x + 1] += 1

        # bottom left
        if (1 <= x <= n - 1) and (0 <= y <= n - 2):
            if my_table[y + 1][x - 1] != 'B':
                my_table[y + 1][x - 1] += 1

        # bottom center
        if (0 <= x <= n - 1) and (0 <= y <= n - 2):
            if my_table[y + 1][x] != 'B':
                my_table[y + 1][x] += 1

    for row in my_table:
        print("".join(str(cell) for cell in row))

    if len(bombs_array) > 0:
        print('The bombs are at locations:')
        for i in bombs_array:
            print(i, end=" ")
        print('\n')
    else:
        print('There are no bombs.')


if __name__ == '__main__':
    solution(n=3, r=[2, 1, 0, 2], c=[0, 2, 1, 2])
    solution(n=5, r=[2, 3, 2, 3, 1, 1, 3, 1], c=[3, 3, 1, 1, 1, 2, 2, 3])
    solution(n=2, r=[], c=[])
