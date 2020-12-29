# Python-path-Codeacademy
Exercises and code from code academy
CODE CHALLENGE: STRING METHODS

Count Letters

letters = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz"
# Write your unique_english_letters function here:
def unique_english_letters(word):
  uniques = []
  for letter in word:
    if letter in letters and not letter in uniques:
      uniques.append(letter)
  return len(uniques)
