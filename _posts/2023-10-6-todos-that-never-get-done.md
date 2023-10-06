Over the last week ive learned many commands and done many exercises and the first one that ive done was a calculator that would take many different operators and print the result of whatever the user inputs. During the assignment i didnt have much difficulties at first since i made mine simple and only allowed for 2 number inputs from the user and preset operators and knowledge of math operators. Later on when i was nearing the end and adding all the error messages was when i started to struggle a bit as i didnt know how to properly make it so the user would get a try again message if they entered the wrong data types and etc. But thats also when i learned of try and except errorvalue and it made it so much easier to just customize the error message instead of giving the user a headache trying to figure out what was wrong. The usuage of this particular code would look something like this 
```python
import math

x = int(input('Please enter a positive number:\n'))

try:
    print(f'Square Root of {x} is {math.sqrt(x)}')
except ValueError as ve:
    print(f'You entered {x}, which is not a positive number.')
```
In this code segment, its basically saying that if x is negative then instead of the usual code block error that the terminal prints back to you, it would tell you exactly why the code didnt work since square roots do not work with negatives. This was one function that i found very useful in my recent coding exercises that ive done.

#
Then over the next few days i had my first project
which was to create a todo tracker which ive actually done before in my previous year using vue but now it was with python and it was way more watered down since we did not have to create too much visuals such as aesthetics and such and instead only had to make it easy on the eyes in terminal. For this particular project i started relatively easily using a while loop to get started so that it would always run and constantly ask the user if they wished to add more to a list that i created beforehand or remove from that list. Displaying the list pleasantly would require me to make a for loop and it honestly worked better than what was displayed the first time around when i just printed the list.

```python
while True:
print("Your current todos are: ")
#the x variable is set to zero so that it resets every loop
x = 0
#this for loop would display every todo in its own line with a number before that which is what the x variable is for
for list in todos:
    x = x + 1
    print(str(x) + ". " + list)
print("")
print("")
```
The number before the list value displays not just serves to make it easier for the user to view the list but also helps with picking what to delete later on as shown below.
```python
#im now making an input which would ask for a user input to tell you whether you want to add or remove
    func = input("Would you like to add or remove? ")
    #im now making a if function that would say if the input is equal to add then it would take an input from the user
    #asking for the new input then append it to the list
        new = input("what is your new todo? ")
        todos.append(new)
        print("")
        print("")
        print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
#an elif for when function is equal to remove so i can then delete stuff from the list.
    elif func == "remove":
        print("") 
        #i add this here again so that it would be part of the loop and reread the todos number
        num = int(len(todos))      
        #i added a if statement so that if there is nothing in the list then the command will not run and give an error
        if num <= 0:
            print("")
            print("you have nothing in the list yet")
            print("")
            time.sleep(1)
            print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
        else:
            #i made a variable so that i could ask for a integer input of the number they wish to remove.
            delete = int(input("Please select the number you wish to delete: "))  
            index = int(delete - 1)
                #i then delete the input they put in and add 2 empty spaces
                del todos[index]  
```
This large chunk of code is almost the entirety of the code which the todo functions in and now this is where the 