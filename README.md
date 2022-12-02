# Summative Assessment 6 - 

This assessment is summative - which means that you get feedback for completing this, and marks from this work count towards your final mark for this portfolio.

## ToDo List

- [ ] [:key: Give examples of when you have called a method that already exists.](#Method_Call)
- [ ] [:key: Demonstrate how to write and call a method, and how to pass data into a method and get data out of a method.](#How_To_Write_And_Call_A_Method,_And_How_To_Pass_Data_Into_A_Method_And_Get_Data_Out_Of_A_Method.)
- [ ] [:key: Demonstrate how to use methods to increase readability and reduce scope.](#Methods_To_Increase_Readability_And_Reduce_Scope.)
- [ ] [:key: Demonstrate the use of optional parameters and method overloading.](#Demonstrate_The_Use_Of_Optional_Parameters_And_Method_Overloading.)
- [ ] [:speech_balloon: Express new semantics](#semantics)
- [ ] [:thought_balloon: Reflect on what you have learnt](#reflection)
- [ ] [:question: Request feedback (optional)](#requesting-feedback)
- [ ] :white_check_mark: Get your work checked off by a feedback engineer

## Method Call.
We call methods regularly when programming, procedure/rutines that are pre built in Visual studio for C# are called methods.  

eg.
```C#
string input;
input = Console.ReadLine();
Console.Writeline(input);

```


## How To Write And Call A Method, And How To Pass Data Into A Method And Get Data Out Of A Method.
you declare a method along its type in the following format [Data Type] [Method name] () . After that in pointy brackets you code its purpose. the method can be called into and object of the same data type for the data to be stored. u can pass data through it using the Interpolated String technique by declaring the objects in the brackets after the method name while calling it.

```C#

int Getage()
{
    Console.WriteLine("What is your Age?");
    int age = int.Parse(Console.ReadLine());
    return age;
}
int Age = Getage();

string GetName()
{
    Console.WriteLine("What is your name?");
    string name = Console.ReadLine();
    return name;
}

String Name = GetName();

void NameAge(string pName, int pAge)
{
    Console.WriteLine($"Hello, {pName} your age is {pAge} ");
}

NameAge(Name, Age);


```

## Methods To Increase Readability And Reduce Scope.

 The variables pMessage and pRepetitions are only in scope whilst the method is called. Once execution leaves the method these variables are no longer in scope. Reducing scope is useful because it means that you only need to be concerned about a small part of a problem at a time.

```cs
void MessageRepeater(string pMessage, int pRepetitions)
{
  for(int i = 1; i <= pRepetitions; i++)
  {
    Console.WriteLine($"{i}. {pMessage}");
  }
}
```

When a method is called the calling code provides arguments/ The types of the arguments must match the parameters defined in the method. The values of these arguments are copied into the variables pMessage and pRepetitions. In the code below the MessageRepeater method is called twice. this inceases the readability and reduces the scope of the code.

```cs
MessageRepeater("Hello, World!", 5);
MessageRepeater("Goodbye!", 3);
```

## Demonstrate The Use Of Optional Parameters And Method Overloading.
Method overloading allows us to have two methods with the same name, but with different sets of parameters. For example, we could also create a method called SumValues that has two integer paramters, and just returns the sum of those two integers, or three integer values, or four, and so on.

```cs
int[] numbers = { 10, 2, 5, 7, 13, 8, 4 };
int sum = SumValues(numbers);

Console.WriteLine(sum);

numbers = { 1, 2, 3, 4, 5 };

sum = SumValues(numbers);

Console.WriteLine(sum);


```

Optional parameters allow you to specify arguments in a method signature that the caller of the method is free to omit. In other words, while you must specify values for required parameters, you might choose not to specify values for optional parameters.

When a method is called the calling code provides arguments/ The types of the arguments must match the parameters defined in the method. The values of these arguments are copied into the variables pMessage and pRepetitions. In the code below the MessageRepeater method is called twice.



```cs
MessageRepeater("Hello, World!", 5);
MessageRepeater("Goodbye!", 3);
```




The MessageRepeater method does not return a value to the calling code. Instead the keyword void indicates that this method does not return anything.



You can specify default values for a parameter in a method declaration. For example the following method specifies a default value for pRepetitions. When the method is called if no value is provided for pRepetitions then the default value of 1 will be used.



```cs
void MessageRepeater(string pMessage, int pRepetitions = 1)
{
  for(int i = 1; i <= pRepetitions; i++)
  {
    Console.WriteLine($"{i}. {pMessage}");
  }
}
```



## Requesting Feedback

This section is optional, but encouraged. Feedback is crucial to the learning process. If you have any questions about what you have learnt this week record them here for your demonstrator to answer. **Replace** the bullet points below with any questions you might have.
- Why are we here?
- What is the meaning of life?

## Semantics

In order to talk about programming we need to establish a set of core terminology, or "semantics". In this context "semantics" means the words we use to talk about programming. This is different to Syntax, which is what we type to tell the computer what we want it do to. It is important that when we use words that have
a special meaning in the context of programming we share a common understanding.

Complete this table of semantics with your understanding of what these terms mean:

| Word | Meaning |
|---|---|
|Method Signature|  A method signature is a unique identification of a method for the C# compiler. The signature consists of a method name and the type and kind (value, reference, or output) of each of its formal parameters. Method signature does not include the return type. Any legal character can be used in the name of a method |
|Parameter|  Parameters act as variables inside the method. They are specified after the method name, inside the parentheses. You can add as many parameters as you want, just separate them with a comma.|
|Argument|  the actual value sent to the function when its called |
|Return type|  the value returned by the funtion after exicution |
|Method Call|  A method in C# is a code block that contains a series of statements. A program runs the statements by calling the method and specifying arguments |
|Method Scope|  Whenever we define a variable within a method, it is assigned the method level scope. and we cannot access it outside this method. This variable cannot overwrite or be overwritten by a variable of the same name from a higher scope. |
|Overloaded Method|  2 or more methods with the same name in a class with different parameters and types |
|Optional Parameter|  parameters for which u dont need to specify values etc. |
|Refactor|  refractoring allows you to alter the structure of the code without effecting its outcome. |



## Reflection
In this section you should reflect upon what you have learnt. This is an important part of the learning process.
- What have you learnt from these exercises?
- How can you apply what you have learnt?
- What new features of C# are you now able to use?#
