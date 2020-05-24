# Assignment 2 #

For this assignment we will be modifying our code to be more reusable and adding a menu driven interface to it. The hard requirements for this assignment are:

1. Separate the integer calculations into methods and put them in a class separate from your main class (Sum, Evens, Odds, Max, Min).
   * Keep the integer calculation methods free of any printing. 
   * Your Main class shall handle all the UI functionality.
2. On first run of the application prompt user for initial list of integers (not as command line arguments).
3. Add a menu for the user with the following options:
   1. Update Integer List
        * Prompts user to input new list of integers. 
        * This time allow users to do any integer (negative, 0 and positive)
        * Validate that all the inputs are valid integers
   2. Sum
   3. Evens
   4. Odds
   5. Max
   6. Min
   7. Exit
4. Allow the user to select any of the above operations, output the results then loop back unless the user selects 'Exit'.
5. Make sure the methods are commented well as well as your classes.

As far as how you should make the user interface to work you may do a number based menu where the user just enters a number for option they want to execute. Or you could have the user type their command out. However you do it just make sure that the user can input a list of integers once then run any number operations on that list until they decide to update it.

Possible example:

```[console]
> java Main
Welcome to Ethan Brown's CS3230 Project!
Please Enter a List of Integers:
> -1 2 -3 4 -5
Choose an Operation:
1. Sum - sum the integers
2. Evens - find the evens
3. Odds - find the odds
4. Max - find the max
5. Min - find the min
6. Update - enter a new list of integers
7. Exit
> 5
Min: -5
Choose an Operation:
1. Sum - sum the integers
2. Evens - find the evens
3. Odds - find the odds
4. Max - find the max
5. Min - find the min
6. Update - enter a new list of integers
7. Exit
> 7
Goodbye!
```