## Simple "Hello World!"
```python
print("Hello World!")
```
> Hello world!

- if you want to run it in terminal do the following:
`python3 helloworld.py`

___

## Deceleration of Variables 
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
2. The naming doesn't like spaces so use underscores or CamelCase naming.
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
