# 1.4 Interpret Python scripts containing data types, functions, classes, conditions, and looping


## Variables

- Define value in one place and reuse it in many places
- Collect data from outside systems and use that value

## Data Types

### Numeric Types

#### int

- Whole number without any decimals

#### float

- Floating-point decimal number

### String Types

- Grouping of text characters surrounded by single or double quotes

#### Bytes

- Binary string
- Default string type in python2
- Support for fewer characters


#### Unicode

- UTF-8 string
- Default string type in python3
- Support for more characters


### Boolean

- True/False value

### Collections


#### Lists

- Ordered collection of unnamed items
- Zero-indexed - position numbering starts at 0 and counts up
- Can be called by ordinal position

```
fruits = ["apple", "banana", "strawberry", "orange", "pear"]
print(fruits[3])
"strawberry"
```

- Mutable: values in list can be changed

```
fruits.append("kiwi")
print(fruits)
["apple", "banana", "strawberry", "orange", "pear", "kiwi"]
```

#### Dictionaries

- Unordered collection of named items
- Key/Value pairs
- Called by key

```
favorite_fruits = {"me": "grapefruit", "jim": "grapes", "mary": "peach"}
print(favorite_fruits["jim"])
"grapes"
print(favorite_fruits.get("mary")
"peach"
```

- Mutable

```
favorite_fruits["lucy"] = "blueberries"
print(favorite_fruits)
{"me": "grapefruit", "jim": "grapes", "mary": "peach", "lucy": "blueberries"}
```

#### Tuples

- Immutable list: cannot change, add, or remove values once they have been assigned

```
animals = ("dog", "cat", "mouse")
animals[2] = "rat" # results in a TypeError
```

## Conditionals

### if

- Only execute code under certain conditions
- Can optionally add additional conditions to check if a preceding condition is not met

```
foo = "bar"
if foo == "spam":
    print("foo is spam")
elif foo == "ham":
    print("foo is ham")
elif foo == "eggs":
    print("foo is eggs")
else:
    print(f"foo is {foo}")
"bar"
```


## Loops

### for

- Iterate over a fixed sequence (list, tuple, dict under certain circumstances)

```
states = ["Maine", "Idaho", "Iowa"]
for state in states:
    print(state)
"Maine"
"Idaho"
"Iowa"
```

### while

- Iterates until a condition is false

```
cont = True
while cont:
    cont_prompt = input("Do you want to continue? (y/n) ")
    if cont_prompt.lower().startswith("n"):
        cont = False
    elif cont_prompt.lower().startswith("y"):
        pass
    else:
        print("I did not recognize your input.")
```


## Functions

- Named block of code that can be invoked at any other point during the execution of the program
- Can be run multiple times over the course of the program

```
def greeter():
    print("Hello!")
greeter()
"Hello!"
```
- Can accept data prior to running (parameters) and return/yield data after execurtion

### Parameters

```
def greeter(name):
   print(f"Hello, {name}!" 
greeter("Jimmy")
"Hello, Jimmy!"
```

## Classes

- Custom data type
- Represent objects or ideas
- Example: Class is a blueprint
  - Blueprint can be used to make one or more houses with the same structure but is not the same as the house itself
  - Not all objects houses have to be identical - properties of houses can differ (roof can be different color, floor can have hardwood instead of carpet, etc)
- Class is defined by state and behavior
  - State: properties/variables
  - Behavior: methods/functions

```
class House(object):
    walls = 4

    def __init__(self, length, width, floors):
        self.length = length
	self.width = width
	self.floors = floors

    def calculate_perimeter(self):
        perimeter = (2 * self.length) + (2 * self.width)
	return perimeter

    def calculate_area(self):
        area = (self.length * self.width) * self.floors
	return area
    
my_house = House(40, 25, 2)
jeffs_house = House(30, 20, 3)

print(my_house.calculate_area())
2000
print(jeffs_house.calculate_area())
1800
```
