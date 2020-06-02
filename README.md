# hangman-project
hangman project 


import random
from words import words
import string

def get_valid_word(words): # used to not choice the words which contain space or -.
    word=random.choice(words)
    while "-" in word or " " in word:
        word = random.choice(words) # for a loop.
        
    return word
    
def hangman():
    word = get_valid_word(words)
    word_letter = set(word)
    letter= set(string.ascii_uppercase)
    used_letters=set() #already done
    
    
    user_letter =input("guess a letter for starting the game: ").upper()  #user_input is saved as a letter in input
    if user_letter_letter in letter - used_letters:             # haven't used the letter 
        used_letters.add(user_letter)
        if user_letter in word_letter:
            word_letter.remove(user_letter)
            
            
    elif user_letter in used_letters:
        print("It is already printed . try another one")
        
        
    else:
        print("wrong letter")
    
    
    
    
    
user_input = input("type")
print(user_input)
