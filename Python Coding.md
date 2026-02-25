## Simple "Hello World!"
```python
print("Hello World!")
```
> Hello world!

- if you want to run it in terminal do the following:
`python3 helloworld.py`

___

## Decleration of Variables 
```Python
message = "Hello World!"
print(message)

message = "Hello World Again!"
print(message)
```
> Hello World!
> Hello World Again!

- As you can see, the variable message was created with the value "Hello World!" and then it got printed. After that, the variable got reassigned as "Hello World Again!" and got printed again. ==You can reassign variables.==

#### Variables naming rules:
1. It should just include letters, nums and underscores. It cannot begin with a number. 
2. The naming doesnt like spaces so use underscores or CamelCase naming.
3. You shouldn't use names that are in python like print or whatever else.
___

## Strings
```Python title:Strings
string1 = "You can use Doube Quotes"
string2 = 'Or you can use Single Quotes'
```
```Python title:Methods
# You can Titleize a text with this method:
TextToBeTitled = "its my duty."
print(textToBeTitled.title())

# You can also capitalize or make lower all the letters with this two methods:
TestTextUpper = "hi my name is bob."
TestTextLower = "HI MY NAME IS BOB TOO."
print(TestTextUpper.upper())
print(TestTextLower.lower())
```
> Its My Duty.
> HI MY NAME IS BOB.
> hi my name is bob too.

#### Concatenation of strings
```python title:"Concatinaion"
first_name = "Mehdi"
last_name = "Akramzadeh"
full_name = first_name + " " + last_name
print(full_name)
```
>  Mehdi Akramzadeh
#### F Strings:
```Python title:"F Strings"
firstName = "Mehdi"
lastName = "Akramzadeh"

fullName = f"{firstName} {lastName}"
print(fullName)
```
> Mehdi Akramzadeh
- as you see, the F in F_String stands for *format* and it will replace the variables with their value.
- you can also assign an F_String to another variable if you wanted to.

#### Tab and New line:
```Python
print("Hello\n\tWorld!")
```
> Hello
>     World!

#### Cleaning White Space:
```Python title:"Strip Method"
TestString = " Dumb String "

# For removing the right side of a string from white space:
TestString = TestString.rstrip()
print(TestString)

# For removing the left side of a string from white space:
TestString = TestString.lstrip()
print(TestString)

# For removing the right side and the left side of a string from white space:
TestString = TestString.strip()
print(TestString)
```
> ' Dumb String'
> 'Dumb String '
> 'Dumb String'

#### Removing Prefix & Suffix:
```Python title:"RemovePrefix & RemoveSuffix"
userLink = "https://Google.com"
userLink = userLink.removeprefix("https://")
print(userLink)

userFile = "Beta-File.txt"
userFile = userFile.removesuffix(".txt")
print(userFile)
```
>  Google.com
>  Beta-File
- in the parentheses of the *removeprefix* and *removesuffix* method, you add the string that you want to remove from the string.

#### To string conversion
```Python title:"str() function "
age = 18
age_str = str(age)
print(age, type(age))
print(age_str, type(age_str))
```
> 18 <class = int>
> 18 <class = str>
___
## Integers & Floats
```Python
int1 = 10
float1 = 10.0
int2 = 10_000 # It can aslo be like this. The same as 10000

# You can also do multiple assignments like this:
x, y, z = 1, 2, 3
```
- whenever you divide 2 nums, the results will always be a float. Also mixing a int with float will always result in a float.
```Python
int1 = 10
int2 = 5
results1 = int1 / int2
print(results1)

int3 = 10
float1 = 2.0
results2 = int3 * float1
print(results2)
```
> 2.0
> 20.0
___
## Lists
```Python
list1 = ["St1", "St2", "St3"]
print(list1)
print(list1[0])
print(list1[-1])
```
> ["St1", "St2", "St3"]
> St1
> St3

- if you want to change or modify an item, you can do so by referring to its index number and reassigning another value:
```Py
list1 = [num1, num2, num3]
print(list)
list1[0] = num4
print(list)
```
> [num1, num2, num3]
> [num4, num2, num3]

- if you want to add an item to end of a list, you can do so with this command:
```Py
list1 = ["item1", "item2", "item3"]
print(list1)
list1.append("item4")
print(list1)
```
> ["item1", "item2", "item3"]
> ["item1", "item2", "item3", "item4"]

- if you want to insert an item in a list, you can use the *.insert* method. All the item after the specified index will be moved 1 to the right.
```Py
list1 = ["item1", "item2", "item3"]
print(list1)
list1.insert(1, "item4")
print(list1)
```
>  ["item1", "item2", "item3"]
["item1", "item4", "item2", "item3"]

- if you want to remove an item and you know its index, you can use the *del* command to do so:
```Py
list1 = ["item1", "item2", "item3"]
print(list1)
del list1[1]
print(list1)
```
> ["item1", "item2", "item3"]
> ["item1", "item3"]

- but if you dont know its index, you can use *.pop()* to remove the last item from the list:
```Py
list1 = ["item1", "item2", "item3"]
print(list1)
list1.pop()
print(list1)
```
>  ["item1", "item2", "item3"]
>  ["item1", "item2"]
- the thing about *.pop()* you can use it to take that poped item back as a value:
```Py
list1 = ["item1", "item2", "item3"]
popedItem = list1.pop() # You can also store it in a variable.
print(popedItem)
```
> item3