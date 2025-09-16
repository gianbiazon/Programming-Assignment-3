# Programming-Assignment-3

This repository contains solutions to identify the codes and functions needed in cleaning and visualizing data and be able to apply and use the different codes and functions in creating a Python program that will be used in data wrangling and data visualization












Problem #1.1 - ECE BOARD EXAM PROBLEM - Using data wrangling and data visualization technique with storytelling, analyze the data and present different data frames and visuals using the dataset given

Code:

            import pandas as pd
            cars = pd.read_csv('cars.csv')
            cars.head()
            cars.tail()


Output:

First 5 cars:  
            <img width="696" height="217" alt="image" src="https://github.com/user-attachments/assets/4b11c45b-dda0-4931-84ff-177ad8932bf9" />  
            

Last 5 cars:  
            <img width="669" height="230" alt="image" src="https://github.com/user-attachments/assets/1318cbc8-11ce-4261-9cde-181415dcdda0" />



Analysis:
            In order to display the first and last 5 cars, the syntax head() is for displaying the first 5 cars and tail() is for displaying the last 5 cars. They are crucial for the first and last 5 cars to be displayed. It is also flexible, wherein you can indicate a specific number of items you want to display, but by default, or by not putting any value inside the parentheses, it displays the first and last 5 items.










Problem #1.2 - ECE BOARD EXAM PROBLEM - Create a visualization that shows how the different features contribute to the average grade. Does the chosen track in college, gender, or hometown contribute to a higher average score?

Code:

        import pandas as pd
        cars = pd.read_csv('cars.csv')
        cars

        cars.loc[(cars['Model'] == 'Mazda RX4')]

        cars.loc[(cars['Model'] == 'Camaro Z28') , ['cyl']]

        cars.loc[cars.Model.isin(['Mazda RX4 Wag','Ford Pantera L','Honda Civic']),                      
        
        ['Model','cyl','gear']]


Output:

a. First five rows with odd-numbered columns of cars

<img width="410" height="225" alt="image" src="https://github.com/user-attachments/assets/9817cbae-e904-40f6-91a3-9580dc04a558" />

b. Row that contains the ‘Model’ of ‘Mazda RX4’

<img width="635" height="70" alt="image" src="https://github.com/user-attachments/assets/ed6afa04-c8ef-4c7d-bb03-6f670c933847" />

c. How many cylinders (‘cyl’) does the car model ‘Camaro Z28’ have

<img width="92" height="72" alt="image" src="https://github.com/user-attachments/assets/91b7500b-2a1f-4d77-80fb-af1cbab0e218" />

d. How many cylinders (‘cyl’) and what gear type (‘gear’) do the car models ‘Mazda RX4 Wag’, ‘Ford Pantera L’ and ‘Honda Civic’ have.

<img width="267" height="155" alt="image" src="https://github.com/user-attachments/assets/70c1fa7c-15cc-4672-8c48-a4765bf3a35b" />


Analysis: In problem a, the important syntax is .iloc[], the syntax calls the specific item by locating it using its index which is indicated inside its brackets. In the problem, to get the first five rows and the only odd-numbered columns. :5 is used to locate the first five rows, while ::2 is used to get the only odd-numbered columns. For problem b, the syntax cars[cars.Model == ' Mazda RX4'] calls the column model, then finds every model element-wise to get the item mazda rx4. For problem c, .loc is similar with iloc, but the exact item is declared inside its parenthesis, .item is used to get the single value only, it is used to make the result cleaner which is required in the problem that only asked for how many cylinder does the item camaro z28 have. For problem d, isin is used to select multiple models at once and display only model,cyl,and gear columns. It is important to show how to filter multiple conditions and view and the columns needed in the question.

