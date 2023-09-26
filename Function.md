Function: 

A block of reusable code that performs a specific task.

You can pass data, known as parameters, into a function.

A function can return data as a result.

Examples of parameters, return values, and diiferent scopes.

Function Parameters:

def write_a_book(character, setting, special_skill):
  print(character + " is in " + 
        setting + " practicing her " + 
        special_skill)

Multiple Parameters: 

def ready_for_school(backpack, pencil_case):
  if (backpack == 'full' and pencil_case == 'full'):
    print ("I'm ready for school!")

Return Value:

def add(a, b):
 
    # returning sum of a and b
    return a + b
 
def is_true(a):
 
    # returning boolean of a
    return bool(a)
 
# calling function
res = add(2, 3)
print("Result of add function is {}".format(res))
 
res = is_true(2<5)
print("\nResult of is_true function is {}".format(res))

Returning Multiple Values:

lass Test:
    def __init__(self):
        self.str = "geeksforgeeks"
        self.x = 20  
   
# This function returns an object of Test
def fun():
    return Test()
       
# Driver code to test above method
t = fun() 
print(t.str)
print(t.x)

Globals() scope:

score = 23
globals()['score'] = 10
print('The Score is:', score)
OUTPUT:
The Score is: 10

Locals() scope:

# Without using local variables
def test_1():
    print("No local variable : ", locals())
# Using local variables
def test_2():
    Language = "Python Programming"
    print("Local variable: ", locals())
test_1()
test_2()
OUTPUT:
No local variable :  {}
Local variable :  {'Language': 'Python Programming'}

Dir() scopes:

scores = [5, 2, 3]
print(dir(scores))
print('\n Return values from the empty dir()')
print(dir())
OUTPUT:  
['__add__', '__class__', '__contains__', '__delattr__', '__delitem__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__gt__', '__hash__', '__iadd__', '__imul__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__rmul__', '__setattr__', '__setitem__', '__sizeof__', '__str__', '__subclasshook__', 'append', 'clear', 'copy', 'count', 'extend', 'index', 'insert', 'pop', 'remove', 'reverse', 'sort']
 Return values from the empty dir()
['__annotations__', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', 'scores']

Vars() scope:

class Scores:
    def __init__(self, Roll_1 = "Alice", Roll_2 = "Bella", Roll_3 = "Cindrella"):
        self.Roll_1 = Roll_1
        self.Roll_2 = Roll_2
        self.Roll_3 = Roll_2
score = Scores()
print(vars(score))
OUTPUT:
{'Roll_1': 'Alice', 'Roll_2': 'Bella', 'Roll_3': 'Bella'}
