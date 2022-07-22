# PythonProjects. A simple python guessing game. learnt from Nick Walter

import random
import time

print("Hello! Welcome to the guessing game, you need to guess between 1 and 100")
time.sleep(3)
print("Picking a number ...")
time.sleep(3)
guess = int(input("what is your guess? "))
correct_number = random.randint(1, 100)
guess_count = 1

while guess != correct_number:
  time.sleep(1)
  guess_count += 1
  if guess <= correct_number:
    guess = int(input("Wrong answer. You need to guess higher. what is your guess? "))
  else:
    guess = int(input("Wrong answer. You need to guess lower. what is your guess? "))
print(f"Yea! That's the correct number {correct_number}. it took you {guess_count} guesses")
