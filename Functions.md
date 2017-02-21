# Functions

```
def hello():
    print('Howdy!')
    print('Howdy!!!')
    print('Hello there.')
```

### Arguments

- Most arguments are identified by their position in the function call.
- *keyword arguments* are identified by the keyword put before them in the function call.
    - `print('Hello', end='')`
- Default values
    - `def describe_pet(pet_name, animal_type='dog'):`
    - When you use default values, any parameter with a default value needs to be listed after all the parameters that don’t have default values. This allows Python to con-tinue interpreting positional arguments correctly.


### Return value

- The `return` statement uses the return keyword and value or expression that should be returned
- Numerous returns could be in a function to allow it to break early with a value
- Functions which do not return a value like print() still return the value 'None'
    - Behind the scenes, Python adds return None to the end of any func-tion definition with no return statement.

### Modifying a list in a function

When you pass a list to a function, the function can modify the list. Any changes made to the list inside the function’s body are permanent, allowing you to work efficiently even when you’re dealing with large amounts of data.


    
