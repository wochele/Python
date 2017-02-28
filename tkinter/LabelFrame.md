# Label Frame

```

# Create a container to hold labels
labelsFrame = ttk.LabelFrame(win, text=' Labels in a Frame ')
labelsFrame.grid(column=0, row=7)

# Place labels into the container element
ttk.Label(labelsFrame, text="Label1").grid(column=0, row=0, sticky=tk.W)
ttk.Label(labelsFrame, text="Label2").grid(column=1, row=0, sticky=tk.W)
ttk.Label(labelsFrame, text="Label3").grid(column=2, row=0, sticky=tk.W)

```

- The frame is created in the main 'win'
- The labels use the frame in their constructor and grid corrdinates based on it
