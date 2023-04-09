 > # Python Course

## Others Functions:
`chr()` => takes a character and returns the corresponding unicode.    
`ord()` => takes Unicode and returns corresponding character.

---
## Data types:

[1] `int` -> Integer   
[2] `float` -> Floating point number   
[3] `str` -> String    
[4] `list` -> List [ 1, 2, 3 ]    
[5] `tuple` -> ( 1, 2, 3 )   
[6] `dict`-> Dictionary => {"one" : 1, "two" :2 }   
[7] `bool`-> boolean value [ True - False ]   
***
## Variable:

```python
name = "Tom Itadori" # Single word => Normal
myName = "Tom Itadori" # Two words => camelCase
my_name = "Tom Itadori" # Two Words => snake_case
```
**Source Code** : Original Code you write it in computer

**Translation** : Converting source code into machine language.

**Compilation** : Translate code before run time.

**Run-Time** : Period app take to executing commands

**Interpreted** : Code translated on the fly during execution.

***Escape Sequences characters:***

```python
# \b       => Backspace
# \newline => Escape New Line + \
# \n => Line feed character
# \r => Carriage Return 
print("123456\rabcd") # Output : abcd56
# \t => Horizontal Tab
# \xhh => Character Hex Value
```
***
## String:
#### String methods: 

**`len()`** ⇒ length of character

**`strip()`** ⇒ clear spaces.

**`rstrip()`** ⇒ clear spaces from right

**`lstrip()`** ⇒ clear spaces from left

```python
print(len("Tom")) # 3
string = "   Tom  "
print(string.strip()) # Output "Tom"
print(string.rstrip()) # Output "   Tom"
print(string.lstrip()) # Output "Tom  "
string2 = "#@#@Tom#@"
print(string2.strip("@#")) # Output "Tom"
```
**`title()`** ⇒ words start with uppercased characters and all remaining cased characters have lower case.

**`capitalize()`** ⇒  make the first character have upper case and the rest lower case.

**`zfill()`** ⇒ Pad a numeric string with zeros on the left, to fill a field of the given width.

**`upper()`** ⇒ Return a copy of the string converted to uppercase.

**`lower()`** ⇒ Return a copy of the string converted to lowercase.

```python
print("test test 2d".title()) # Test Test 2D
print("test test 2d".capitalize()) # Test test 2d
print("1".zfill(4)) # 0001
```

`def split(sep, maxsplit) -> List[str]`   
`def rsplit(sep, maxsplit) ->List[str]`   
split() or  *rspit() → [ reverse ]* Return a list of the substrings in the string, using sep as the separator string.

**`center()`** ⇒ Return a centered string of length width.

**`rjust()`** ⇒ [ like center() ] Return a right-justified string of length width.

**`ljust()`** ⇒ [ like center() ] Return a left-justified string of length width.

**`count()`** ⇒ Return the number of non-overlapping occurrences of substring sub in string

```python
a = "itadori"
print(a.center(10,"@")) # @itadori@@

print(a.count("i",1,7) 
# count the number of "i" in the str 'a' starting with index 1 and ending with index 7.
# Output : 1
```
**`swapcase()`** ⇒ Convert uppercase characters to lowercase and lowercase characters to uppercase.

```python
a = "ITADori"
print(a.swapcase()) # itadORI
```

**`startwith()`** ⇒ Return True if S starts with the specified prefix, False otherwise.

**`endwith()`** ⇒ Return True if S ends with the specified suffix, False otherwise.

**`replace()`** ⇒ Return a copy with all occurrences of substring old replaced by new.

```python
a = "I love Python"

print(a.replace("o", "O",1))# I lOve Python
```

**`join()`** ⇒ Concatenate any number of strings.

```python
List = ['ab', 'pq', 'rs']
print("-".join(List)) # ab-pq-rs
```
#### Strings formatting:

**`Old Way:`**:
%s => String   
%d => Integer   
%f => Float    

```python
name = "Tom"
age = 20
rank = 14.97
print("My name is %s and my age is %d and my rank is %.2f"%(name, age, rank))
# My name is Tom and my age is 20 and my rank is 14.97
```

**`New Way:`**
```
{:s} ⇒ String   
{:d} ⇒ Integer     
{:f} ⇒ Float  
```
Exemples:
```python
name = "Tom"
age = 20
rank = 14.97
print("My name is {:s}. Age is {:d}. Rank is {:.2f}".format(name, age, rank))
# My name is Tom. Age is 20. Rank is 14.97
```

```python
a, b, c = 1, 2, 3
print("Hello {1} {0} {2}".format(a, b, c))
# Hello 2 1 3
print("Hello {2:.2f} {1:.1f} {0:.0f}".format(a, b, c))
# Hello 3.00 2.0 1
```

```python
# Other method:
name = "Tom"
age = 20
print(f"My name is {name} And my age is {age}."
```
---
## Number, Lists, Tuples:
#### Numbers:
**`Int`** ⇒ 100, -10, …

**`Float`** ⇒ 10.5, -3.4, …

**`Complex`** ⇒ (5+6j)

```python
myComplexNumber = 5+6j
print(type(myComplexNumber)) # <class 'complex'>
print(myComplexNumber.real) # 5.0 [ Real part of complex number ]
print(myComplexNumber.imag) # 6.0 [ imagianry part of complex number ]
```

- You can convert int or float to any type [ int, float, complex ]
- Can’t convert complex to int or float

**Operators:**

`[+]`   Addition
`[-]`   Subtraction
`[*]`   Multiplication
`[/]`   Division
`[%]`   Modulus
`[**]` Exponent (2**3 = 8)
`[//]` Floor Division
#### Lists:
**`append()`** ⇒ Append object to the end of the list.

**`extend()`** ⇒ Extend list by appending elements from the iterable.

**`remove()`** ⇒ Remove first occurrence of value.

**`sort(reverse=True)`** ⇒ Sort the list in ascending order and return None.

**`reverse()`** ⇒ Reverse _IN PLACE_.

```python
myFriends = ["outhman", "yassir"] 
schoolFriends = ["walid", "mr1"]
myFriends.append(schoolFriends) # ['outhman', 'yassir', ['walid', 'mr1']]

myFriends.extend(schoolFriends) # ['outhman', 'yassir', 'walid', 'mr1']

myFriends.remove("walid") # ['outhman', 'yassir', 'mr1']

myFriends.sort(reverse=True) # ['yassir', 'walid', 'outhman', 'mr1']

myFriends.reverse() # ['mr1', 'walid', 'yassir', 'outhman']
```

**`clear()`** ⇒ Remove all items from list.

**`copy()`** ⇒ Return a shallow copy of the list.

**`count()`** ⇒ Return number of occurrences of value.

**`index()`** ⇒ Return first index of value.

**`insert(index, object)`** ⇒ Insert object before index.

**`pop()`** ⇒ Remove and return item at index (default last).
#### Tuples:
```python
myTuple = (1, 2)
# We can Remove The Parentheses if we want
myTuple2 = 1, 2
# We connot edit or delete item from tuple

# Tuple with one element
myTuple3 = (1, ) # or
myTuple4 = 1, 
```

***Tuple, List, String Repeat ( * )***

```python
myString = "Tom"
myList = [1, 2]
myTuple = (3, 4)

print(myString * 3)
print(myList * 3)
print(myTuple * 3)

# TomTomTom
# [1, 2, 1, 2, 1, 2]
# (3, 4, 3, 4, 3, 4)
```

**`count()`** ⇒ Return number of occurrences of value.

**`index()`** ⇒ Return first index of value.

```python
a = ('A', 'B', 4, 'C')
x, y, _, z = a # [ x='A', y='B', z='C' ]
```
## Set, Dictionary:
#### Set:
[1] Set items are enclosed in curly braces   
[2] Set items are not ordered and not indexed   
[3] Set indexing and slicing cannot be done   
[4] Set has only immutable data types (numbers, strings, tuples) List and Dict are not   
[5] Set items is unique    

**`clear()`** ⇒ Remove all elements from this set.

**`union()`** ⇒ Return the union of sets as a new set. [print(a | b)]

**`add()`** ⇒ Add an element to a set. [add one by one]

**`copy()`** ⇒ Return a shallow copy of a set.

**`remove()`** ⇒ Remove an element from a set; it must be a member.

return error if the element not a set member

**`discard()`** ⇒ Remove an element from a set if it is a member.

**`pop()`** ⇒ remove random element

Remove and return an arbitrary set element.

Raises KeyError if the set is empty.

**`update()`** ⇒ Update a set with the union of itself and others.

**`defference()`** ⇒ Return the difference of two or more sets as a new set.

**`difference_update()`** ⇒ Remove all elements of another set from this set.

— difference does’t update changing
but difference_update does.

```python
mySet = {1, 2, 3, "Four", 3.4, False, 4}
a = {1, 2, 3}
print(mySet.difference(a)) # or
print(mySet - a)
```

**`intersection()`** ⇒ Return the intersection of two sets as a new set.

**`intersection_update()`** ⇒ Update a set with the intersection of itself and another.

```python
mySet = {1, 2, 3, "Four", 3.4, False, 4}
a = {1, 2, 3}

print(mySet.intersection(a)) # or
print(mySet & a)
mySet.intersection_update(a)
print(mySet)
```

**`symmetric_difference()`** ⇒ Return the symmetric difference of two sets as a new set.

**`symmetric_difference_update()`** ⇒ Update a set with the symmetric difference of itself and another.

```python
mySet = {1, 2, 3, "Four", 3.4, False, 4}
a = {1, 2, 3}

print(mySet.symmetric_difference(a)) # or
print(mySet ^ a)
mySet.symmetric_difference_update(a)
print(mySet)
```

**`issuperset()`** ⇒ Report whether this set contains another set.

**`issubset()`** ⇒ Report whether another set contains this set.

**`isdisjoint()`** ⇒ Return True if two sets have a null intersection.

```python
a = {1, 2, 3, 4}
b = {2, 3}
c = {1, 2, 3, 4, 5}
d = {11, 23, 12}

print(a.issuperset(b)) # True [ a contains {2, 3} ]
print(a.issubset(c))   # True [ c contains a ]
print(a.isdisjoint(d)) # True [ a and **d** doesn't have the same element ]
```

#### Dictionary:
[1] Dict items are enclosed in curly braces   
[2] Dict items are contains key : value   
[3] Dict key need to be immutable ⇒ (number, string, tuple) List not allowed    
[4] Dict value can have any data types   
[5] Dict Key Need To Be Unique    
[6] Dict Is Not Ordered You Access Its Element With Key    

```python
user = {
    "name": "Aymane",
    "age": 20,
    "country": "Morocco",
    "skills": ["html", "css", "python"]
}
print(user["skills"]) # or 
print(user.get("skills")
print(user.keys())
print(user.values())
```

**Two-Dimensional Dictionary:**

```python
language = {
    "FrontEnd" : {
        1: "html",
        2: "css",
        3: "js",
    },
    "BackEnd" : {
        1: "php",
        2: "mysql",
    }
}
print(language["BackEnd"])
```

**`clear()`** ⇒ Remove all items from Dict.

**`update()`** ⇒ D.update([E, ]**F) -> None. Update D from dict/iterable E and F.

Ex: 

```python
adding = {
	  "Data analysis": {
        1: "Python",
        2: "R",
        3: "PowerBI"
    }
}
language.update(adding)
print(language)
```

**`copy()`** ⇒ Return a shallow copy of Dict.

**`keys()`** ⇒ set-like object providing a view on Dict's keys

**`values()`** ⇒ ValuesView

**`setdefault()`** ⇒ Insert key with a value of default if key is not in the dictionary.

**`popitem()`** ⇒ Remove and return a (key, value) pair as a 2-tuple.

**`items()`** ⇒ return list, every list item contains tuple (key, value)

Ex: a.items() ⇒ [ (key1, value1), (key2, value2), (key3, value3) ]

**`fromkeys()`** ⇒ Create a new dictionary with keys from iterable and values set to value.

---
## Boolean, Operators, Input:
#### Boolean: 
[1] In programming you need to know your if your code output is True or False   
[2] Boolean values are the two constant objects False + True    
#### Operators:
**Boolean Operators:**

```python
100 > 20 and 1=1 # => And
100 > 20 or 1=1 # => Or
not 1=1 # => Not
```

**Assignment Operators:**

```python
 # [//=]		
 # [%=]		
 # [**=]		
 # [/=]		
 # [*=]		 
 # [-=]		 
 # [+=] 
```

**Comparison Operators:**

```python
# Equal                 ==> [==]
# Not Equal             ==> [!=]
# Greater Than          ==> [>]
# Less Than             ==> [<]
# Greater Than Or Equal ==> [>=]
# Less Than Or Equal    ==> [<=]
```

**Type Conversion:**

```python
str() # => To String
list() # => To List
tuple() # => To Tuple
set() # => To Set
dict() # => To Dict
```
#### Input:
```python
name = input("Enter Your Name: ")
print(name) 
```
---
## Control Flow:
**Syntaxe:**
```python
if_stmt ::= "if" assignment_expression ":" suite
               ("elif" assignment_expression ":" suite)*
               ["else" ":" suite]
```

**Ternary Conditional Operator:**

```python
watching = "film"
print ("Film" if watching == "film" else "Anime")
```

**Membership Operators:**

```python
# in     # not in
friends = ["yassir", "outhman", "walid", "mr1"]

print("Osama" in friends) # False
print("aymane" not in friends) # True
print("yassir" in friends) # True
```
---
## Loop:
```python
a = 0
while a < 10:
    print(a)
    a += 1
else: 
    print("Loop Is Done.")
# else will excecute when while condition is false.
```

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]
for num in numbers:
    if num%2 == 0:
        print(f"Number {num} is Even")
    else:
        print(f"Number {num} is Odd")
```

- The **`continue`** statement is used to skip the remaining code inside a loop for the current iteration only.
- The **`break`** statement in Python terminates the loop containing it.
- As its name suggests, the **`pass`** statement does nothing.
It’s used when a statement or a condition is required to be present in the program, but we do not want any command or code to execute.
---
## Functions:
[1] A Function is A Reusable Block Of Code Do A Task    
[2] A Function Run When You Call It    
[3] A Function Accept Element To Deal With Called [Parameters]    
[4] A Function Can Do The Task without Returning Data   
[5] A Function Can Return Data After Job is Finished    
[6] A Function Create To Prevent DRY [ Don't Repete Your Self ]   
[7] A Function Accept Elements When You Call It Called [Arguments]   
[8] There's A Built-In Functions and User Defined Functions    
[9] A Function Is For All Team And All Apps   
```python
def function_name():
    return ("Hello Python From Inside Function")
    # Or
    print ("Hello Python From Inside Function")

dataFromFunction = function_name()
print(dataFromFunction)
```
**Function Parameters And Arguments:**
```python
def sey_hello(name): # Here name is a parameter
    print(f"Hello {name}") # Here name is an argument
    
sey_hello("Tom")
# def                    => Function Keyword [Define]
# say_hello()            => Function Name
# print(f"Hello {name}") => Task
```
**Function Packing, Unpacking Arguments \*Args :**
```python
def say_hello(name, *skills): # Skills Is A Tuple
    print(f"Hello {name}. Your skills are: ")
    for skill in skills:
        print(f"#{skills.index(skill) + 1} {skill}")
    # skills.index(skill) + 1  => To get index of skill
say_hello("Tom", "html", "css", "php")
```

```output
Output:

Hello Tom. Your skills are: 
#1 html
#2 css
#3 php
```

**Function Default Parameters:**
```python
def say_hello(name, age, country="Unknown"):
    print(f"Hello {name} Your age is {age} and Your Country is {country}.")
    
say_hello("Tom", 20)
# You should put Your default parameter in the last place (name, age, country="Unknown")
# If you put it some place else, You will get [SyntaxError: non-default argument follows default argument]
# say_hello("Tom", "Morocco")
```

```
Output:

Hello Tom Your age is 20 and Your Country is Unknown.
```

**Fuction Packing, Unpacking Arguments \*\*KWArgs:**
```python
def show_skills(**skills): # Skills Is A Dict
    for skill, value in skills.items():
        print(f"{skill} => {value}")
        
show_skills(html="90%", css="80%", python="90%", php="60%")
```

```
Output:

html => 90%
css => 80%
python => 90%
php => 60%
```

Exemple:
```python
myTuple = ("Python", "PHP", "HTML", "CSS")
skillsWithProgress = {
    "python": "90%",
    "mysql": "70%",
    "java": "80%",
}

def show_skills(name, *skills, **skillsWithProgress):
    print(f"Hello {name}. \nYour Skills without Progress Are:")
    for skill in skills:
        print(f"#{skills.index(skill)+1} {skill}")
    print("Your Skills With Progress Are:")
    for skill, value in skillsWithProgress.items():
        print(f"-{skill} => {value}")

show_skills("Tom", *myTuple,**skillsWithProgress)
```

```
Output:

Hello Tom. 
Your Skills without Progress Are:
#1 Python
#2 PHP
#3 HTML
#4 CSS
Your Skills With Progress Are:
-python => 90%
-mysql => 70%
-java => 80%
```
**Function Scope:**
```python
x = 1 # Global Scope

def one():
    global x
    x = 2
    print(x) 
    
one() # 2
print(x) # here x comes global and get 2 as output
```

**Function Recursion:**
```python 
def cleanWord(word):
    if len(word) ==  1:
        return word
    if word[0] == word[1]:
        return cleanWord(word[1:])
    return word[0] + cleanWord(word[1:])

print(cleanWord("WWWoooorrrldd"))
```

```
Output:

Word
```
**Function lambda [ Anonymous Function ]:**
```python
def say_hello(name, age): return f"Hello {name}. Age {age}"
print(say_hello("aymane", 20))

var = lambda name, age : f"Hello {name}. Age: {age}"
print(var("aymane",20))

print(say_hello.__name__)
print(var.__name__)
print(type(var))
```

```
Output:

Hello aymane. Age 20
Hello aymane. Age: 20
say_hello
<lambda>
<class 'function'>
```
---
## Files:
#### File Handling:

`"a" Append` => Open File For Appending Values, Create File If Not Exists    
`"r" Read`   => [Default Value] Open File For Read and Give Error If File is Not Exists    
`"w" Write`  => Open File For Writing, Create File If Not Exists    
`"x" Create` => Create File, Give Error If File Exists  

```python
import os

# Return a unicode string representing the current working directory.
print(os.getcwd()) 

# Return an absolute path.
# __file__ means my local file [ This file ]
print(os.path.abspath(__file__)) 

# Directory For The Opened File
print(os.path.dirname(os.path.abspath(__file__)))

# Change Current Working Directory
os.chdir(os.path.dirname(os.path.abspath(__file__)))

file = open(r"D:\Python\Files\nfiles\osama.txt") # Here we was using 
# '\n' in \nfiles will detected as a skiped character, so we was adding 'r' character to say this is all String. 
```
#### Read Files:
```python
import os
os.chdir(os.path.dirname(os.path.abspath(__file__)))
# print(os.getcwd())

file = open("file.txt")


print(file) # File Data Object 
print(file.name) # file.txt
print(file.mode) # r
print(file.encoding) # cp1252

# Read at most size bytes, returned as bytes.
print(file.read())  

# Read and return a line from the stream.
print(file.readline())

# Return a list of lines from the stream.
print(file.readlines())

# Flush and close the IO object.
file.close()
```
#### Write and Append in Files:
```python
file = open("myFile.txt","w") 
# 'w' => Create file if not exist
#        Delete all previous file content 
file.write("Hello World\n")
file.write("Second Line.")

myList = ["Osama\n", "Ahmed\n", "Sayed\n", "Walid"]
file.writelines(myList)
file.close()


myFile = open("myFile.txt","a") 
# 'a' => Create file if not exist 
# append content to the previous one

myFile.write("\nHello All. How Are You?")
myFile.close()
```
#### Important Info:
```python
file = open("myFile.txt","a") 

# Truncate the file to at most size bytes and return the truncated size.
# In the append mode 'a'
file.truncate(5)

file = open("myFile.txt","r") 
# Return current stream position.
print(file.tell())

file.seek(6)
print(file.read())

import os
print(os.path.dirname(__file__)) # Diractory Path.

os.remove(os.path.dirname(__file__)+r"\file.txt") 
# Remove file [ file.txt ] in the same place with this file
``` 
---
## Built In Functions:

**`all()`** => Return True if bool(x) is True for all values x in the iterable. [ && ]   
- All Elements Should Be True.  

**`any()`** => Return True if bool(x) is True for any x in the iterable. [ || ]   
- At Least One Element Should Be True. 
    
**`bin()`** => Return the binary representation of an integer.   
**`hex()`** => Return the hexadecimal representation of an integer.   
**`oct()`** => Return the octal representation of an integer.   
**`id()`** => Return the identity of an object. [ Addresse ]    
**`sum()`** => Return the sum of a 'start' value (default: 0) plus an iterable of numbers   
**`round()`** => Round a number to a given precision in decimal digits.   
**`range()`** => Return an object that produces a sequence of integers from start   
**`print()`** => Prints the values to a stream, or to sys.stdout by default.   
- **file** :  a file-like object (stream); defaults to the current sys.stdout.   
- **sep** :   string inserted between values, default a space.   
- **end** :   string appended after the last value, default a newline.   
- **flush** : whether to forcibly flush the stream.   

**`abs()`** => Return the absolute value of the argument.

**`pow()`** => Equivalent to base **exp with 2 arguments or base** exp % mod with 3 arguments
Exemple:
```python
print(pow(2, 3, 4)) # (2**3) % 4 = 0 
```
**`min()`** => Return the smallest value in an iterable.    
**`max()`** => Return the largest value in an iterable  

Exemples for Functions Concept:
```python
print(all([1, 2, 3, 0])) # False
print(any(["",0,[]])) # False
print(bin(4)) # 0b100
print(hex(10)) # 0xa
print(oct(8)) # 0o10
a = 1
print(id(a)) # 2302595236080 [ Adress id ] 
print(sum([1, 2, 3, 4], 5)) # 15 <= [1, 2, 3, 4] + 5
print(round(12.256,2)) # 12.26
print(range(10)) # [0, 1, 2, 3, 4, 5, 6, 7, 8, 9] or range(0, 10) [In the lastest version of python]
print("Hello","World",sep="|", end=".") # Hello|World.
print(abs(-15)) # 15
print(min([1, 10, -50, 2.4, ])) # -50
print(max([1, 10, -50, 2.4, ])) # 10
```
**`slice()`** => Create a slice object.  This is used for extended slicing    
Exemple:
```python
a = ["A", "B", "C", "D", "E"]
print(a[slice(3)]) # ['A', 'B', 'C']
```
**`map()`** => Make an iterator that computes the function using arguments from
each of the iterables    
Exemple:
```python
# => Using Normal Function 
def formatText(text):
    return f"- {text} -"

myTexts = ["Osama", "Ahmed", "Sayed"]

print(list(map(formatText, myTexts)))
# Output: ['- Osama -', '- Ahmed -', '- Sayed -']

# => Using Lambda Function
print(list(map( lambda text : f"- {text} -" , myTexts)))
#Output: ['- Osama -', '- Ahmed -', '- Sayed -']
```
**`filter()`** => Return an iterator yielding those items of iterable for which function(item)
is true.   
If function is None, return the items that are true.  

Exemple:
```python
a = lambda num : num if (num > 10) else None

# filter doesn't return false 

print(list(filter(a, [1, 3, 12, 23, 45, 10])))
# Output : [12, 23, 45]
```
**`Reduce()`** => Apply a function of two arguments cumulatively to the items of a sequence
or iterable, from left to right, so as to reduce the iterable to a single
value.    

**For example:**  
reduce(lambda x, y: x+y, [1, 2, 3, 4, 5]) calculates ((((1+2)+3)+4)+5).  
If initial is present, it is placed before the items
of the iterable in the calculation, and serves as a default when the
iterable is empty.
```python
from functools import reduce

def sumAll(num1, num2):
    return num1 + num2

numbers = [1, 3, 5, 12, 39, 56, 199]

result = reduce(sumAll, numbers) # Or 
result = reduce(lambda num1, num2 : num1+num2, numbers) # With Lambda Function

print(result)
```

**`enumerate()`** => Return an enumerate object.
```python
mySkills = ["html", "css", "js", "python", "php"]
SkillsWithEnumerate = enumerate(mySkills, 10)
print(type(SkillsWithEnumerate)) # <class 'enumerate'>
for count, skill in SkillsWithEnumerate:
    print(f"{count} - {skill}")
    # We can modify counter or leave him as default.
```
```
Output:

10 - html
11 - css
12 - js
13 - python
14 - php
```
**`help()`** => Define the builtin 'help'

**`reversed()`** => Return a reverse iterator over the values of the given sequence.
```python
string = reversed("Tom Itadori")
for char in string:
    print(char)
```
```
Output:

i
r
o
d
a
t
I

m
o
T
```
---
## Modules, Date, Decorators:
### Modules:
**Introduction:**   
[1] Module is a file contain a set of fucntions   
[2] You can import module in your app to help you   
[3] You can import multiple modules  
[4] You can create your own modules   
[5] Modules saves your time   
```python 
# Import main module
import random
print(random)
print(f"Print Random Float Number {random.random()}")

# Show All Functions Inside Module
print(dir(random)) 

# Import One Or Two Functions From Module
from random import randint, random
print(f"Print Random Float {random()}")
print(f"Print Random Integer {randint(100, 900)}")
```

**Create Our Module:**   
We create file and we put in it some functions 
Now, In Our code we'll call it
```python 
# hello File

def say_hello():
    return "Hello Sir"

def say_bye():
    return "Bye Sir"

def say_HowAreYou():
    return "How Are You ?"
```
```python
import hello

print(hello.say_hello())
print(hello.say_bye())
print(hello.say_HowAreYou())

from hello import say_bye as sb

print(sb())
```
**Install External Packages:**   
[1] Module vs Package   
[2] External Packages Downloaded From The Internet   
[3] You Can Install Packages With Python Package Manager PIP   
[4] PIP Install the Package and Its Dependencies    
[5] Modules List "https://docs.python.org/3/py-modindex.html"    
[6] Packages and Modules Directory "https://pypi.org/"    
[7] PIP Manual "https://pip.pypa.io/en/stable/reference/pip_install/"    

```python
import pyfiglet, termcolor
# pyfiglet package takes ASCII text and renders it in ASCII art fonts
print(pyfiglet.figlet_format("Tom Itadori"))

# termcolor pachage ANSI color formatting for output in terminal.
print(termcolor.colored("Elzero", color="yellow"))
```
### Date:
**Introduction**
```python
import datetime

print(datetime.datetime.now())

print(datetime.datetime.now().year)
print(datetime.datetime.now().month)
print(datetime.datetime.now().day)

print(datetime.datetime.min)
print(datetime.datetime.max)

myBirthday = datetime.datetime(2003, 2, 13)
now = datetime.datetime.now()

print(f"I lived for {(now-myBirthday)}")
```

**Format Date:**   
Using [strftime Website](https://strftime.org/) to see all datetime format.    

```python
import datetime

myBirthday = datetime.datetime(2003, 2, 13)
print(myBirthday)

print(myBirthday.strftime("%d-%m-%Y"))
print(myBirthday.strftime("%A %B %Y"))

# %d => Number of day 
# %a or %A => Name of day [ a => Thu , A => Thursday ]
# %B or %b => Name of month 
# %m => Number of month 
# %Y => Year 
```
### Decorators:

 ***Iterable vs Iterator***   
>`Iterable: `     
[1] Object Contains Data That Can Be Iterated Upon    
[2] Examples (String, List, Set, Tuple, Dictionary)    

>`Iterator: `   
[1] Object Used To Iterate Over Iterable Using next() Method Return 1 Element At A Time    
[2] You Can Generate Iterator From Iterable When Using iter() Method    
[3] For Loop Already Calls iter() Method on The Iterable Behind The Scene    
[4] Gives "StopIteration" If Theres No Next Element    

**Generators:**     

[1] Generator is a Function With "yield" Keyword Instead of "return"    
[2] It Support Iteration and Return Generator Iterator By Calling "yield"     
[3] Generator Function Can Have one or More "yield"     
[4] By Using next() It Resume From Where It Called "yield" Not From Begining    
[5] When Called, Its Not Start Automatically, Its Only Give You The Control     

```python
def myGenerator():
  yield 1
  yield 2
  yield 3
  yield 4

myGen = myGenerator()

print(next(myGen), end=" ")
print("Hello From Python")
print(next(myGen), end=" ")

for number in myGen:
  print(number)
```


**Decorators:**    
[1] Sometimes Called Meta Programming    
[2] Everything in Python is Object Even Functions    
[3] Decorator Take A Function and Add Some Functionality and Return It    
[4] Decorator Wrap Other Function and Enhance Their Behaviour    
[5] Decorator is Higher Order Function (Function Accept Function As Parameter)    

```python
def myDecorator(func):
    def nestedFunc():
        print("#" * 10)
        func()
        print("#" * 10)
    return nestedFunc
    
    
@myDecorator
def say_hello():
    print("Hello All")
    print("HOW ARE YOU?")

say_hello()
```
```
Output:

##########
Hello All
HOW ARE YOU?
##########
```


**Decorators [ Function With Parameters ]**
```python
def myDecorator(func):
    def nestedFunc(num1, num2):
        print("#" * 50)
        if num1 < 0 or num2 < 0:
            print("Beware one of the numbers is less than zero")
        func(num1, num2)
        print("#" * 50)
    return nestedFunc


@myDecorator
def my_sum(num1, num2):
    print(f"Sum of the two numbers is",num1 + num2) 

my_sum(-10, 20)
```
---
## Modules, Error Handling:

**`zip()`**    
Exemple 1:    
```python
list1 = [1, 2, 3, 4]
list2 = ['A', 'B', 'C', 'D']

for item in zip(list1, list2):
    print(item)
```
Exemple 2:
```python
list1 = [1, 2, 3]
list2 = ['A', 'B', 'C', 'D']
tuple1 = ("man", "woman", 'boy')
dict1 = {"name": "Tom", "age":20, "country":"Morocco"}

for item in zip(list1, list2, tuple1, dict1):
    print(item)
    print(type(item)) # Tuple 
    # print("List1 item =>",item1)
    # print("List2 item =>",item2)
    # print("Tuple1 item =>",item3)
    # print("Dict1 item =>",item4, "| Value =>",dict1[item4])
```

**`Image Manipulation:`**

```python
from PIL import Image

# Open The Image
myImage = Image.open("luffy.jpg")

# Show The Image
myImage.show()

# My Cropped Image
myBox = (300, 300, 800, 800)
myNewImage = myImage.crop(myBox)

# Show The New Image
myNewImage.show()

# My Converted Mode Image
myConverted = myImage.convert("L") # Black & White
myConverted.show()
```

**`Doc String & Commenting vs Documenting:`**   

[1] Documentation String For Class, Module or Function   
[2] Can Be Accessed From The Help and Doc Attributes     
[3] Made For Understanding The Functionality of The Complex Code    
[4] Theres One Line and Multiple Line Doc Strings    

```python
# Documenting => ''' This is Documenting not Commenting '''

def person_function(name):
    '''This Function return a message to descripe that someone send message to python.'''
    return f"This is message from {name} to python."


# Return DocString in person_function.
print(person_function.__doc__)
```

**`Using Pylint For Better Code:`**    
Correct method to code in python     
To use pylint, type in terminal: `pylint.exe 'path'`
```python
"""
This File Using to learn coding with Python
"""


def say_hello(name):
    '''This function only to send message hello '''
    return f"Hello {name}."
```

**`Errors and Exception Raising: `**      

[1] Exceptions Is A Runtime Error Reporting Mechanism    
[2] Exception Gives You The Message To Understand The Problem      
[3] Traceback Gives You The Line To Look For The Code in This Line      
[4] Exceptions Have Types (SyntaxError, IndexError, KeyError, Etc...)     
[5] Exceptions List https://docs.python.org/3/library/exceptions.html      
[6] raise Keyword Used To Raise Your Own Exceptions       

```python
# How to Raise Exception
# Exemple:

x = -10
if x < 0:
    raise Exception(f"The Number {x} is less than zero")
else:
    print("Your Number is good.")
    
print("Continue Your program")
```
```
Output: 

Traceback (most recent call last):
  File "c:\Users\AYMANE\Desktop\Learning\Python\code.py", line 6, in <module>
    raise Exception(f"The Number {x} is less than zero")
Exception: The Number -10 is less than zero
```

**`Exception Handling Try, Except, else, finally: `**       

Try     => Test The Code For Errors     
Except  => Handle The Errors     

Else    => If No Errors     
Finally => Run The Code     

```python
Exemple

try:
    num = int(input("Enter Number: "))
except:
    print("This is Not Integer")
else:
    print("This is integer from else")
finally:
    print("Print from finally whatever happens")
```

```python
Exemple 2:

try:
    print(10/0)
    print(x)
except ZeroDivisionError:
    print("Can't Divide by 0")    
except NameError:
    print("variable not defined")    
except:
    print("Error Happens")
```

**`Type Hinting`**  

```python
def say_hello(name)-> str: # This is hunting to say that this function return string.
    print(f"Hello {name}")

say_hello("Tom")
```
---
## Regular Expression:
For Typing Regular Expression, use  [PyThex](https://pythex.org/) website.    
For Testing to Regular Expression [Python Regex Cheatsheet](https://www.debuggex.com/cheatsheet/regex/python)    
Regular Expression Tester [Regex101](https://regex101.com/)


#### Exemple In Regular Expression:
```python
import re
pattern = r"[\w\.]+@\w+\.\w+"
email_list = []
email_input = input("Enter Your Emain Adress\n>  ")

if re.findall(pattern, email_input):
    print("Your Email Adress is Valid")
    email_list.append(email_input)
else:
    print("You Email Adress is Invalid")
    
for email in email_list:
    print(email)
```
#### Regular Expression Functions:  

**`search()`** => Scan through string looking for a match to the pattern, returning
a Match object, or None if no match was found.   
* search.group(number)
* search.groups() 
* search.span()
* search.string()
  
```python
import re

my_search = re.search(r"[A-Z]{2}", "OOsamaEElzero")

print(my_search) # <re.Match object; span=(0, 2), match='OO'>
print(my_search.span()) # (0, 2)
print(my_search.string) # OOsamaEElzero
print(my_search.group()) # OO

is_email = re.search(r"[A-z0-9\.]+@[A-z0-9]+\.(com|net)", "os@osama.com")

if is_email:

    print("This is A Valid Email")

    print(is_email.span()) # (0, 12)
    print(is_email.string) # os@osama.com
    print(is_email.group(1)) # com
```  

**`findall()`** => Return a list of all non-overlapping matches in the string.     

**`split()`**  => Split the source string by the occurrences of the pattern,
returning a list containing the resulting substrings.

```python
import re

string_one = "I Love Python Programming-Language"

print(re.split("[\s-]", string_one,3))

string_two = "How_To-Write_A_very_Good-Article"

print(re.split("[_-]", string_two))
```
**`sub()`** => Return the string obtained by replacing the leftmost
non-overlapping occurrences of the pattern in string by the
replacement repl.

```python
import re

my_string = "I Love Python Programming Language"

print(re.sub(r"\s", "-", my_string)) # I-Love-Python-Programming-Language

print(re.sub(r"\s", "-", my_string, 2)) # I-Love-Python Programming Language
```
---
## OOP:

**`[01]`** Class is The Blueprint Or Construtor Of The Object     
**`[02]`** Class Instantiate Means Create Instance of A Class     
**`[03]`** Instance => Object Created From Class And Have Their Methods and Attributes     
**`[04]`** Class Defined With Keyword class     
**`[05]`** Class Name Written With PascalCase [UpperCamelCase] Style     
**`[06]`** Class May Contains Methods and Attributes     
**`[07]`** When Creating Object Python Look For The Built In __init__ Method     
**`[08]`** __init__ Method Called Every Time You Create Object From Class    
**`[09]`** __init__ Method Is Initialize The Data For The Object     
**`[10]`** Any Method With Two Underscore in The Start and End Called `Dunder or Magic Method`      
**`[11]`** self Refer To The Current Instance Created From The Class And Must Be First Param     
**`[12]`** self Can Be Named Anything    
**`[13]`** In Python You Dont Need To Call new() Keyword To Create Object     


Exemple:

```python
class Member:
    def __init__(self, name):
        self.name = name

    def welcome(self):
        return f"Hello, Your name Is {self.name}."
        
print(Member("Tom").welcome())
```
```
Output:

Hello, Your name Is Tom.
```


#### Class Methods & Static Methods:

**`Class Methods: `**   
- Marked With @classmethod Decorator To Flag It As Class Method     
- It Take Cls Parameter Not Self To Point To The Class not The Instance     
- It Doesn't Require Creation of a Class Instance     
- Used When You Want To Do Something With The Class Itself  
     
**`Static Methods:`**    
- It Takes No Parameters    
- Its Bound To The Class Not Instance     
- Used When Doing Something Doesnt Have Access To Object Or Class But Related To Class     

```python
class Member:
    users_num = 0
    @classmethod
    def show_users_count(cls):
        print(f"We Have {cls.users_num} Users In Our System.")
        
    @staticmethod
    def say_hello():
        print("Hello From Static Method.")
    
    
    def __init__(self, name):
        self.name = name
        Member.users_num += 1

Member("tom")
Member("mot")
Member("omt")
Member.show_users_count()
Member.say_hello()
```
```
Output:

We Have 3 Users In Our System.
Hello From Static Method.
```

**`Magic Methods:`**

Everything in Python is An Object     
**\_\_init__**  Called Automatically When Instantiating Class      
self.**\_\_class__** The class to which a class instance belongs     
**\_\_str__**   Gives a Human-Readable Output of the Object      
**\_\_len__**   Returns the Length of the Container     
          Called When We Use the Built-in len() Function on the Object    

```python
class Skill:

  def __init__(self):

    self.skills = ["Html", "Css", "Js"]

  def __str__(self):

    return f"This is My Skills => {self.skills}"

  def __len__(self):

    return len(self.skills)

profile = Skill()
print(profile)
print(len(profile))

profile.skills.append("PHP")
profile.skills.append("MySQL")

print(len(profile))

print(profile.__class__)
my_string = "Osama"
print(type(my_string))
print(my_string.__class__)
print(dir(str))
print(str.upper(my_string))
```

**`Inheritance:`**

```python
class Food:
    def __init__(self, name):
        self.name = name
        print(f"{name} Is Created From Base Class")
        
    def eat(self):
        print("Eat Method From Base Class")
        
class Apple(Food):
    def __init__(self, name):
        
        # Food.__init__(self, name) # Create Instance From Base Class
        super().__init__(name)
        print(f"{self.name} Is Created From Derived Class")
        
        
food_one = Apple().eat()
```

**`Multiple Inheritance:`**

```python
class BaseOne:

  def __init__(self):

    print("Base One")

  def func_one(self):

    print("One")

class BaseTwo:

  def __init__(self):

    print("Base Two")

  def func_two(self):

    print("Two")

class Derived(BaseOne, BaseTwo):

    pass

my_var = Derived()

print(Derived.mro()) 
# # Return a type's method resolution order.
# [<class '__main__.Derived'>, <class '__main__.BaseOne'>, <class '__main__.BaseTwo'>, <class 'object'>]


print(my_var.func_one)
print(my_var.func_two)

my_var.func_one()
my_var.func_two()
```


**`Polymorphism:`**

```python
class A:

  def do_something(self):

    print("From Class A")

    raise NotImplementedError("Derived Class Must Implement This Method")
    # You should implement your method in every derived class
class B(A):

  def do_something(self):

    print("From Class B")

class C(A):

  def do_something(self):

    print("From Class C")

my_instance = B()
my_instance.do_something()
```

**`Encapsulation:`**

- Restrict Access To The Data Stored in Attirbutes and Methods   
   
Public     
- Every Attribute and Method That We Used So Far Is Public       
- Attributes and Methods Can Be Modified and Run From Everywhere       
- Inside Our Outside The Class     
  
Protected
- Attributes and Methods Can Be Accessed From Within The Class And Sub Classes      
- Attributes and Methods Prefixed With One Underscore _       
  
Private       
- Attributes and Methods Can Be Accessed From Within The Class Or Object Only      
- Attributes Cannot Be Modified From Outside The Class       
- Attributes and Methods Prefixed With Two Underscores __      

```python
class Member:
    def __init__(self, name, age, country):
        self.name = name # Public
        self._age = age # Protected
        self.__country = country # Private
        
        
one = Member("Ahmed", 90, "Morocco")
```

**`Getters & Setters:`**

```python 
class Member:
    def __init__(self, name):
        self.name = name 
    
    def get_name(self):
        return self.name

    def set_name(self, new_name):
        self.name = new_name
        
one = Member("Ahmed")
print(one.get_name())
one.set_name("tom")
print(one.get_name())
```

**`Property Decorator:`**

```python
class Member:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    
    def say_hello(self):
        return f"Hello {self.name}"
    
    @property
    # To Swith from method to property. 
    def age_in_days(self):
        return self.age * 365
    
    
one = Member("Ahmed", 20)

print(one.say_hello())
print(one.age_in_days)
```

**`Abstract Base Class:`**

```python
from abc import ABCMeta, abstractmethod

class Programming(metaclass=ABCMeta):

  @abstractmethod
  def has_oop(self):

    pass

  @abstractmethod
  def has_name(self):

    pass

class Python(Programming):

  def has_oop(self):

    return "Yes"

class Pascal(Programming):

  def has_oop(self):

    return "No"

  def has_name(self):

    return "Pascal"

one = Pascal()

print(one.has_oop())
print(one.has_name())
```
---
## SQLite:

**`Introduction:`**

- Database Is A Place Where We Can Store Data
- Database Organized Into Tables (Users, Categories)
- Tables Has Columns (ID, Username, Password)
- There's Many Types Of Databases (MongoDB, MySQL, SQLite)
- SQL Stand For Structured Query Language
- SQLite => Can Run in Memory or in A Single File
- You Can Browse File With https://sqlitebrowser.org/
- Data Inside Database Has Types (Text, Integer, Date)

```python
import sqlite3

# Create Database Anad Connect
db = sqlite3.connect("app.db")

# Create Tables and Fields
db.execute("CREATE TABLE IF NOT EXISTS skills (name TEXT, progress INTEGER, user_id INTEGER)")

# Close Database
db.close()
```

**`Insert Data Into Database:`**

- cursor => All Operation in SQL Done By Cursor Not The Connection Itself
- commit => Save All Changes
  
```python
import sqlite3

# Create Database Anad Connect
db = sqlite3.connect("app.db")

# Setting Up The Cursor
cr = db.cursor()

# Create Tables and Fields
cr.execute("CREATE TABLE IF NOT EXISTS users (user_id INTEGER, name TEXT)")

cr.execute("CREATE TABLE IF NOT EXISTS skills (name TEXT, progress INTEGER, user_id INTEGER)")

# Insert Data Into Database
cr.execute("INSERT INTO users(user_id, name) values (1, 'Ahmed')")
cr.execute("INSERT INTO users(user_id, name) values (2, 'Sayed')")

# Save (Commit) Changes
db.commit()

# Close Database
db.close()
```
**Exemple To Insert A List Into Database:**

```python
import sqlite3

# Create Database Anad Connect
db = sqlite3.connect("app.db")

# Setting Up The Cursor
cr = db.cursor()

# Create Tables and Fields
cr.execute("CREATE TABLE IF NOT EXISTS users (user_id INTEGER, name TEXT)")

cr.execute("CREATE TABLE IF NOT EXISTS skills (name TEXT, progress INTEGER, user_id INTEGER)")

# Insert Data Into Database
my_list = ["Ahmed", "Sayed", "Mahmoud", "Ali", "Kamel", "Ibrahim", "Sameh", "Enas"]
for name in my_list:
    cr.execute(f"INSERT INTO users (user_id, name) VALUES ({my_list.index(name)+1}, '{name}')")

# Save (Commit) Changes
db.commit()

# Close Database
db.close() 
```

**`SQLite Retrieve Data From Database:`**

- fetchone => returns a single record or None if no more rows are available.
- fetchall => fetches all the rows of a query result. It returns all the rows       
            as a list of tuples. An empty list is returned if there is no record to fetch.
- fetchmany(size)


> fechone():
```python
cr.execute("SELECT * FROM users")
print(cr.fetchone())
print(cr.fetchone())
```
```
Output:

(1, 'Ahmed')
(2, 'Sayed')
```

> fechall():
```python
cr.execute("SELECT * FROM users")
print(cr.fetchall())
```
```
Output:

[(1, 'Ahmed'), (2, 'Sayed'), (3, 'Osama')]
```

> fechmany(size):
```python
print(cr.fetchmany(2))
```
```
Output:

[(1, 'Ahmed'), (2, 'Sayed')]
```


**Practice Exemple:**
```python
import sqlite3
def get_all_data():
    try:
        # Connect to db
        db = sqlite3.connect("app.db")
        print("Connected To Database Successfully.")
        
        # Setting Up The Cursor
        cr = db.cursor()
        
        # Fetch Data From Database
        cr.execute("SELECT * FROM users")
        
        # Assign Data To Varaible
        result = cr.fetchall()
        
        # Pring Number Of Rows
        print(f"Number Of Rows: {len(result)}")
        
        # Printing Message
        print("Showing Data:")
        
        # Loop On Results
        for count, row in result:
            print(f"UserID => {count}, Username => {row}")
    except sqlite3.error as er:
        print(f"Error Reading Data {er}")
    finally:
        if db:
            # Close Database Connection
            db.close()
            print("Connection To Database Is Closed")


get_all_data()
```

**`SQLite Update And Delete From Database:`**

```python
cr.execute("UPDATE users SET name = 'Itadori' WHERE user_id = 2")

cr.execute("DELETE FROM users WHERE user_id = 4")

cr.execute("SELECT * FROM users")
print(cr.fetchall())
```


**`SQLite Very Important Information`**

```python
# Import SQLite Module
import sqlite3

# Create Database And Connect
db = sqlite3.connect("app.db")

# Setting Up The Cursor
cr = db.cursor()

my_tuple = ('html', '50', 3)

# Inserting Data
cr.execute("insert into skills values(?, ?, ?)", my_tuple) # SQL Injection

# Fetch Data From Database
cr.execute('SELECT * FROM skills')

cr.execute("select * from skills order by name")

cr.execute("select * from skills order by name limit 3")

cr.execute("select * from skills order by name limit 3 offset 2")

cr.execute("select * from skills where user_id > 1")

cr.execute("select * from skills where user_id not in(1, 2, 3)")

# Assign Data To Variable
results = cr.fetchall()

# Loop On Results
for row in results:

    print(f"Skill Name => {row[0]},", end=" ")
    print(f"Skill Progress => {row[1]},", end=" ")
    print(f"User ID => {row[2]}")
# Save (Commit) Changes
db.commit()

# Close Database
db.close()
```
---
