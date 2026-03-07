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

- but if you want to add list to another list you can use the *.extend()* Method:
```Py title="Extending"
list1 = [1, 2, 3, 4]
list2 = [5, 6 , 7 , 8]
extended_list = list1.extend(list2)
print(extended_list)
```
> [1, 2, 3, 4, 5, 6, 7, 8]

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

- or you can just use the *.remove* method for removing your desired item:
```Py title="Removing an specific item"
list1 = [1, 2, 3, 4]
list1.remove(3)
print(list1)
```
> [1, 2, 4]

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
- You can also slice a part of the list with the slice operator (:):
```py title="Slicing"
list1 = ["num1", "num2", "num3", "num4"]
print(list[1:3])
```
> ["num1", "num2"]

- you can also clear a list by *.clear* method:
```py 
list1 = [1, 2, 3]
list1.clear()
print(list1)
```
> [ ]

- for sorting list you can do 2 things:
```Py title="sorting with .Sort() method"
list1 = [3, 4, 1, 2]
list1.sort()
print(list1)
```
> [1, 2, 3, 4]

```Py title="sorting with sorted() function"
list1 = [3, 4, 2, 1]
sorted_list = sorted(list1)
print(list1)
print(sorted_list)
```
> [3, 4, 2, 1]
> [1, 2, 3, 4]

- sometimes you want to reverse a list and you can use *.reverse* method:
```py
list1 = [1, 2, 3, 4]
list1.reverse()
print(list1)
```
> [4, 3, 2, 1]

- and if you want to find the index of an item, you can use the *.index* Method:
```Py
list1 = ['Hello', 'name', 'slimshady']
print(list1.index('slimshady'))
print(list1.index('marshall'))
```
> 2
> ValueError # if the item is not existent

## Tuples
```Py title="Tuples example"
tuple1 = (67, 'Sin of pie', False)
# the only thing about tuples is its ordered and cannot be charged. 
print(tuple1[1])
# you can also use negetive indexing for reaching from the back
```
> 'Sin of pie'

#### the tuple() function 
```Py
string_name = 'John doe'
print(tuple(string_name))
```
> ('J', 'o', 'h', 'n', ' ', 'd', 'o', 'e')

#### Checking if something is in the tuple or nah
```Py title=""in" keyword"
tuple1 = (23, 47, 'Hello', False)
'Hello' in tuple1 # True
89 in tuple1 # False
```

#### Unpacking a tuple
```Py 
tuple1 = ('John Doe', 23, False)
name, age, is_married = tuple1
print(name)
print(age)
print(is_married)
```
> John Doe
> 23
> False

- you can also get one thing from the list and set everything aside:
```Py
tuple1 = ('John Doe', 23, False)
name, *rest = tuple1
print(name)
print(rest) # the output will be a list!
```
> John Doe
> [23, False]

#### slicing a tuple
```Py
tuple1 = (23, 46, 'IDK', True)
print(tuple1[1:3])
```
> (46, 'IDK')

#### Counting items in tuples
```Py title=".count method"
tuple1 = (1, 1, 2, 2, 2, 3)
print(tuple1.count(1))
print(tuple1.count(2))
print(tuple1.count(3))
print(tuple1.count(4))
```
> 2
> 3
> 1
> 0 # if there is none, it will return 0

#### Finding the index
```Py title=".index method"
tuple1 = (2, 4, 1, 3)
print(tuple1.index(1))
print(tuple1.index(8))
```
> 2
> ValueError # if the item wasn't found

#### Sorting tuples
```Py title="sorted() function"
tuple1 = (3, 2, 4, 1)
tuple1_sorted = sorted(tuple1)
print(tuple1)
print(tuple1.sorted)
# you cannot use .sort method on tuples cause they are immutable.
```
> (3, 2, 4, 1)
> (1, 2, 3, 4)

- you can use arguments such as reverse or key for other purposes:
```py title="Arguments for sorted() function"
tuple1 = ("Hello", "Hi", "Hey", "Name")
print(sorted(tuple1, reverse=True))
print(sorted(tuple1, key=len))
```
> ("Name", "Hey", "Hi", "Hello") # Reversed
> ("Hi", "Hey", "Name", "Hello") # Sorted by length

## For loops
```py title="Looping through a List"
list1 = [1, 2, 3, 4, 5]
for item in list1:
    print(item)
```
> 1
> 2
> 3
> 4
> 5

- you can also loop through strings:
```Py title="looping through strings"
str1 = "My String"
for char in str1
    print(char)
```
> M
> y
>     
>S
>t
>r
>i
>n
>g

- you can also nest some loops for further shit:
```py title="Nesting for Loops"
categories = ("Fruits", "Vegetables")
edibles = ("apple", "banana", "orange")
for category in categories:
    for edible in edibles:
        print(category, edible)
```
> Fruits apple
> Fruits banana 
> Fruits orange 
> Vegetables apple
> Vegetables banana 
> Vegetables orange

## While loops
```py title="While loop example"
x = 0
while x < 9:
	print(x)
	x++
```
> 0, 1, 2, 3, 4, 5, 6, 7, 8

- you can use "continue" to skip a loop iteration or use "break" to exit a loop when a iteration comes.
#### using else for loops:
- you can use "else" after while or for loops and it will be executed if an operation of loop is finished and it is not terminatied by a "break" statement:
```py
words = ['sky', 'apple', 'rhythm', 'fly', 'orange']

for word in words:
    for letter in word:
        if letter.lower() in 'aeiou':
            print(f"'{word}' contains the vowel '{letter}'")
            break
    else:
        print(f"'{word}' has no vowels")
```
>'sky' has no vowels
>'apple' contains the vowel 'a'
>'rhythm' has no vowels
>'fly' has no vowels
>'orange' contains the vowel 'o'

#### range() function 
```py
range(start, stop, step) #Generate a sequence of ints and the stop is not inclusive. If the start is not Declered it is assumed 0.

# you can also turn it into a list by list() function:
numbers = list(range(0, 10))
print(numbers)
```
> [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

## Enumerate() function 
- it is a function that takes a list and returns a tuple that has 2 members; first it the index and second is the member from the first list:
```Py
languages = ["Rust", "C++", "Zig"]
print(list(enumerate(languages)))
```
> [(0, "Rust"), (1, "C++"), (2, "Zig")]

- we can also unpack the list with enumerate function:
```Py
Languages = ["Rust", "C++", "Zig"]

for index, language in enumerate(Languages):
    print(f"the index {index} is occupied by item {language}")
```
> The index 0 is occupied by item Rust
> The index 1 is occupied by item C++
> The index 2 is occupied by item Zig

- you can also give it a start argument so it starts counting from that.

