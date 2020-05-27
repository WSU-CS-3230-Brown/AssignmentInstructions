# Assignment 3 #

Let's add some functionality to our new menu based UI. 

## Part 1 - More Maths ##

Add methods to your math class that will find the **mean**, [**standard deviation**](https://www.programiz.com/java-programming/examples/standard-deviation) and the [**5 number summary**](https://www.statisticshowto.com/how-to-find-a-five-number-summary-in-statistics/) for the list of numbers. 

> NOTE: You'll notice the 5 number summary is really 5 different calculations on the data and 2 of these are ones you've already implemented. Make sure you aren't repeating code for this.

> NOTE2: You'll also notice that the **mean** and **standard deviation** aren't going to be nice round integers. Make sure you handle the floating point results properly and when you print the results of these truncate the result to 4 decimals places.

## Part 2 - Strings ##

We are also going to add a whole new set of functionality for your application. Let's do some string operations. Since these are not related to doing anything with integers we are going to need a new class. You can name this class whatever makes sense to you. We will be filling it with various methods that do stuff to strings. Some suggestions: StringOperations, StringFunctions or Stringinator. I'm not too worried about it. 

In this class we will start with a method that will take a list of `String` and check if they are a **palindrome**. It will return a list of `Boolean` that corresponds with each string in the input list. You will then need to print these out in your menu.

> NOTE3: A **palindrome** is a string of characters that is the same forwards or backwards. ie: racecar, 10101, abccba

Here is an example of the palindrome method input and output:
```[java]
List<String> listOfStrings = new ArrayList() {{
        add("racecar");
        add("foo");
        add("javaj");
    }}
List<Boolean> resultList = StringOperations.isPalindrome(listOfStrings);
resultList ==> [true, false, true]
```

You'll need to update your menu to include these functions. Also it looks like we may need a couple new menus to separate this functionality.

Here is a possible example:

```[console]
> java Main
Welcome to Ethan Brown's CS3230 Project!
Top Menu:
1. String Operations
2. Math Operations
3. exit
> 1
Enter a list of strings: Ethan Brown aaaa 
String Operations:
1. Palindrome Check
2. Back to main
> 1
Ethan: Not a palindrome
Brown: Not a palindrome
aaaa: Is a palindrome
String Operations:
1. Palindrome Check
2. Back to main
> 2
Top Menu:
1. String Operations
2. Math Operations
3. exit
> 3
Goodbye!
```
