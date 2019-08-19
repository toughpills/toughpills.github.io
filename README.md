# This program demonstrates a function.
# First, we define a function named welcome_message.
def welcome_message():
    print('This is Python course')
    print('Welcome to this world')

# Main program to call the welcome_message function.
welcome_message()

# This program demonstrates a function.
# First, we define a function named welcome_message.
def welcome_message():
    print('This is Python course')
    print('Welcome to this world')

# Second, we define a function named get_name_target.
def get_name():
    name = input ("what is your name ")
    return name  


# Main program to call the welcome_message and get_name function.
welcome_message()
name = get_name()
print("Hi, ", name, ", So glad to see you in this class")

# This program demonstrates a function.
# First, we define a function named welcome_message.
def welcome_message():
    print('This is Python course')
    print('Welcome to this world')

# Second, we define a function named get_name_target.
def get_name():
    name = input ("what is your name ")
    return name

def get_target(name):
    print("Welcome to AE8225", name)
    target_project = int(input("What is your target score for project (0-100):"))
    target_test = int(input("What is your target score for test (0-50):"))
    total = (target_project/100)*50 + target_test
    return total

# Main program to call the functions.
welcome_message()
name = get_name()
total = get_target(name)
print(name, "Noted that your target total score is:", total, "Let's work together to achieve that")


## if there are 3 coffee shops
count = 1
while count <= 3:
    print ("input information of coffee shop NO. ", count)
    horizonDist = int(input("Read horizonDist in meters: "))
    vertDist = int(input("Read vertDist in meters: "))
    dist = horizonDist + vertDist
    print("dist from home to coffee shop NO. ", count, " is ", dist, "m")
    count = count + 1
    
    
Number = 67
print("Hi-Lo Number Guessing Game: between 0 and 100 inclusive.")
guess= int(input("Guess a number: "))
while 0 <= guess <= 100:
    if guess > Number:
        print("Guessed Too High.")
    elif guess < Number:
        print("Guessed Too Low.")
    else: # correct guess, exit with break
        print("You guessed it. The number was:",Number)
        break  # keep going, get the next guess
    guess= int(input("Guess a number: "))
else:
    print("A pity. You quit the game early, the number was:",Number)


# sum up a series of even numbers
# make sure only even numbers contribute to sum

print ("Allow the user to enter a series of even integers. Sum them.")
print ("Ignore non-even input. End input with a '.'")
# initialize the input number and the sum
number_str = input("Number: ")
the_sum = 0
# Stop if a period ( . ) is entered .
# remember , number_str is a string until we convert it
while number_str != "." :
    number = int(number_str)
    if number % 2 == 1: # number is not even ( it is odd)
        print ("Error, only even numbers please.")
        number_str = input("Number: ")
        continue # if the number is not even , ignore it
    the_sum += number
    number_str = input("Number: ")
print ("The sum is:",the_sum)

#get ship orientation from user
while(True):
  user_input = input("vertical or horizontal (v,h) ? ")
  if user_input == "v" or user_input == "h":
    break
  else:
    print ("Invalid input. Please only enter v or h")

