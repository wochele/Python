# Combo Box

### Basic Combobox

```
numberChosen = ttk.Combobox(win, width=12, textvariable=number)
numberChosen['values'] = (1, 2, 4, 42, 100)
numberChosen.grid(column=1, row=1)
numberChosen.current(0)
```

If we want to restrict the user to only be able to select the values we have programmed into the Combobox, we can do that by passing the state property into the constructor. 

```
numberChosen = ttk.Combobox(win, width=12, textvariable=number, state='readonly')
```

### Get value from Combobox

```
numberChosen.get()
```

