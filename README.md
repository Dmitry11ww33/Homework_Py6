Homework PY

-----------------------------------------------

Ex.1

Вывести на экран фигуру из звездочек:
*******
*******
*******
*******
(квадрат из n строк, в каждой строке n звездочек)
n - гарантируется, что целое число

strings = 4
string_1 = 4

while strings != 0 :
    strings -=1
    if string_1 == 4:
        string_1 = 4
        print("*******")
    elif string_1 == 4:
        string_1 = 4
        print("*******")
    else:
        print("Число не существует")

-----------------------------------------------

Ex.2

# распечатайте все числа, которые делятся на 3 от start до end(включительно) (start, end - могут быть перепутаны), start , end- гарантируется, что целые числа

start = 1
end = 50

for i in range(start, end+1):
    if i % 3 == 0:
        print(i)

-----------------------------------------------

Ex.3

напишите программу для черепахи, чтобы она рисовала вот так  (кол-во углов произвольное)

import turtle

turtle.color('red')
turtle.forward(50)
turtle.left(90)
turtle.color('green')
turtle.forward(50)
turtle.right(90)
turtle.color('yellow')
turtle.forward(70)
turtle.left(90)
turtle.color('blue')
turtle.forward(70)
turtle.right(90)
turtle.color('purple')
turtle.forward(90)
turtle.left(90)
turtle.color('orange')
turtle.forward(90)

-----------------------------------------------

Ex.4

Выведите на экран числа 1.2, 1.4, 1.6, ..., 2.8. Для программы необходимо использовать цикл for

for i in range(12, 29, 2):
    print(i/10)

-----------------------------------------------

Ex.5

n - кол-во сторон (гарантируется, что число целое)
a - сторона многоугольника
is_fill - нужно залить фигуру (гарантируется, что будет использован только логический тип данных)
нарисовать ПРАВИЛЬНЫЙ многоугольник по заданным характеристикам 

import turtle

def draw_polygon(n, a, is_fill=False):
    angle = 360 / n
    length = a
    turtle.begin_fill() if is_fill else None  
    for _ in range(n):
        turtle.forward(length)
        turtle.right(angle)       
    turtle.end_fill() if is_fill else None  
    turtle.done()

n = 5
a = 100
is_fill = True

draw_polygon(n, a, is_fill)
