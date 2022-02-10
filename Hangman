# Write your code here
import random

correct_words = 'python', 'java', 'kotlin', 'javascript'
lives = 8
correct_word = random.choice(correct_words)
hidden_word = len(correct_word) * '-'
missed_letters = []
correct_letters = []

print("H A N G M A N")
while True:
    correct_words = 'python', 'java', 'kotlin', 'javascript'
    lives = 8
    correct_word = random.choice(correct_words)
    hidden_word = len(correct_word) * '-'
    missed_letters = []
    correct_letters = []
    button = input('Type "play" to play the game, "exit" to quit:')
    if button == 'play':
        while lives > 0:
            print()
            print(hidden_word)
            print('Input a letter: > ')
            user_letter = input()
            word = list(hidden_word)
            if 0 < len(user_letter) < 2:
                if user_letter.isascii():
                    if user_letter.islower():
                        if user_letter in correct_word:
                            if user_letter in correct_letters:
                                print("You've already guessed this letter")
                            else:
                                position = correct_word.find(user_letter)
                                word[position] = user_letter
                                hidden_word = "".join(word)
                                position = correct_word.rfind(user_letter)
                                word[position] = user_letter
                                hidden_word = "".join(word)
                                correct_letters.append(user_letter)
                        elif user_letter in missed_letters:
                            print("You've already guessed this letter")
                        else:
                            print("That letter doesn't appear in the word")
                            lives -= 1
                            missed_letters.append(user_letter)
                        if hidden_word == correct_word and lives >= 1:
                            print('You guessed the word ' + correct_word + '!')
                            print('You survived!')
                            break
                    else:
                        print('Please enter a lowercase English letter')
                else:
                    print('Please enter a lowercase English letter')
            else:
                print('You should input a single letter')
        else:
            print('You lost!')
            continue
    elif button == 'exit':
        exit()
else:
    button = input('Type "play" to play the game, "exit" to quit:')
