#  CODE CHALLENGE: STRING METHODS
Exercises and code from code academy
CODE CHALLENGE: STRING METHODS

Count Letters

Q: Write a function called unique_english_letters that takes the string word as a parameter. The function should return the total number of unique letters in the string. Uppercase and lowercase letters should be counted as different letters.

We’ve given you a list of every uppercase and lower case letter in the English alphabet. It will be helpful to include that list in your function.

ANS:
letters = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz"
# Write your unique_english_letters function here:
def unique_english_letters(word):
  uniques = []
  for letter in word:
    if letter in letters and not letter in uniques:
      uniques.append(letter)
  return len(uniques)


Count X

Q: 1.
Write a function named count_char_x that takes a string named word and a single character named x as parameters. The function should return the number of times x appears in word.

ANS: 
def count_char_x(word, x):
  counter = 0
  for letter in word:
    if letter == x:
      counter += 1
  return counter

other solution with list comprehension:

def count_char_x(word, x):
  lst = [letter for letter in word if letter == x]
  return len(lst)
  
  Count Multi X
  
  Q: Write a function named count_multi_char_x that takes a string named word and a string named x. This function should do the same thing as the count_char_x function you just wrote - it should return the number of times x appears in word. However, this time, make sure your function works when x is multiple characters long.

For example, count_multi_char_x("Mississippi", "iss") should return 2

ANS:
def count_multi_char_x(word, x):
  splits = word.split(x)
  return(len(splits)-1)
  
  
  Substring Between

Q: Write a function named substring_between_letters that takes a string named word, a single character named start, and another character named end. This function should return the substring between the first occurrence of start and end in word. If start or end are not in word, the function should return word.

For example, substring_between_letters("apple", "p", "e") should return "pl".

ANS:
def substring_between_letters(word, start, end):
  start_ind = word.find(start)
  end_ind = word.find(end)
  if start_ind > -1 and end_ind > -1:
  	return(word[start_ind+1:end_ind])
  return word
  
  X Length

Q: 1.
Create a function called x_length_words that takes a string named sentence and an integer named x as parameters. This function should return True if every word in sentence has a length greater than or equal to x.

ANS: 
def x_length_words (sentence, x):
  words = sentence.split(' ')
  for word in words:
    if len(word) < x:
      return False
  return True
  
  Check Name
  
 Q: Write a function called check_for_name that takes two strings as parameters named sentence and name. The function should return True if name appears in sentence in all lowercase letters, all uppercase letters, or with any mix of uppercase and lowercase letters. The function should return False otherwise.

For example, the following three calls should all return True:
check_for_name("My name is Jamie", "Jamie")
check_for_name("My name is jamie", "Jamie")
check_for_name("My name is JAMIE", "Jamie")

ANS:
def check_for_name(sentence, name):
  words = sentence.split(' ')
  for word in words:
    if word.lower() == name.lower():
      return True
  return False
  
  Every Other Letter

Q: Create a function named every_other_letter that takes a string named word as a parameter. The function should return a string containing every other letter in word.
ANS:
def every_other_letter (word):
  other_letter = ''
  for i in range(0, len(word),2):
    other_letter += word[i]

  return other_letter
  
 Reverse
 
 Q: Write a function named reverse_string that has a string named word as a parameter. The function should return word in reverse.
 ANS: def reverse_string(word):
  reverse = ""
  for i in range(len(word)-1, -1, -1):
    reverse += word[i]
  return reverse
  
  Make Spoonerism

Q: A Spoonerism is an error in speech when the first syllables of two words are switched. For example, a Spoonerism is made when someone says “Belly Jeans” instead of “Jelly Beans”.Write a function called make_spoonerism that takes two strings as parameters named word1 and word2. Finding the first syllable of a word is a difficult task, so for our function, we’re going to switch the first letters of each word. Return the two new words as a single string separated by a space.

ANS:
def make_spoonerism(word1, word2):
  return word2[0]+word1[1:]+" "+word1[0]+word2[1:]
  
Add Exclamation

Q: Create a function named add_exclamation that has one parameter named word. This function should add exclamation points to the end of word until word is 20 characters long. If word is already at least 20 characters long, just return word.

ANS:
def add_exclamation(word):
  while(len(word) < 20):
    word += "!"
  return word
