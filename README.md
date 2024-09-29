# Password-Cracking
Let us crack the password by creating th python code .

import random
import os

user_input_password = input("Enter the password: ")

#All possible letters and characters of an password .
password_keys = list("abcdefghijklmnopqrstuvwxyz1234567890")

#Create a blank variable with empty value .
password = ""

#State the condition when the password varable value is not match with value of user_input_password .
while password != user_input_password:

    #Call the blank valkue variable password .
    password = ""

    #By using for loop  we tried to crack password again and again by the length of user_input_password .
    for _ in range(len(user_input_password)):
        #Create a guess_password variable to used a random.choice function on the variable password_keys .
        guess_password = random.choice(password_keys)
        #If the guess_password is not equal to user_input_password then the add this password into the password variable .
        password += guess_password
    #call the password variable .
    print(password)
    #Write a syntax to show on screen while the code is processing .
    print("We are cracking the password!\nPlease wait...\n")
    #It will be used to clear the screen when the code will be try again and again .
    os.system("cls" if os.name == "nt" else "clear")

#When the password will be cracked then it will be used to display the password .
print(f"The password is cracked! Your password is: {password}")
