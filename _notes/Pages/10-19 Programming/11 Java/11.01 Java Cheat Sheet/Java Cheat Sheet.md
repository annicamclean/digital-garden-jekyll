Hi there. This is a java cheat sheet that will show you the basics of the programming language Java and aid you in creating programs with Java. Enjoy reading.

  

# Printing

Printing is one of the first concepts you will learn in  most languages including Java. Java has multiple print statements that will print out strings, numbers, and variables.

  

The 3 main printing statements are:

```java

public class Main {

    public static void main(String[] args) {

        System.out.print("");

        System.out.println("");

        System.out.printf("");

    }

}

```

*Notice how each line without a curly bracket has a semicolon. They are mandatory to have at the end on the line without a curly bracket.*

  

The first print statement will output anything you want and **WILL NOT** go to a new line.

```java

public class Main {

    public static void main(String[] args) {

        System.out.print("Welcome");

        System.out.print(" to ");

        System.out.print("my program");

    }

}

```

The output will be:

Welcome to my program

**OUTPUT ENDED**

  

*The output would be represents what would happen if you ran the code in java. Every line after the output would be line is what is outputted. It ends when the words **OUTPUT ENDED** in bold*

  

The second print statement will output anything you want and **WILL** go to a new line.

```java

public class Main {

    public static void main(String[] args) {

        System.out.println("Welcome");

        System.out.println(" to ");

        System.out.println("my program");

    }

}

```

The output will be:

Welcome

  to

my program

**OUTPUT ENDED**

  

The third print statement is like the first except it is used to format variables. Each percent sign represents a variable (more on variables in the next section).

```java

public class Main {

    public static void main(String[] args) {

        String program = "program";

        int numOfPrograms  = 152;

        System.out.printf("Welcome to my new %s.", program);

        System.out.printf(" I have created %d programs", numOfPrograms);

    }

}

```

The output will be:

Welcome to my new program. I have 152 programs.

**OUTPUT ENDED**

  

# Variables

Variables are a very important part of most programming languages. In Java there are 3 parts to creating a new variable. You need the datatype, the variable name, and the value.

  

## Creating A New Variable

### Datatype

The datatype(type) is the first part in creating a variable. There are a lot of different datatypes, but for the basics there are strings, doubles, ints, floats, chars, booleans, and arrays. I know that sounds like a lot, but you will remember them as you keep going. There are also other datatypes that are objects. I will cover more about objects later, but the main ones which are strings and a scanner(we will talk about soon) fall into objects. The others mentioned above are primitive datatypes.

  

### Variable Names

The variable name is the second part of creating a new variable. Variable names can almost be whatever you want. Most will recommend that you use **MEANINGFUL** names so that when others or you read it you can understand what is going on in your program. Variables cannot have a space in between the name and cannot start with a number. To mitigate this problem programmers either use camel case or underscores to show separate words. Camel case is when the first letter is lower case and the start of every new word is uppercase.(thisIsHowCamelCaseLooks) With underscorse you just change spaces for underscores. (this_is_a_variable_with_underscores) While creating this cheat sheet I will only use camel case. For the numbers problem most people will add the number to the back of the variable or spell out the word. For example if you want a variable to signify the first number the variable cannot be named 1stNumber, but it can be number1 or firstNumber.

  

### Variable Value

The variable value is the last part of variable creation. It comes after the equals sign and has to match the datatype. Matching the datatype means that ints can only store whole numbers, doubles and floats store decimal numbers, strings store a string, a chars stores one character and so on. The only time it does not have to match is when doubles and floats can store whole numbers.

  

Here is an example of creating the main variables up above:

```java

public class Main {

    public static void main(String[] args){

        int wholeNumber = 10;

        float floatingNumber = 3.5;

        double doubleNumber = 6.9235;

        boolean booleanValue = false;

        char aCharacter = 'L';

        String aString = "This is a great string";

    }

}

```

*Notice how the char has single quotes while the string has double quotes. They have to be that way and they are not interchangeable*

## Printing variables

  

You print out variables by using any of the print statements like we talked about earlier.

  

Here is 3 different ways to print out the same thing:

```java

public class Main {

    public static void main(String[] args){

        int myAge = 25;

  

        System.out.print("I am " + myAge + " years old");

        System.out.println("");

        System.out.println("I am " + myAge + " years old");

  

        System.out.printf("I am %d years old", myAge);

    }

}

```

The output would be:

I am 25 years old

I am 25 years old

I am 25 years old

**OUTPUT ENDED**

  

*Notice how in the print and println the plus sign is used to add in the variable while in the printf the % and comma is used.*

  
  

Using printf to print out different variables:

```java

public class Main {

    public static void main(String[] args){

        int myAge = 25;

        System.out.printf("I am %d years old", myAge);

        System.out.println("");

  

        float money = 2100;

        System.out.printf("I have $%,.2f in my pocket", money);

        System.out.println("");

        double division = 19.0 / 6;

        System.out.printf("The equation 19 / 6 = %f", division);

        System.out.println("");

  

        boolean youngerThan30 = true;

        System.out.printf("It is %B that I am younger than 30", youngerThan30);

        System.out.println("");

  

        String name = "John Smith";

        char firstNameInitial = 'j';

        System.out.printf("His name is %s and the first name initial is %C", name, firstNameInitial);

        System.out.println("");

    }

}

```

The output would be:

I am 25 years old

I have $2,100.00 in my pocket

The equation 19 / 6 = 3.166666666667

It is TRUE that I am younger than 30

His name is John Smith and the first name initial is J

**OUTPUT ENDED**

  

*Notice how the boolean and char have capitalized letters. This allows the variable to be capitalized the lowercase version of the letter will make it lowercase. Also notice how there is a .2 after the percent sign for the double variable. This just means the variable has to have 2 places after the decimal. The comma infront of the decimal gives the number commas and will keep adding commas every 3 numbers.*

  

## Reassigning Variables

Reassigning variables is slightly simpler than creating new variables. All you need is the same variable name and a new value. It is separated by an equal sign. It also must match the previous datatype from when it was created.

  

Here is an example:

```java

public class Main {

    public static void main(String[] args) {

        int myAge = 25;

  

        System.out.println("My age is " + myAge);

  

        myAge = 35;

  

        System.out.println("Actually my age is " + myAge);

    }

}

```

The output would be:

My age is 25

Actually my age is 35

**OUTPUT ENDED**

  

## User input

Some of the time you don't only want a predetermined value, but also user inputted values or values that change due to user input. That is when the Scanner object comes in. There are 3 parts to the Scanner object: the import statement, creating the scanner variable, and using the scanner.

  

### The Import Statement

The import statement(s) are the first line(s) in the java program. This is only not true if there is a package statement in your program. If there is then it is the second line(s). To write the import line you write import then whatever you want to import. For the scanner it is import java.util.Scanner;.

  

### Creating The Scanner Variable

The second part is creating the Scanner variable. This must be done before you actually use the variable. The datatype for the scanner is Scanner. For the variable it can be something like in, input, scanner, or something else meaningful. The value of the scanner is new Scanner(System.in). Altogether it is Scanner input = new Scanner(System.in);. This only needs to be created once, but can be used multiple times.

  

### Using The Scanner

The third part is actually using the scanner. For this you need to have a prompt and then the scanner variable that will hold the user input. You need to have a prompt so your user knows what they should be typing in. A prompt is just a System.out.print() statement. The user input variable must have a datatype that matches the user input, a meaningful name, and the input value. It should look something like int userInteger = input.nextInt();

  

#### Dissecting the Value

input.nextInt() is the value mentioned above when using the scanner. Lets take a moment to dissect it to understand it better. First you have input and input should match the variable you created in the "Creating The Scanner Variable" section. Then you have the period. It represents calling a method(function) for an object. That may sound foreign if you have never heard of that term, but it will be talked about later. All you need to know is that it is needed. The next part is the nextInt(). The "next" part must always be used with the correct datatype so if it is an int it must be nextInt if it is a boolean in needs to be nextBoolean. The times that it is different is if it is a String or a char. For strings you need to use either next or nextLine depending on if it doesn't have or does have spaces respectively. For chars you would use next().charAt(0). Again if you have never programmed before this may not make any sense, but it will make more sense as you go.

  

### Examples

  

Now lets put it all together now in an example.

```java

import java.util.Scanner;

  

public class Main {

    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);

  

        System.out.print("Please enter your first name: ");

        String name = input.next();

  

        System.out.print("Please enter your age: ");

        int age = input.nextInt();

  

        System.out.println("Your name is " + name);

        System.out.println("You are " + age + " years old.");

    }

}

```

The output would be:

Please enter your first name: ==Jack==

Please enter your age: ==19==

Your name is Jack

You are 19 years old.

**OUTPUT ENDED**

  

*Notice that there are parts highlighted in the output. The highlights represent the user input and any other user input will be represented by highlighting what is the user input*

# Conditional Statements

Conditional statements are a key part of programming. They are constantly used to control what may happen in a program. There are a few different types of conditional statements in Java, but we will only go over the 2 main ones. If statements and Switch statements.

  

## If statements

The if statement has 2 parts to it. You have the keyword of if and the conditional. The if statement also ends with curly brackets so **DO NOT** add a semicolon to the end of the condition or the curly brackets.

  

Here is an example of an if statement:

  

```java

public class Main {

    public static void main(String[] args) {

        int age = 25;

  

        if (age > 20) {

            System.out.println("You can drink in the US");

        }

    }

}

```

The output would be:

You can drink in the US

**OUTPUT ENDED**

  

The if statement is saying if the variable age is greater than 21 then output the statement "You can drink in the US". If it is not true then do nothing.

  

### Comparison Operators

If you noticed up above the condition (in the parentheses) has a greater than sign. When you are creating conditionals you have some type of comparison that will evaluate to true. When it comes to **PRIMITIVE** datatypes you can use >, <, >=, <=, !=, == . In order they are greater than, less than, greater than or equal to, less than or equal to, not equal to, and equal to (equivalent to). These comparison operators do not work for Objects such as Strings and Scanners. Instead strings and other objects have their own ways to compare the same object.

  

#### Comparing Strings

Like we talked about above objects like strings have methods (something we will talk about later) that can be used to change the string and compare strings to other strings. You use the methods equals, equalsIgnoreCase, and compareTo. The 2 equal methods will return either true or false, while compareTo will return either a negative number, a zero, or a positive number.

  
  

```java

public class Main {

    public static void main(String[] args) {

        String str1 = "Hello";

        String str2 = "World";

        String str3 = "Hi";

  

        System.out.println(str1.compareTo(str2));

        System.out.println(str2.compareTo(str2));

        System.out.println(str3.compareTo(str1));  

    }

}

```

The output would be:

-15

0

4

**OUTPUT ENDED**

  

Other helpful methods to use for comparison would be compareToIgnoreCase, contains, endsWith, isEmpty, and length. The methods contains, endsWith, and isEmpty all return either a true or false value. The method compareToIgnoreCase is just like compareTo method excepts the case is ignored. The length method will return how long the string is(int).

  

Here is how you would use all of the methods:

```java

public class Main {

    public static void main(String[] args) {

        String str1 = "How is life";

        String str2 = "Hello, World";

        String str3 = "program";

        System.out.println(str1.contains("World"));

        System.out.println(str2.endsWith("World"));

        System.out.println(str1.isEmpty());

  

        System.out.println(str1.length());

  

        System.out.println(str3.compareToIgnoreCase("PROGRAM"));

    }

}

```

The output would be:

false

true

false

11

0

**OUTPUT ENDED**

  

## Else Statements

An else statement is highly similar to an if statement, it just lacks the condition. *An else statement must have an if conditional*. It first checks the if statement conditionals, if it is true it does what is in the curly brackets, else it does whatever is in the else statement's curly brackets. It may be hard to understand so I will show you:

  

```java

public class Main {

    public static void main(String[] args) {

        int age = 20;

  

        if (age >= 18) {

            System.out.println("You can vote in the US");

        } else {

            System.out.println("You CANNOT vote in the US");

        }

  

        if (age >= 21) {

            System.out.println("You can drink in the US");

        } else {

            System.out.println("You CANNOT drink in the US");

        }

    }

}

```

The output would be:

You can vote in the US

You CANNOT drink in the US

**OUTPUT ENDED**

## Else-If Statements

An else if statement is exactly like an if statement the only difference is that the else keyword comes before the if keyword. Also just like an else statement it needs an if statement before it. Here is an example:

  

```java

public class Main {

    public static void main(String[] args) {

        int age = 25;

  

        if (age < 18) {

            System.out.println("You are younger than 18");

        } else if (age >= 18) {

            System.out.println("You can vote in the US");

        } else if (age >= 21) {

            System.out.println("You can drink in the US");

        } else {

            System.out.println("You can vote and drink in the US");

        }

    }

}

```

The output would be:

You can vote in the US

**OUTPUT ENDED**

  

If you look at the result you will notice that it will only print out the first else-if statement. That is because once one of the conditions is met it will not look for any other condition after it. A way to fix it is to change the order of the conditions.

  

## Multiple Conditions

Sometimes when you are creating a condition you may want to have more than one condition before something executes. You can of course use nested if statements like so:

```java

public class Main {

    public static void main(String[] args) {

        int age = 10;

        int height = 48;

  

        if (age > 8) {

            if (height > 50) {

                System.out.println("You can ride the roller coaster");

            }

        }

    }

}

```

The output would be:

**OUTPUT ENDED**

  

*It ends right after it begins because there is no output due to the second if statement being false*

  

Or you could use an and operator (&&) to get the same results.

```java

public class Main {

    public static void main(String[] args) {

        int age = 10;

        int height = 48;

  

        if (age > 8 && height > 50) {

            System.out.println("You can ride the roller coaster");

        }

    }

}

```

The output would be:

**OUTPUT ENDED**

  

There are 3 operators the AND operator, the OR operator, and the NOT operator. The AND operator looks like this: && and only happen if both parts of the conditions are true. The OR operator looks like this: || and happen if one or the other condition is true. The NOT operator looks like this: ! and changes the condition to false/ checks to see when it is false. With the not operator it takes the condition an evaluates it. If it is true it becomes false and if it is false it becomes true. With all of the operators they have an order of evaluation. It goes NOT, AND, then OR. It also goes from left to right. So if a programmer wanted to add the operators without paratheses they could. Also paratheses come before the NOT operator. You can add as many operators as you want to the condition.

## Switch Statements

A switch statement takes the idea of if statements and only looks for when the condition is equivalent to the case. There are 3 parts of a switch statement: the switch, the cases, and the break.

### The Switch

The switch part of the switch statement uses the keyword switch and the variable that will be used to compare.

### The Cases

The cases are the part of the switch statement that has the value that will be compared to the switch variable.

### The Break Statement

The break statement is needed after every case for the switch statement to work. Without them if a case is true above it at any point it will do every other case no matter what.

  

Now this is just a bunch of words without an example. So here is an example:

```java

public class Main {

    public static void main(String[] args) {

        int age = 13;

  

        switch (age) {

            case 13:

                System.out.println("You are a teenager");

                break;

            case 18:

                System.out.println("You are able to vote");

                break;

            case 21:

                System.out.println("You can drink in the US");

                break;

            default:

                System.out.println("You can do it all");

                break;

        }

    }

}

```

The output would be:

You are a teenager

**OUTPUT ENDED**

  

*Try taking out the breaks to see what happens*

*Also notice there is a default statement. The default is like else statement in which it runs if nothing else matches the other condition.*

  

# Loops

Loops can be a bit confusing to many, but I will try to explain them in the most simple way. Loops are like an if statement that keeps happening until to condition becomes false. There are 4 loops in java called: a while loop, a do-while loop, a for loop, and a for each loop. We will go over all, but the for each loop.

## While Loop

While loops looks the most like an if statement. Instead of the if keyword it becomes the while keyword. *Remember that the while loop will only execute if the condition is true.* Here is an example:

```java

public class Main {

    public static void main(String[] args) {

        int count = 0;

  

        while (count < 10) {

            System.out.println("Count: " + count);

            count++;

        }

    }

}

```

The output would be:

Count: 0

Count: 1

Count: 2

Count: 3

Count: 4

Count: 5

Count: 6

Count: 7

Count: 8

Count: 9

**OUTPUT ENDED**

  

*Notice how there are 2 pluses after the variable count. By doing that you are able to add 1 to a variable quickly.*

### Shorthand for Operations

As mentioned before you can add two plus signs after an int variable to add one to the variable. You can also add 2 minus signs to subtract 1 from an int variable. You can not add two multiplication signs (\*\*) nor two division signs  (//). Also it would be redundant to multiple or divide a number by 1. But there is also another way to add, subtract, multiply, and divide a number to the variable. You essentially write whatever the operation is and add an equal sign. Here is examples of the long form and shorthand forms.

```java

public class Main {

    public static void main(String[] args) {

        int number = 10;

  
  

        //long form (works for all numbers)

        number = number + 1;

        // a shorter form (works for all numbers)

        number += 1;

        //shortest form (only works for 1)

        number++;

    }

}

```

  

*There are lines above the code that start with 2 forward slashes(//). These are known as comments. Here is an example of the 3 types of comments in java:*

```java

public class Main {

    public static void main(String[] args) {

  

    /*

        This is a multiline comment

    */

  
  

    //This is a single line comment

  
  

    /**

    * This is a javadoc comment

    */

    }

}

```

*Comments are used to help others and yourself read and understand the code that has been written*

## Do While Loops

A do-while loop just like a while loop except whatever is in the bracket is done first before the condition is even checked. So you write the keyword do, then the curly brackets, and then whatever you want to do, then the keyword while with your condition and a semicolon at the end. Here is an example:

```java

public class Main {

    public static void main(String[] args) {

        int ages = 13;

  

        System.out.println("Teenagers ages are: ");

  
  

        do {

            System.out.print(ages + " ");

            ages++;

        } while (ages < 20);

    }

}

```

The output would be:

Teenagers ages are:

13 14 15 16 17 18 19

**OUTPUT ENDED**

  

## For Loops

A for loop is if you take the variable that you want to change as the loop goes, the condition, and the actual changing of the variable added it altogether and put it where the condition used to go. So first you start with the keyword for, then you add the parentheses and in the paratheses you add in the new variable you want to change, then the condition, then the  changing of the variable. Here is an example:

  

```java

public class Main {

    public static void main(String[] args) {

        for (int i = 0; i < 10; i++) {

            System.out.println("i. " + i);

        }

    }

}

```

The output would be:

i. 0

i. 1

i. 2

i. 3

i. 4

i. 5

i. 6

i. 7

i. 8

i. 9

**OUTPUT ENDED**

### Infinite Loops

When writing loops make sure your loop has a way to actually stop. If it doesn't it will cause an infinite loop. An infinite loop is when a condition is never met, so it keeps repeating over and over again until you stop it. *I even did it while writing this.* Make sure you always have a way to end and leave the loop.

  

# Methods

Methods are smaller parts of a program that allow the programmer to call it multiple times or separate parts of a program to make it more readable. There are 5 parts of of creating a method. There is public vs private, static or non-static, the method type, the name, and the parameters.

  

## Creating a Method

### Public vs Private

A method can either be private or public. The difference is if a method outside of the class it is made in is allowed to call the method (calling methods will be covered soon). If it is public it can be called and it cannot be called if it is private. The keyword public is not actually needed, but should be used for readability.

  

### Static or Non-static

A static or non-static method mostly depends on how you are using the method. The need to know when to use static comes up when you are creating other classes. For right now all of the methods in the main class need to have the word static in the declaration (the creation).

  

### Method Types

A method type is the same as a variable datatypes and has one extra type called void. The datatypes like int, double, String etc. all return the type specified in the the creation of the method. If you use void it does not return anything. This is best shown through examples (which will be shown later).

  

### Method Names

A method name is just like a variable name. It should be **MEANINGFUL** as mentioned when naming variables and cannot have spaces nor start with a number.

  

### Parameters

Parameters are a way to transport values from the other methods to the method you have created. You write parameters(inside a set of paratheses) by giving it a datatype then adding the variable name. You can have multiple parameters and separate them with a comma.

  

## Calling Methods

Once you have created the method now comes the easier part of calling the method. To call a method you need the method name and the needed arguments. The arguments should match the parameter in the amount and the datatypes. If a method is not a void method then the results can be stored into a variable. That variable must match the datatype that is being returned.

  

Here is an example of methods:

```java

    import java.util.Scanner;

    public class Main {

    public static void printNumbers(int sum, int sub, int multiply, double divide) {

        System.out.println("The sum: " + sum

        + "\nThe subtraction: " + sub + "\nThe multiplication: " +

        multiply + "\nThe division: " + divide);

    }

    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);

  

        System.out.print("Eneter the first whole number: ");

        int num1 = input.nextInt();

        System.out.print("Eneter the second whole number(cannot be 0): ");

        int num2 = input.nextInt();

  

        int sum = sum(num1, num2);

        int sub = sub(num1, num2);

        int mul = multiply(num1, num2);

        double div = divide(num1, num2);

  

        printNumbers(sum, sub, mul, div);

    }

    public static int sum(int num1, int num2) {

        int sum = num1 + num2;

        return sum;

    }

    public static int sub(int num1, int num2) {

        int sub = num1 - num2;

        return sub;

    }

    public static int multiply(int num1, int num2) {

        return num1 * num2;

    }

    public static double divide(int num1, int num2) {

        return (double) num1 / num2;

    }

}

```

The output would be:

Eneter the first whole number: ==10==

Eneter the second whole number(cannot be 0): ==7==

The sum: 17

The subtraction: 3

The multiplication: 70

The division: 1.4285714285714286

**OUTPUT ENDED**

  

*Notice there is a \\n and it is allowing the print to go down a line. This is an Escape Character.*

### Escape Characters

Escape characters are symbols used to control the output of the print statement. The main ones I would know is \\n, \\t, \\", \\', \\\\. \\n goes to a next line. \\t tabs over in the same line. \\" allows the quotation mark to show when using it already in the print statement. \\' is the same as \\" except for single quotation marks. \\\\ is for showing a backslash in the print statement.

# Arrays

Arrays are a slightly complex topic, so I will try my best to explain with topics we have already gone over. An array is taking a bunch of variables and putting them all into one variable and managing it. You can access any of the array indices(the "variables" inside of the main variable) are accessed by using square brackets (\[\]) and a whole number or a variable holding a whole number (int variable or char but I don't recommend using a char).

  

## Creating an Array

You create an array buy starting with the datatype you want the array to hold. *An array can only have one datatype.* Then you add square brackets right after to signify that it is an array and not a normal variable. Then you need your array variable name. Then you add the equals sign and after that there are 2 ways to finish creating a new array. You can either put the keyword new then the datatype that has to match the same one on the other side and then square brackets with the number of indices you want in-between them. The second way is to take all the values separate each one with a comma and add curly brackets around the values. The first way is if you don't know the values you want to have in the array. The other way is if you know the values before you create the array.

  

Here are the 2 ways to create an array:

```java

public class Main {

    public static void main(String[] args) {

        int[] array1 = new int[5];

        int[] array2 = {1, 2, 3, 4, 5};

    }

}

```

  

## Changing and Printing Indices

You can change the value of an indices of an array by typing the array name, followed by square brackets with the index (singular of indices), then the equal sign and the new value after the equal sign. You print one index of the array by using a sout (System.out.print/ln/f) then adding the array and the square brackets with the index in the brackets inside of the paratheses. To print out the entire array it's best to use a loop. You can either use a for loop or a for-each loop.

  

Here is an example of everything:

```java

public class Main {

    public static void main(String[] args) {

        int[] intArray = {1, 2, 3, 4, 5};

  

        System.out.println("The first index is: " + intArray[0]);

  

        intArray[0] = 15;

  

        System.out.println("The new first index is: " + intArray[0]);

  

        System.out.println("The Entire Array:");

        //for loop

        for (int i = 0; i < intArray.length; i++) {

            System.out.print(intArray[i] + " ");

        }

  

        System.out.println();

        System.out.println("The Entire Array Again:");

        //for-each loop

        for (int number : intArray) {

            System.out.print(number + " ");

        }

    }

}

```

The output would be:

The first index is: 1

The new first index is: 15

The Entire Array:

15 2 3 4 5

The Entire Array Again:

15 2 3 4 5

**OUTPUT ENDED**

  

*Things you may have noticed:*

1. *The first index starts at 0*

2. *The condition of the for loop has intArray.length*

3. *A for-each loop looks very different*

  

When using arrays or Strings to get the first index or character(letter) you use the number 0. The .length method for arrays is just like the Strings .length method. The for each loop is similar to the regular for loop. The for-each loop essentially runs for the length of the array, and each time changes the variable value (on the left side before the colon) with a value in the array (on the right side of the colon). The for-each loop is mostly used to print out the indices of an array.

## Multi-dimensional Arrays

A multi-dimensional array allows you to hold arrays inside of arrays.

  

Here is everything learned about 1 dimensional arrays applied to a 2 dimensional(2D) array:

```java

public class Main {

    public static void main(String[] args) {

        int[][] newArray = new int[2][3];

  

        newArray[0][0] = 200;

  

        System.out.println("The index in the first row and column is: " + newArray[0][0]);

  

        //giving a number other than 0 in each index

        for (int i = 0; i < newArray.length; i++) {

            for (int j = 0; j < newArray[i].length; j++) {

                newArray[i][j] = i + j + 1;

            }

        }

  

        //printing out the array

        System.out.println("The Entire Array");

        for (int[] row : newArray) {

            for (int number : row) {

                System.out.print(number + " ");

            }

            System.out.println();

        }

    }

}

```

The output would be:

The index in the first row and column is: 200

The Entire Array

1 2 3

2 3 4

**OUTPUT ENDED**

  

*Noticed that when giving the numbers to the array the for loops have 2 different letter variables used (i, j). That is because of the scope of the variable i. If you use i for the nested loop then you will mess up the loop variable, so different variables must be used for each nested loop.*

  

# Objects and Classes

This is the last thing that I will talk about in this little cheat sheet for java. In java an object is a user or already created datatype that has attributes (variables) and methods that can be used. The class is where you create the methods and attributes that the object can use. If you remember from earlier in this cheat sheet it was mentioned that Strings and the Scanner (used for user input) are both Objects. So lets go over Objects and Classes.

  

## Classes

As mentioned before Classes are where you create the attributes and methods that you will allow the object to use. You are able to create as many classes as you want and can name it whatever you would like.

  

### Attributes

Attributes are essentially variables that are specific for the class. The class attributes are usually private because we usually do not want the user to easily change the variable. By making the variable private no other class (like the main) can easily access it.

  

### Methods

A method is just like the other method we talked about earlier in the cheat sheet. The methods are either private (if it only needs to be used in that class) or public (needs to be used outside the class). 2 popular methods used with attributes are the getter and setter method.  

  

#### Getter and Setter Methods

The getter and setter methods as mentioned before are used to get and change(set) the attributes of a class. Hence the name getter and setter. How the method is usually named is getAttribute and setAttribute. So if the attribute(private variable) is named "name" the the getter and setter is getName and setName.

  

### Constructors

A constructor is what gets used to create the the object in other classes. There is an automatic constructor that gets created when you make the new class. There is also another construct you have to create in order to use the constructor. The constructor takes all of the attributes, adds them to the parameter, then changes the attributes in the class.

  

Here is everything that is in a new class if we made a class called Journal:

```java

public class Journal {

    //attributes

    private String cover = "";

    private String paperType = "";

    private int numOfPages = 0;

    private boolean hasBookmark = false;

  

    //not needed but nice to have

    public Journal() {

    }

  

    //how I would write the second constructor

    public Journal(String cover, String paperType, int numOfPages,

        boolean hasBookmark) {

        this.cover = cover;

        this.paperType = paperType;

        this.numOfPages = numOfPages;

        this.hasBookmark = hasBookmark;

    }

  

    //another way to write it, but I don't use it

    /*public Journal(String nCover, String nPaperType, int nNumOfPages,

        boolean nHasBookmark) {

        cover = nCover;

        paperType = nPaperType;

        numOfPages = nNumOfPages;

        hasBookmark = nHasBookmark;

    }*/

  
  

    //all of the getters and setters

    public String getCover() {  

        return cover;  

    }  

    public void setCover(String cover) {  

        this.cover = cover;  

    }  

    public String getPaperType() {  

        return paperType;  

    }  

    public void setPaperType(String paperType) {  

        this.paperType = paperType;  

    }  

    public int getNumOfPages() {  

        return numOfPages;  

    }  

    public void setNumOfPages(int numOfPages) {  

        this.numOfPages = numOfPages;  

    }  

    public boolean isHasBookmark() {  

        return hasBookmark;  

    }  

    public void setHasBookmark(boolean hasBookmark) {  

        this.hasBookmark = hasBookmark;  

    }

}

```

*If you noticed there is another constructor that is commented out. That is just another way to write the same thing. Another thing you may have noticed is that the class has a capitalized name. That is how most classes are created, with the first letter being capitalized.*

  

## Objects

Objects are the second part of this chapter. An object is the actual use of the class in a place outside of the class it was created.

  

### Creating an Object

If you remember how we created a Scanner object, then creating any object is pretty simple. For the datatype of the variable it is the name of the object. Then you have the variable name. Then on the right side of the equal sign you have new then which ever constructor you would like to use. So if I used the example with the journal before it would look something like this:

```java

Journal newJournal1 = new Journal();

  

Journal newJournal2 = new Journal("hard", "grid", 240, true);

  

Scanner input = new Scanner(System.in);

  

```

*The scanner is there to help you compare it to the objects that were created before*

  
  

### Calling the Object's Methods

After you have created a new object you can call its methods by adding a period after the variable name that is holding the object. After the period you add the method name, the parentheses, and any arguments needed for the method.

  

Here is an example of calling a method with the creation of a new object and class:

```java

import java.util.Scanner;

  
  

public class Main {

    public static void main(String[] args) {

        //Creating the Scanner Object

        Scanner input = new Scanner(System.in);

  

        //Creating a journal object with predefined attributes

        Journal averageJournal = new Journal("hard", "lined", 180, true);

  

        //Creating a journal object with attributes that will be changed

        Journal yourJournal = new Journal();

  

        //Prompting user for the type of journal cover

        System.out.print("What type of cover does your journal have? ");

        String cover = input.next();

  

        //Prompting user for the type of paper

        System.out.print("What type of paper is it? ");

        String paper = input.next();

  

        //Prompting user for the amount of pages

        System.out.print("How many pages are in your journal? ");

        int pages = input.nextInt();

  
  

        //Asking user if has a bookmark in the journal

        System.out.print("Does it have a bookmark? ");

        boolean bookmark = input.nextBoolean();

  

        //Adding all the attributes to the journal

        yourJournal.setCover(cover);

        yourJournal.setPaperType(paper);

        yourJournal.setNumOfPages(pages);

        yourJournal.setHasBookmark(bookmark);

  

        //Printing out everything about the second journal

        System.out.print("Your journal has a " + yourJournal.getCover() + " cover");

        System.out.print(", " + yourJournal.getPaperType() + " paper");

        System.out.print(", " + yourJournal.getNumOfPages() + " pages");

        if (yourJournal.isHasBookmark()) {

            System.out.println(", and a bookmark.");

        } else {

            System.out.println(", and does not have a bookmark.");

        }

    }

}

  

public class Journal {

    //attributes

    private String cover = "";

    private String paperType = "";

    private int numOfPages = 0;

    private boolean hasBookmark = false;

  

    //not needed but nice to have

    public Journal() {

    }

  

    //how I would write the second constructor

    public Journal(String cover, String paperType, int numOfPages,

        boolean hasBookmark) {

        this.cover = cover;

        this.paperType = paperType;

        this.numOfPages = numOfPages;

        this.hasBookmark = hasBookmark;

    }

  

    //all of the getters and setters

    public String getCover() {  

        return cover;  

    }  

    public void setCover(String cover) {  

        this.cover = cover;  

    }  

    public String getPaperType() {  

        return paperType;  

    }  

    public void setPaperType(String paperType) {  

        this.paperType = paperType;  

    }  

    public int getNumOfPages() {  

        return numOfPages;  

    }  

    public void setNumOfPages(int numOfPages) {  

        this.numOfPages = numOfPages;  

    }  

    public boolean isHasBookmark() {  

        return hasBookmark;  

    }  

    public void setHasBookmark(boolean hasBookmark) {  

        this.hasBookmark = hasBookmark;  

    }

}

```

The output would be:

What type of cover does your journal have? ==Hard==

What type of paper is it? ==Grid==

How many pages are in your journal? ==240==

Does it have a bookmark? ==true==

Your journal has a Hard cover, Grid paper, 240 pages, and a bookmark.

**OUTPUT ENDED**

  

Here is an second example using a new class:

```java

public class Main {

    public static void main(String[] args) {

  

    Job myJob = new Job();

    myJob.setSalary(100000);

    myJob.setTitle("Software Engineer");

  
  

    myJob.jobDesc();

    myJob.hourlyPay();

    }

}

  

public class Job {

    private double salary = 0;

    private String title = "";

  

    void jobDesc() {

        System.out.println("The job is: " + title + "\nThe salary is: $" + salary);

    }

  

    public void setSalary(double salary2) {

        salary = salary2;

    }

  

    public void setTitle(String title2) {

        title = title2;

    }

  

    public void hourlyPay() {

        double hourPay = salary / 40 / 52;

        System.out.printf("The jobs hourly pay is: $%,.2f", hourPay);

    }

}

```

The output would be:

The job is: Software Engineer

The salary is: $100000.0

The jobs hourly pay is: $48.08

**OUTPUT ENDED**

  

This is the basics of Java, and while I didn't go into deep detail I believe it is enough to get you started. I hope you enjoyed reading.