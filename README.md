import random
num = 1

print(" welcome to number guessing game.guess your number with in 5 attempts")
print("The secret number is between 1 and 50")

secret_number = random.randint(1,50)
attempts = 6
if_guess_correct = False

while num <= 6:
    print(f"you have {attempts} attempts remaimg")
    user_number = int(input(" enter your number to guess secret number :"))
    if user_number == secret_number:
        if_guess_correct = True
        print("congrats! you guessed the number")
        break
    elif user_number < secret_number:
        print(" your number is too low")
    elif user_number > secret_number:
        print(" your number is too high")
        print(f"you have {attempts} attempts remaimg")
        if_guess_correct = False

        print("bad luck")

    attempts -= 1
    num += 1

print(f"secret number is {secret_number}. game over!")
