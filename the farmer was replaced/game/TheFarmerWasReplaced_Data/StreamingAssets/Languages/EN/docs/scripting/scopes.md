# Name Scopes
Scopes determine which variables can be accessed from where. A scope is basically a mapping from names to values.
They work almost the same as in Python, but not always, so be sure to read this section carefully.

Just like Python, there is a global scope, and each function has a local scope.
When you define a variable, it gets added to the current scope.
Anything outside of a function definition is considered part of the global scope.

`x = 1`
Assigns a value of `1` to the name `x` in the global scope.

This `def` statement assigns a function to the name `f` in the global scope.
`def f():
    `Assign a value of `1` to the name `y` in the local scope of `f`.`
    y = 1

    `Assign a function to the name `g` in the local scope of `f`.`
    def g():
        pass`

`f()`
Retrieves the function stored in `f` from the global scope and calls it.

`print(y)`
This print statement in the global scope throws an error because `y` was never declared in the global scope so we can't read it here.
It only existed in the local scope of `f`.


Loops and branches do not create their own scopes, so anything declared within them can still be used outside.

`for i in range(3):
    pass
print(i)`

This will print `2` because the last iteration of the `for` loop assigned `2` to `i`.

Everything up to here is the same in Python. The first difference is in how global definitions from other files are imported. Python uses the import statement for this, the game imports global functions automatically.

Any functions defined in loaded files will be added to the global scope before execution, so you can use functions declared in other files.
Note that this is not the case for global variables. They are only available when the line where they are assigned actually runs. Only the global scope of the window on which you click the execute button will be executed.

Variables from the global scope can be read anywhere, but assignments will always assign to the local scope.

`x = 1

def f():
    x += 1

f()

print(x)`

This code prints `1` not `2` because `x += 1` will first read `1` from the global variable `x` and then assign `2` to a new local variable that is also called `x`.
So the global variable `x` is never changed.

This behavior differs slightly from that of Python.
Python throws an error here because you are trying to read from a local variable before it is assigned.

In Python it is also possible to use the 'global' keyword to declare that you want to use the global variable instead of the local one, but this is not supported in this game.

If you really need to update global variables you can use a dictionary for it.
They use reference semantics, which means that the variable holds a reference to the underlying dictionary, rather than storing the data structure directly in the variable.
A global variable can store a reference to a dictionary that can be read in a function.
You can modify the underlying dictionary without updating the variable in the global scope.
Since the variable in the global scope still points to the same dictionary, it will also reflect any changes made to that dictionary. To illustrate, consider the following code:

Assign dictionary in global scope
`d = {"x": 1}

def f():
    `make a change to the dictionary that is referenced by `d`.`
    d["x"] += 1

`prints `2
print(d["x"])`