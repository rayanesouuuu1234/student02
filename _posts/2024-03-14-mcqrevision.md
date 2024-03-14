---
toc: True
comments: True
layout: post
title: MCQ Revision
description: None
courses: {'compsci': {'week': 17}}
type: hacks
---

## Reflection: 
After taking this review test, I was pretty surprised. I felt like I was between 2 answers on a couple of problems and was expecting a B. I was particularly confused on questions like pseudo-code algorithms or list manipulation q's. 

## Question 45
The following question uses a robot in a grid of squares. The robot is represented by a triangle, which is initially facing right.

<img src="https://i.postimg.cc/1X3dWxBt/Screenshot-2024-03-14-at-8-52-01-AM.png" alt="">

Consider the following procedure.

<img src="https://i.postimg.cc/Dzb4X8Kf/Screenshot-2024-03-14-at-8-53-58-AM.png" alt="">

Which of the following code segments will move the robot to the gray square along the path indicated by the arrows?

<img src="https://i.postimg.cc/133jsZ1r/Screenshot-2024-03-14-at-8-54-55-AM.png" alt="">

Correct answer: C

Answer A:
In this code segment, the first call to the function botStepper instructs the robot to perform a series of movements. It moves the robot forward two squares, then rotates it left so that it faces towards the top of the grid. After that, it moves the robot forward two squares again and rotates it right so that it faces towards the right side of the grid. The second call to botStepper instructs the robot to perform a different set of movements. It moves the robot forward three squares, rotates it left so that it faces towards the top of the grid, moves it forward three squares again, and finally rotates it right so that it faces towards the right side of the grid.
After executing these movements, the robot ends up one square to the left of the gray square.

Answer B:
The first call to the function botStepper instructs the robot to perform a series of movements. It moves the robot forward three squares, then rotates it left so that it faces towards the top of the grid. After that, it moves the robot forward three squares again and rotates it right so that it faces towards the right side of the grid.
However, the second call to botStepper attempts to move the robot forward four squares, which would cause it to go off the edge of the grid. As a result, the execution of the code terminates.

Answer C:
The first call to the function botStepper instructs the robot to perform a series of movements. It moves the robot forward two squares, then rotates it left so that it faces towards the top of the grid. After that, it moves the robot forward two squares again and rotates it right so that it faces towards the right side of the grid.
Following these movements, the code segment moves the robot forward one square. Then, the second call to botStepper instructs the robot to perform another set of movements. It moves the robot forward three squares, rotates it left so that it faces towards the top of the grid, moves it forward three squares again, and finally rotates it right so that it faces towards the right side of the grid.
As a result of executing these movements, the robot ends up in the gray square.

Answer D:
The first call to the function botStepper instructs the robot to perform a series of movements. It moves the robot forward three squares, then rotates it left so that it faces towards the top of the grid. After that, it moves the robot forward three squares again and rotates it right so that it faces towards the right side of the grid.
Following these movements, the code segment moves the robot forward one square.However, the second call to botStepper attempts to move the robot forward four squares, which would cause it to go off the edge of the grid. Consequently, the execution of the code terminates.

## Question 55

<img src="https://i.postimg.cc/8cDjr41N/Screenshot-2024-03-14-at-8-57-31-AM.png" alt="">

Correct answer: C

Answer A: This code segment is incorrect because it performs the following steps: it assigns the value of the last element of the list to a variable called "temp," then removes the last element from the list, and finally appends the value of "temp" to the end of the list. As a result, the modified list remains the same as the original list.

Answer B: This code segment is incorrect as it removes the last element of the list and then tries to access an element at an index equal to the length of the list. This action leads to an error because there is no longer an element at that index.

Answer C: This code segment is correct. It functions as follows: it assigns the value of the last element of the list to a variable named "temp," removes the last element from the list, and then inserts the value of "temp" as the first element of the list.

Answer D: This code segment is incorrect because it removes the last element of the list and then attempts to access an element at an index equal to the length of the list. This results in an error because there is no longer an element at that index.