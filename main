import string
import random
from time import sleep

matrix_dim = 20
clear = "\n" * 100
string.ascii_letters = 'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789'
matrix = []

def generate_matrix():
    row = []
    i = 0
    while i < matrix_dim:
        j = 0
        while j < matrix_dim:
            x = random.choice(string.ascii_letters)
            row.append(x)
            j += 1
        i += 1
        matrix.append(row)
        row = []

def print_matrix():
    k = 0
    while k < len(matrix):
        print(matrix[k])
        k += 1

def shuffle_matrix():
    k = 0
    while k < len(matrix):
        l = 0
        while l < len(matrix[k]):   
            z = random.randint(0,10)
            if z < 3:   # raise this value to increase random char generation
                matrix[k][l] = random.choice(string.ascii_letters)
            l += 1
        k += 1

def scroll_matrix():
    i = 1
    while i < len(matrix):
        matrix[i-1] = matrix[i]
        i += 1
    row = []
    j = 0
    while j < len(matrix):
        x = random.choice(string.ascii_letters)
        row.append(x)
        j += 1
    matrix[-1] = row

generate_matrix()

t = 0
while t < 100:
    print(clear)
    print_matrix()
    scroll_matrix()
    shuffle_matrix()
    sleep(0.5)
    print(clear)
    print_matrix()
    t += 1
