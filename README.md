# module7.py
# Assignment 7
# Oluwapelumi Omidiji
# 11/11/2024

import turtle
import math


def areaOfCircle(r):
    return math.pi * (r ** 2)
        
def check_number(n, arr):
    return n in arr

def list_multiplication(arr):
    result = 1
    for num in arr:
        result *= num
    return result
    
def list_multiplication_recursive(arr):
    if len(arr) == 0:
        return 1
    return arr[0] * list_multiplication_recursive(arr[1:])
    
def get_unique(arr):
    return list(set(arr))
    
def drawSquare(t, sz) :
    for _ in range(4):
        t.forward (sz)
        t.left(90)

def main():
    r = 3
    n = 9
    print("Area of Circle:", areaOfCircle(r))
    print("Is number in range:", check_number(n, [1,2,3,4,5,6,7,8,9,10]))
    print("List Multiplication:", list_multiplication([1,2,3,4]))
    print("Unique Elements:", get_unique([1, 2, 2, 3, 4, 4, 5]))

    wn = turtle.Screen()
    alex = turtle.Turtle()
    alex.color("blue")
    drawSquare(alex, 100)
    wn.exitonclick()

if __name__ == "__main__":
    main()
    
