# Model-View-Controller (MVC)

- Model
  - Representation and interface to the data. Allows pulling of data from database without knowing the intricacies of the underlying database.
  - Provides and abstraction layer so the same model can be used with different databases.
- View
  - What is seen - The presentation layer for the model
  - Provides and interface to collect us
  er input
- Controller
  - Controls the flow of information between the model and view
  - Decides what information is pulled from the database via the model and what information is passed to the view
  - Gets information from the user via the view and implements business logic by changing the view or modifying data through the model or both
  
