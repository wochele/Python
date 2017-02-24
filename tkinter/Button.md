# Button

```
#Modified Button Click Function
def clickMe():
    action.configure(text='Hello ' + name.get())

# Adding a Button
action = ttk.Button(win, text="Click Me!", command=clickMe)   
action.grid(column=1, row=1)
```

