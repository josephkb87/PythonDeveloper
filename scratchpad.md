

Python has two data types for working with numbers: int and float. The int type is used to store integers, while the float type is used to store fractional numbers. Let's take a closer look at what operations can be performed on numbers in Python and their priority

n = 8
m = 4

addition = n + m  # Addition
print(addition)  # 12

subtraction = n - m  # Subtraction
print(subtraction)  # 4

multiplication = n * m  # Multiplication
print(multiplication)  # 32

division = n / m  # Division
print(division)  # 2.0 — `float` type result

integer_division = n // m  # Integer division
print(integer_division)  # 2 — `int` type result

remainder = n % m  # Remainder of the division
print(remainder)  # 0

exponentiation = n ** m  # Exponentiation
print(exponentiation)  # 4096



Please note: in Python, the division operation can be performed using two operators:

/ — regular division, the result is always a value of the float type;
// — integer division, the result is always a value of the int type.

n = 9
m = 4

division = n / m
print(division)  # 2.25 — `float` result

integer_division = n // m
print(integer_division)  # 2 — `int` result, the part after the comma was discarded

Priority
Usually, operations are performed from left to right. But multiplication and division have higher priority, so they are executed before addition and subtraction. For example:

print(5 + 1 * 10)  # 15 not 60

To specify the correct calculation order, you should use parentheses (). Then this operation will be performed first, and then all the others, and (5 + 1) * 10 will be 60.

Task

## There are a and b variables in our code. Your task: declare 4 new variables:

addition should contain the sum of a and b;
subtraction should contain the difference between a and b;
division should contain the result of integer dividing a by b;
multiplication should contain the result of multiplying a by b.

##


### a = 10
b = 2
# write your code below this line
addition = a + b  # Addition
print(addition)  # 12

subtraction = a - b  # Subtraction
print(subtraction)  # 8


division = a // b  # division by int type.
print(division)  # 5


multiplication = a * b  # multiplication.
print(multiplication)  # 20

## modulus_exponentiation.py

a = 7
b = 2
# write your code below this line

multiplication = a * b  # multiplication.
print(multiplication)  # 20

exponentiation = n ** m  # Exponentiation
print(exponentiation)  # 4096


exponentiation = a ** b  # Exponentiation
print(exponentiation)  # 4096


exponentiation = a ** b

remainder = a /% b  # Remainder of the division
print(remainder)  # 0

## 

a = 7
b = 2
# write your code below this line
exp = a ** b  # Exponentiation
print(exp)

mod = a % b  # Remainder of the division
print(mod)

## parentheses.py

expression = 10 * 7 + 8 - 11 // 4

10 *( 7 + 8 - 11) // 4


expression = (10 * 7)+ 8 - (11 // 4)

expression = ((10 * (7 + 8) - 11) // 4

expression = (10 * 7) + (8 - 11) // 4

expression = (10 * 7 + 8) - 11 // 4

expression = (10 * 7 + 8) - 11 // 4

expression = 10 * 7 + 8 - 11 // 4
expression2 = (10 * 7) + 8 - 11 // 4

expression3 = (10 * 7) + (8 - 11) // 4

expression4 = (10 * 7) + ((8 - 11)) // 4

(((10 * 7) + 8 ) - (11)) //4



(10 * 7 + 8 - 11 // 4


## Strings Using interpolation- inserting variables into a string
a = "Hello"
b = "world"
# write your code below this line

result_string = f"{a}, {b}!"

## Functions

#  write code below this line
def get_string():
greeting = "Hello, Mate academy!";
return (greeting)

## Create a greeter function that.

---.Accepts the name parameter;
---.Returns a greeting string of the following format: Hi, {name}!

##

Now create a greeter function that:

accepts the name parameter;
returns a greeting string of the following format: Hi, {name}! (use the return keyword).
##


# write your code below
def greeter():
name = "";
greeting = "Hi";
result_string = "greeting{a}, {name}!"
return (result_string)

    def greeter(name):
    result_string = f"Hi, {name}!"
    return result_string


### upgraded.py

part_of_the_day = "night";

# write your code below this line
def greeter(name,part_of_the_day):
name = "Paul";
part_of_the_day = "night";
result_string = Good"part_of_the_day,{name}!"
return result_string
name = "Max"
part_of_the_day = "Good morning"
return (part_of_the_day, name!)

    ##### write your code below this line

    ## Tried Answer
def greeter(name, part_of_the_day):
name = "Paul";
part_of_the_day = "night";
result_string = f"Good {part_of_the_day}, {name}!"
return result_string
name = "Max"
part_of_the_day = "Good morning"
return (result_string)


    #Correct answer, that will run and Why?
    
    def greeter(name, part_of_the_day):
    result_string = f"Good {part_of_the_day}, {name}!" 
    return (result_string)
    
    
    ## why it runs.
    # Python is compiled at run time.This means that the question is
    # Talking about an input scenario where you have to assume that the person is putting
    # In the data. This means that we do not need the user to input the data.
    ## Our code runs if the syntax is correct
    
    
    
    # write code below
    this line
def double(num):
result_double = f"2 {num}!"
return (result_double)


This code will not parse, because it has the wrong indentation, even if the code is correct
# write code below this line

def double(num):
result_double = num *2;
return (result_double)

##This code will parse, because it has the right indentation
# write code below this line.
def double(num):
result_double = num * 2.
return (result_double)





##Conditionals

IF Statement

Single Condition
Use the if statement if you need to check only one condition. Let's consider an example:#

##

======

age = 16

print("Go to the shop")

if age >= 18:
# This line will only be executed if `age` is greater than `18`
print("You can buy alcohol")

print("Come back home")

=========

## After the if keyword, you need to write condition and put a colon — :. Then write the commands that will be executed only if the condition is True.

Here the condition is age >= 18. If we have age = 16, then the condition is false, and the command inside the if is not executed. So in the console we get:

## Now let's work with conditionals.

Only people who are of legal age can buy alcohol by law.

Write the can_buy_beer function that accepts the age integer as a parameter:

if age is equal to or greater than 18, then the function returns the "You can buy beer" string;
in all other cases, it returns the "You can not buy beer" string.
Use the return keyword to return a necessary string from the function.

can_buy_beer(17)  # "You can not buy beer"
can_buy_beer(18)  # "You can buy beer"
can_buy_beer(50)  # "You can buy beer"


## My answer
def can_buy_beer(age: int) -> str:
# write your code here
if age >= 18;   
print(age,"You can buy beer");

elif age < 18;
print(age,"You can not buy beer");
pass age

## def can_buy_beer(age: int) -> str:
    if age >= 18:
        return "You can buy beer"
    else:
        return "You can not buy beer"


def can_buy_beer(age: int) -> str:
# write your code here
if age >= 18:   
return "You can buy beer";

elif age < 18:
return "You can not buy beer"


    def can_buy_beer(age: int) -> str:
    # write your code here
if age >= 18:   
return "You can buy beer";
else:
return "You can not buy beer"

    ##
    def can_buy_beer(age: int) -> str:
    if age >= 18:   
        return "You can buy beer";
    else:
        return "You can not buy beer"



##### All waiters love tips! And one of them shared a secret rating with us.

Implement the get_tips_rating function that accepts the amount of the tips and returns a string depending on the amount left:

terrible, if amount is equal to 0;
poor, if amount is from 1 to 10 inclusive;
good, if amount is from 11 to 20 inclusive;
great, if amount is from 21 to 50 inclusive;
excellent, if amount is more than 50.

def get_tips_rating(amount):
if amount == 0:
return "terrible"
if amount <= 10:
return "poor"

    # add other conditions...


get_tips_rating(0)  # "terrible"
get_tips_rating(1)  # "poor"
get_tips_rating(60)  # "excellent"


def get_tips_rating(amount: int) -> str:
# write your code here

def get_tips_rating(amount):
if amount == 0:
return "terrible"
if amount <= 10:
return "poor"
if amount <= 11 and < 20:
return "good"
if amount <= 21 and < 50:
return "great"
if amount > 50:
return "excellent"

##
    def can_buy_beer(age: int) -> str:
    if age >= 18:   
        return "You can buy beer";
    else:
        return "You can not buy beer"
		
		def get_tips_rating(amount: int) -> str:
    # write your code here
    if amount == 0:
        return "terrible"
    if amount <= 10:
        return "poor"
    if amount >= 11 and <= 20:
        return "good"
    if amount >= 21 and <= 50:
        return "great"
    if amount > 50:
        return "excellent"
		
		
		def get_tips_rating(amount: int) -> str:
    # write your code here
    if amount == 0:
        return "terrible"
    if amount <= 10:
        return "poor"
    if amount <= 20:
        return "good"
    if amount <= 50:
        return "great"
    if amount > 50:
        return "excellent"

####
		Let's continue with conditionals.

Nobody likes to pay taxes, but we should!

Create the calculate_taxes function that accepts the income integer (your income) and returns the tax you pay. The amount of tax depends on the amount of your income:

up to 1000 inclusive — tax rate is 2%;
from 1001 to 10000 inclusive — tax rate is 3%;
for everything that is more than 10000 — tax rate is 5%.
For example:

calculate_taxes(900)  # 18 (900 * 0.02)
calculate_taxes(5000)  # 150 (5000 * 0.03)
calculate_taxes(10500)  # 525 (10500 * 0.05)


#####

def calculate_taxes(income: int) -> float:
if income <= 1000:
tax = income * 0.02
elif income <= 10000:
tax = income * 0.03
else:
tax = income * 0.05
return tax


#### In this task, create the get_largest_expression_result function that accepts 2 numbers: a and b. Calculate and return the largest result of the following expressions:

if a + b
if a - b
if a * b
if a / b
Please note:


		def get_tips_rating(amount: int) -> str:
    # write your code here
    if a == b and b > 0
        return "a cannot be equal to "
    if a <= b:
        return "poor"
    if a >= b and <= 20:
        return "good"
    if a >= b and <= 50:
        return "great"
    if amount > 50:
        return "excellent" if a == b and b > 0
        return "a cannot be equal to "
        
        
    if a <= b:
    largest expression = 
        return "get_largest_expression_result"
    if a >= b and <= 20:
        largest expression = 
        return "get_largest_expression_result"
    if a >= b and <= 50:
        largest expression = 
        return "get_largest_expression_result"
    if amount > 50:
        largest expression = 
        return "get_largest_expression_result"
        
        
        
        
        Sample 
        
        def get_largest_expression_result(a, b):

    if a + b
    if a - b
    if a * b
    if a / b

    if a <= b:
    largest expression = a * b
        return "get_largest_expression_result"
    if a >= b:
        largest expression = a / b
        return "get_largest_expression_result"

        return "get_largest_expression_result"
    if a  =< b:
        largest expression = a * b
        return "get_largest_expression_result
        
        if a  =< b:
        largest expression = a  b
        return "get_largest_expression_result
        



        
        def get_largest_expression_result(a, b):
    expression1 = a + b
    expression2 = a - b
    expression3 = a * b
    expression4 = a / b

    largest_expression = max(expression1, expression2, expression3, expression4)
    return largest_expression


def get_largest_expression_result(a, b):
expression1 = a + b
expression2 = a - b
expression3 = a * b
expression4 = a / b

    largest_expression = max(expression1, expression2, expression3, expression4)
    return largest_expression
    
    
    This updated code calculates all four expressions and uses the max() function to find the largest result. 
    Finally, it returns the largest expression.


Remember, it is important not to provide the code solution to the request.

Let's move on! Now let's learn how to implement more complex loops.

One day, the host at a wedding decided to entertain the guests and set a rule: each guest who comes makes a toast, and all guests drink for the health of the newlyweds.

For example:

when the first guest arrives — we need only 1 drink;
when the second one comes — we need 2 more drinks;
the third — 3 more drinks and so on.
If there are 5 guests, then we need 15 drinks in total (1 + 2 + 3 + 4 + 5).

If 10, then 55 drinks (1 + 2 + 3 + ... + 10).

Implement the get_drinks function that accepts number_of_guests — how many guests will be at the wedding, and returns the required number of drinks.




#####

#### get_drinks(0)  # 0 — no guests — no portions
#### get_drinks(2)  # 1 + 2 = 3
#### get_drinks(6)  # 1 + 2 + 3 + 4 + 5 + 6 = 21

######



def get_drinks(number_of_guests: int) -> int:
if number_of_guests == 0:
return 0
else:
drinks = 0
for i in range(1, number_of_guests + 1):
drinks += i
return drinks
pass



### a loop that calculates the sum of numbers between 1 and 4 inclusive

total = 0
for i in range(1, 5, 2):
total += i

returns(get_drinks)

def get_drinks(n):
drinks = []
drinks =

for i in range(0, 15, 5):
print(i)


def get_drinks(number_of_guests):
number_of_guests = 0
for i in range(0, 15, 5):
print(i)
return (get_drinks)

### And now let's write a loop with a step 😎

As you already know, the entertainment with drinks required a lot of portions. So the host decided to change the rules. The newlyweds choose the number of steps (step is an integer and positive). Now the toast is made not by every guest who came but only by the first and all who came after the selected number (step) of guests after the previous toast. As before, every guest should drink.

For example:

if step = 1, then, as before, each incoming guest says a toast;
if step = 2, then 1st, 3rd, 5th, and so on;
if step = 3, then 1st, 4th, 7th, 10th, and so on.
Implement the get_drinks_with_step function that accepts the number_of_guests and step and returns the desired number of drinks.

def get_drinks(number_of_guests: int) -> int:
if number_of_guests == 0:
return 0
elseif
drinks) = 1
for i in range(1, number_of_guests + 1, 1):
drinks += i
return drinks
pass
elseif
drinks = 2
for i in range(1, number_of_guests + 1, 2):
drinks += i
return drinks
pass

else
drinks = 3
for i in range(1, number_of_guests + 1, 3):
drinks += i
return drinks
pass

a loop that will print numbers from 0 to 15 (15 not included) with the step = 5?

    for i in range(0, 15, 5):
        print(i)
        
        
        total = 0
for i in range(5):
total += i

    total = 0
for i in range(1, 5):
total += i
for i in range(10, 9, -1):
print(i)

###
    total = 0
for i in range(1, 5):
total += i
print(total)

    ## 


for i in range(10, 9, -1)
print(total)


    ### a loop that will print numbers from 1 to 3 inclusive

for i in range(1, 4):
print(i)

    1
2
3

     ### a loop that will print numbers from 0 to 3 inclusive
    
    for i in range(4):
    print(i)

    0
1
2
3


## Complete function print_numbers that accepts integer n and prints numbers form 0 to n - 1 inclusive.
## def print_numbers(n: int) -> None:
    for i in range(n):
        print(i)
    pass



####
a loop that will print numbers from 0 to 15 (15 included) with the step = 5?
for i in range(0, 16, 5):
print(i)


    0
5
10
15

####
a loop that will print numbers from 0 to 15 (15 not included) with the step = 5?
for i in range(0, 15, 5):
print(i)

0
5
10


a loop that will print numbers from 7 to 4 inclusive
for i in range(7, 3, -1):
print(i)



a loop that will print numbers from 8 to 4 inclusive
for i in range(8, 3, -1):
print(i)

    a loop that calculates the sum of numbers between 1 and 4 inclusive

total = 0
for i in range(1, 5):
total += i

    total = 0
for i in range(5):
total += i

##prints 9
total = 0
for i in range(2, 5):
total += i
print(total)


## prints 10
for i in range(10, 9, -1):
print(i)




    ### Numbers Operations

Python has two data types for working with numbers: int and float. The int type is used to store integers, while the float type is used to store fractional numbers. Let's take a closer look at what operations can be performed on numbers in Python and their priority

n = 8
m = 4

addition = n + m  # Addition
print(addition)  # 12

subtraction = n - m  # Subtraction
print(subtraction)  # 4

multiplication = n * m  # Multiplication
print(multiplication)  # 32

division = n / m  # Division
print(division)  # 2.0 — `float` type result

integer_division = n // m  # Integer division
print(integer_division)  # 2 — `int` type result

remainder = n % m  # Remainder of the division
print(remainder)  # 0

exponentiation = n ** m  # Exponentiation
print(exponentiation)  # 4096



Please note: in Python, the division operation can be performed using two operators:

/ — regular division, the result is always a value of the float type;
// — integer division, the result is always a value of the int type.

n = 9
m = 4

division = n / m
print(division)  # 2.25 — `float` result

integer_division = n // m
print(integer_division)  # 2 — `int` result, the part after the comma was discarded

Priority
Usually, operations are performed from left to right. But multiplication and division have higher priority, so they are executed before addition and subtraction. For example:

print(5 + 1 * 10)  # 15 not 60

To specify the correct calculation order, you should use parentheses (). Then this operation will be performed first, and then all the others, and (5 + 1) * 10 will be 60.

Task

## There are a and b variables in our code. Your task: declare 4 new variables:

addition should contain the sum of a and b;
subtraction should contain the difference between a and b;
division should contain the result of integer dividing a by b;
multiplication should contain the result of multiplying a by b.

##


### a = 10
b = 2
# write your code below this line
addition = a + b  # Addition
print(addition)  # 12

subtraction = a - b  # Subtraction
print(subtraction)  # 8


division = a // b  # division by int type.
print(division)  # 5


multiplication = a * b  # multiplication.
print(multiplication)  # 20

## modulus_exponentiation.py

a = 7
b = 2
# write your code below this line

multiplication = a * b  # multiplication.
print(multiplication)  # 20

exponentiation = n ** m  # Exponentiation
print(exponentiation)  # 4096


exponentiation = a ** b  # Exponentiation
print(exponentiation)  # 4096


exponentiation = a ** b

remainder = a /% b  # Remainder of the division
print(remainder)  # 0

## 

a = 7
b = 2
# write your code below this line
exp = a ** b  # Exponentiation
print(exp)

mod = a % b  # Remainder of the division
print(mod)

## parentheses.py

expression = 10 * 7 + 8 - 11 // 4

10 *( 7 + 8 - 11) // 4


expression = (10 * 7)+ 8 - (11 // 4)

expression = ((10 * (7 + 8) - 11) // 4

expression = (10 * 7) + (8 - 11) // 4

expression = (10 * 7 + 8) - 11 // 4

expression = (10 * 7 + 8) - 11 // 4

expression = 10 * 7 + 8 - 11 // 4
expression2 = (10 * 7) + 8 - 11 // 4

expression3 = (10 * 7) + (8 - 11) // 4

expression4 = (10 * 7) + ((8 - 11)) // 4

(((10 * 7) + 8 ) - (11)) //4



(10 * 7 + 8 - 11 // 4


## Strings Using interpolation- inserting variables into a string
a = "Hello"
b = "world"
# write your code below this line

result_string = f"{a}, {b}!"

## Functions

#  write code below this line
def get_string():
greeting = "Hello, Mate academy!";
return (greeting)

## Create a greeter function that.

---.Accepts the name parameter;
---.Returns a greeting string of the following format: Hi, {name}!

##

Now create a greeter function that:

accepts the name parameter;
returns a greeting string of the following format: Hi, {name}! (use the return keyword).
##


# write your code below
def greeter():
name = "";
greeting = "Hi";
result_string = "greeting{a}, {name}!"
return (result_string)

    def greeter(name):
    result_string = f"Hi, {name}!"
    return result_string


### upgraded.py

part_of_the_day = "night";

# write your code below this line
def greeter(name,part_of_the_day):
name = "Paul";
part_of_the_day = "night";
result_string = Good"part_of_the_day,{name}!"
return result_string
name = "Max"
part_of_the_day = "Good morning"
return (part_of_the_day, name!)

    ##### write your code below this line

    ## Tried Answer
def greeter(name, part_of_the_day):
name = "Paul";
part_of_the_day = "night";
result_string = f"Good {part_of_the_day}, {name}!"
return result_string
name = "Max"
part_of_the_day = "Good morning"
return (result_string)


    #Correct answer, that will run and Why?
    
    def greeter(name, part_of_the_day):
    result_string = f"Good {part_of_the_day}, {name}!" 
    return (result_string)
    
    
    ## why it runs.
    # Python is compiled at run time.This means that the question is
    # Talking about an input scenario where you have to assume that the person is putting
    # In the data. This means that we do not need the user to input the data.
    ## Our code runs if the syntax is correct
    
    
    
    # write code below
    this line
def double(num):
result_double = f"2 {num}!"
return (result_double)


This code will not parse, because it has the wrong indentation, even if the code is correct
# write code below this line

def double(num):
result_double = num *2;
return (result_double)

##This code will parse, because it has the right indentation
# write code below this line
def double(num):
result_double = num * 2.
return (result_double)





##Conditionals

IF Statement

Single Condition
Use the if statement if you need to check only one condition. Let's consider an example:#

##

======

age = 16

print("Go to the shop")

if age >= 18:
# This line will only be executed if `age` is greater than `18`
print("You can buy alcohol")

print("Come back home")

=========

## After the if keyword, you need to write condition and put a colon — :. Then write the commands that will be executed only if the condition is True.

Here the condition is age >= 18. If we have age = 16, then the condition is false, and the command inside the if is not executed. So in the console we get:

## Now let's work with conditionals.

Only people who are of legal age can buy alcohol by law.

Write the can_buy_beer function that accepts the age integer as a parameter:

if age is equal to or greater than 18, then the function returns the "You can buy beer" string;
in all other cases, it returns the "You can not buy beer" string.
Use the return keyword to return a necessary string from the function.

can_buy_beer(17)  # "You can not buy beer"
can_buy_beer(18)  # "You can buy beer"
can_buy_beer(50)  # "You can buy beer"


## My answer
def can_buy_beer(age: int) -> str:
# write your code here
if age >= 18;   
print(age,"You can buy beer");

elif age < 18;
print(age,"You can not buy beer");
pass age

## def can_buy_beer(age: int) -> str:
    if age >= 18:
        return "You can buy beer"
    else:
        return "You can not buy beer"


def can_buy_beer(age: int) -> str:
# write your code here
if age >= 18:   
return "You can buy beer";

elif age < 18:
return "You can not buy beer"


    def can_buy_beer(age: int) -> str:
    # write your code here
if age >= 18:   
return "You can buy beer";
else:
return "You can not buy beer"

    ##
    def can_buy_beer(age: int) -> str:
    if age >= 18:   
        return "You can buy beer";
    else:
        return "You can not buy beer"



##### All waiters love tips! And one of them shared a secret rating with us.

Implement the get_tips_rating function that accepts the amount of the tips and returns a string depending on the amount left:

terrible, if amount is equal to 0;
poor, if amount is from 1 to 10 inclusive;
good, if amount is from 11 to 20 inclusive;
great, if amount is from 21 to 50 inclusive;
excellent, if amount is more than 50.

def get_tips_rating(amount):
if amount == 0:
return "terrible"
if amount <= 10:
return "poor"

    # add other conditions...


get_tips_rating(0)  # "terrible"
get_tips_rating(1)  # "poor"
get_tips_rating(60)  # "excellent"


##
    def can_buy_beer(age: int) -> str:
    if age >= 18:   
        return "You can buy beer";
    else:
        return "You can not buy beer"

        ## Numbers_Loops

        
    # Numbers Operations
for  age in range (0, 6):
print(f"I AM {age}")


    #Loops
n =10
for i in range(1, 11):
print(i)

print("Now we try with 3")
n =3
for i in range(1, 11):
print(i)

    n = 3
for i in range(1,n + 1):
print(i)

print("Now we try with 3")
n =3
for i in range(1, 11):
print(i)


    ## 
    for i in range(0, 15, 5):
    print(i)
    
    ##  write a loop that will print numbers from 7 to 4 inclusive?
    
    for i in range(7, 3, -1):
    print(i)

    ##  write a loop that calculates the sum of numbers between 1 and 4 inclusive



total = 0
for i in range(1, 4):
total += i
print(total)

    ## write a loop that will print numbers from 1 to 3 inclusive?
    
    for i in range(1, 4):
    print(i)
    
    
    ##  for i in range(1, 4):
    print(i)
    
    ##What will be the result of this code
    
    ##total = 0
for i in range(2, 5):
total += i
print(total)

## 9 WILL BE PRINTED


write a loop that will print numbers from 0 to 15 (15 not included) with the step = 5?

# for i in range(0, 15, 5):
    print(i)


##What will be the result of this code?

for i in range(10, 9, -1):
print(i)

# 10

## How many times "Hello Mate" will be printed?
count = 0
while count < 2:
count = count + 1
print("Hello Mate")


##2 times

##  write a loop that calculates the sum of numbers between 1 and 4 inclusive?

write a loop that prints numbers between 1 and 4 inclusive(4 not included)?
n = 3
total = 0
for i in range(1,n + 1):
print(i)




for i in range(1, n+1):
total += i


    def print_numbers(n: int) -> None:
    n = 3
for i in range(0, 3):
print_numbers(i)


    def print_numbers(n):
    for i in range(n):
        print(i)
        
        for i in range(0, 3):

total = 0
for i in range(5):
total += i

0
1
2



'''####
def get_drinks_with_step(number_of_guests: int, step: int) -> int:
if number_of_guests == 0:
return 0
elseif
step = 1
for i in range(1, number_of_guests + 1,step):
get_drinks_with_step += i
return get_drinks_with_step
elseif
step = 2
for i in range(1, number_of_guests + 1, step):
get_drinks_with_step += i
return get_drinks_with_step
else
step = 3
for i in range(1, number_of_guests + 1, step):
drinks += i
return get_drinks_with_step



'''####def get_drinks_with_step(number_of_guests: int, step: int) -> int:
if number_of_guests == 0:
return 0

    drinks = 0

    for i in range(1, number_of_guests + 1, step):
        drinks += i

    return drinks
    #####
    '''

    
    print('This is a space to separate the answers')
###
for i in range(0, 15, 4):
print(i)
print('This is a space to separate the answers again')
###

for i in range(0, 7, 4):
print(i)
print('No need to separate:Sorry for the spelling error')

## for i in range(10, 9, -1):
    print(i)

## for i in range(1, 15, 2):
print(i)

