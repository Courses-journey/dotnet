# .NET CSharp

Metigator | عصام عبدالنبي

[[01] - Mastering C#.NET | احترف سي شارب](https://www.youtube.com/playlist?list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l)

## Important to Note

- This course was published and taught using `.NET 5`.
  - It's possible that something which was not valid in that version may become valid in future versions.
  - There may also be syntax changes

## 003 Variables

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_003/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=j87UkenRf7k&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=4)

- Content

- DECLARATION
- INITIALIZATION
- ASSIGNMENT
- INTEGER VALVE TYPE
- STRING REFERENCE TYPE
- STACK VS HEAP
- STRING CONCATENATION

### STACK VS HEAP

### COMMENT

#### Single Line Comment

```c#
// this is a comment
```

#### Multiline Line Comment

```c#
/* this
* is
* a multi
* line
* comment
*/
```

### DECLARATION

```c#
// 1. Declaration [ <DataType> <identifier>; ]
int num;
```

### ASSIGNMENT

```c#
int num;
// 2. Assignment [ <identifier> = <value>; ]
num = 5;
```

### INITIALIZATION

```c#
// 3. Initialization [ <DataType> <identifier> = <initial Value>; ]
int num2 = 5;
```

### STRING CONCATENATION

```c#
// regular concatenation (plus sign)
string s3 = s1 + " " + s2;
```

### STRING INTERPOLATION

```c#
// regular concatenation (plus sign)
string s4 = $"{S1} {S2}";
```

### STRING REFERENCE TYPE

```c#
// string Reference Type
string s1;

s1 = "Issam";

string s2 = "A.";
```

### INTEGER VALVE TYPE

#### sbyte

```C#
Console.WriteLine($"sbyte: [{sbyte.MinValue} > {sbyte.MaxValue}]"); // [-128 + 127]
```

#### byte

```C#
Console.WriteLine($"int: [{byte.MinValue} > {byte.MaxValue}]"); // [0 + 255]
```

#### short

```C#
Console.WriteLine($"int: [{short.MinValue} = {short.MaxValue}]"); // [-32, 768 - 32, 767]
```

#### ushort

```C#
Console.WriteLine($"ushort: [{ushort.MinValue} > {ushort.MaxValue}]"); // [0 > 65, 535]
```

#### int

```C#
Console.WriteLine($"int: [{int.MinValue} > {int.MaxValue}]"); // [-2, 147, 483, 648 2, 147, 483, 647]
```

#### uint

```C#
Console.WriteLine($"uint: [{uint.MinValue} > {uint.MaxValue}]"); // [0 > 4, 294, 967, 295]
```

#### long

```C#
Console.WriteLine($"long: [{long.MinValue} >> {long.MaxValue}]"); // [-9, 223, 372, 036, 854, 775, 808 - 9, 223, 372, 036, 854, 775, 807]
```

#### ulong

```C#
Console.WriteLine($"ulong: [{ulong.MinValue} > {ulong.MaxValue}]"); // [0 > 18, 446, 744, 073, 709, 551, 615]
```

#### float

```C#
Console.WriteLine($"float: [{float.MinValue} > {float. MaxVaue}]"); // [+1.5 x 10-45 > #3.4 x 1038]
```

#### double

```C#
Console.WriteLine($"double: [{double.MinValue} > {double.MaxValue}]"); // [5.0 x 10-324 -> #1.7 x 10308]
```

#### decimal

```C#
Console.WriteLine($"decimal: [{decimal.MinValue} > {decimal.MaxValue}]"); // [+1.0 x 10-28 > 7.9228 x 1028]
```

### var vs dynamic

#### var

variable type will be the first assignment to it

```c#
var s1 = "Issam"; // s1 will be string
var f = 0f; // float
var d = 0d; // double

int oneMillion = 1_000_000;
```

#### dynamic

considered as object

```c#
dynamic x = 9;
x = "abc";
x = 10m;
```

### char

char is a value type stored in the stack

## 004 Boolean Types & Operators

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_004/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=D9VD0mn6mss&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=5)

- Content

  - Expression
  - Equality operators
  - Comparison operator
  - Equality and REF.Type
  - Conditional operator
  - Short circuit `&&` vs `&`
  - Ternary operator

### Expression

An expression in C# is

```
A combination of operands (variables, literals, method calls) and operators that can be evaluated to a single value.
```

- Declaration
  `<type> <Identifier>`
- Assignment
  `<Identifier> = value`
- Initialization
  `<type> <Identifier> = value`

```c#
//Declaration
bool isWalking;
//Assignment
isWalking = true;

//Initialization
bool isRunning = true;
```

### Equality operators

```c#
var x = 10;
var y = 10;

Console.WriteLine( x == y) // x IS equal to y?
```

### Comparison operator

- `>` greater than
- `<` less than
- `>=` greater than or equal
- `<=` less than or equal
- `==` equality

#### Negation

- `!` not

### Conditional operator

- `&&` Logical and
  - To return true: All operands must be true
- `||` Logical or
  - To return true: one of the operands must be true
- `^` Logical xor
  - To return true: If operands are different from each other

### Short circuit `&&` vs `&`

- `&` and `|` check all
- `&&` and `||` make short circuit

### Reference Type

```
CLR internally calls isEqual()
thats why the result is true
```

```c#
var s1 = "hello"; // reference type
var s2 = "hello"; // reference type

//if address is different then check for letters
var s3 = s1 == s2;
```

there is overloading method called `isEqual()`

### Ternary operator

Expression

`<condition> ? <If_True> : <If_False>`

```c#
var total = 90;
var vipThreshold = 1000;

var title = total >= vipThreshold ? "VIP" : "Customer";
var discount = total >= vipThreshold ? 0.05m : 0.0m;
```

## 005 Array

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_005/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=7)

- Content
  - How they stored
  - Declaration & Init
  - Multi dimensional
  - Jagged array
  - Indices and ranges `c# 8`
  - Bounds checking

Array is `reference type` means that variable stored in the stack and value stored in the heap

### How they stored

Variable stored in stack and value Stored contiguous in heap memory

### Declaration

- Declaration

`<type>[] <identifier>  = new <type>[<size>]`

```c#
string[] friends = new string[5];
```

- Accessing and assigning

`<identifier>[<index>]  = <value>`

```c#
friends[0] = "Ali";
friends[1] = "Reem";
friends[2] = "Faisal";
friends[3] = "Ahmed";
friends[4] = "Abeer";
```

- Initialization

`<type>[] <identifier>  = {value}`

```c#
string[] friends = {
  "Ali",
  "Reem",
  "Faisal",
  "Ahmed",
  "Abeer",
};
```

`<type>[] <identifier>  = new <type>[<size>] {value}`

```c#
string[] friends = new string[5] {
  "Ali",
  "Reem",
  "Faisal",
  "Ahmed",
  "Abeer",
};
```

`var <identifier>  = new <type>[<size>] {value}`

```c#
var friends = new string[5] {
  "Ali",
  "Reem",
  "Faisal",
  "Ahmed",
  "Abeer",
};
```

**Explicitly Defining Data Type**

### Multi Dimensional Array

`<type>[,] <identifier>  = new <type>[<width>,<height>]`

```c#
int[,] board = new int[3, 3]
{
    { 0,0,0},
    { 0,0,0},
    { 0,0,0}
};
```

`<type>[,] <identifier>  = {value}`

```c#
int[,] board =
{
    { 0,0,0},
    { 0,0,0},
    { 0,0,0}
};
```

`var <identifier>  = new <type>[<width>,<height>]{value}`

```c#
var board = new int[3, 3]
{
    { 0,0,0},
    { 0,0,0},
    { 0,0,0}
};

```

### Jagged array (Array of Arrays)

Differ from multidimensional array as the size of inner array can be in different size `multidimensional array has fixed size`

`<type>[][] <identifier>  = new <type>[][]{value}`

```c#
int[][] jagged = new int[][]
{
    new int[]{ 0,0},
    new int[]{ 0,0,0},
    new int[]{ 0}
};
```

`var <identifier>  = new <type>[][]{value}`

```c#
var jagged = new int[][]
{
    new int[]{ 0,0},
    new int[]{ 0,0,0},
    new int[]{ 0}
};
```

### Indices and ranges `c# 8`

Return a new Array

```c#
string[] friends = {"Ali","Reem","Faisal","Ahmed","Abeer"};

```

- Not include the `end`

- `<identifier>[start..end]`
  - Skip First (start) and last (end - 1)

```c#
// Skip first 1 and last (3-1)
var slice = friends[1..3]

// Result:
// {Reem, Faisal}
```

- U can ignore `end` if u want all to end
  - `<identifier>[start..]`
  - Skip First (start)

```c#
// Skip first 1
var slice = friends[1..]

// Result:
// {Reem, Faisal, Ahmed, Abeer}
```

- U can ignore start if start from zero
  - `<identifier>[..end]`
  - Skip last (end - 1)

```c#
// Skip last (3-1)
var slice = friends[..3]

// Result:
// {Ali, Reem, Faisal}
```

- U can ignore both `start` and the `end` if u want all the list
  - `<identifier>[..]`

```c#
var slice = friends[..]

// Result:
// {Ali, Reem, Faisal, Ahmed, Abeer}
```

- Using caret `^`
  - `<identifier>[..^end]`
  - Mean count from end
  - Start from 1 not from 0

```
Normal:--- 0 ---- 1 ----- 2 ------ 3 ---- 4 ----
Array:  {"Ali","Reem","Faisal","Ahmed","Abeer"};
Caret:---- 5 ---- 4 ----- 3 ------ 2 ---- 1 ----
```

```c#
var slice = friends[..^2]

// Result:
// {Ali, Reem, Faisal}
```

### Bounds checking

- Return Out of range exception if index not exist

```c#
string[] friends = {"Ali","Reem","Faisal","Ahmed","Abeer"};
var slice = friends[5] //Throw Out of range exception
```

## 006 Expressions and Iterators

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_006/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=8)

- CONTENT

  - EXPRESSION TYPES
  - BINARY OPERATORS
  - Null (COALESCING, CONDITIONAL)
  - STATEMENT / STATEMENT BLOCKS
  - SELECTION (IF, SWITCH)
  - ITERATION (WHILE, FOR, FOREACH)
  - JUMP STATEMENTS

### EXPRESSION TYPES

- [Microsoft DOCS: Precedence and order of evaluation](https://learn.microsoft.com/en-us/cpp/c-language/precedence-and-order-of-evaluation?view=msvc-170)

- Primary Expression

  - Expression that return a value
  - Expression : anything that will fold or collapse to single thing

- Void Expression
  - Expression that return nothing

### BINARY OPERATORS

### Null (COALESCING, CONDITIONAL)

#### Null COALESCING

- `<identifier> ?? <Expr if null>`

```c#
string s = null;

// If s is null then assign "Ali" to s
s = s ?? "Ali";
```

#### CONDITIONAL Null

- `Null` mean not exist
  - The variable stored in the stack and nothing in the heap

```c#
string s = null;

var s1 = s.ToUpper(); // Will throw Null Reference Exception
```

- `<identifier>?.method`
  - If not null call method otherwise return null

```c#
string s = null;

var s1 = s?.ToUpper();

// Does the same
var s2 = s is null ? null : s.ToUpper();
```

### STATEMENT / STATEMENT BLOCKS

```c#
static void Main(string[] args)
{

  // STATEMENT
  Console.WriteLine("Statement");

  // STATEMENT BLOCKS
  {
    Console.WriteLine("Statement");
    Console.WriteLine("Statement");
    Console.WriteLine("Statement");
  }

}
```

#### Expression statement

```c#
string s = "Name";
```

1. Change state

```c#
// Change state
name = name + "A.";
```

2. Call something that change the state

```c#
// Call something that change the state
name = name.ToUpper();
```

3. assignment

```c#
// Call something that change the state
name = name.ToUpper();
```

4. Increment and Decrement

- Increment
  - Pre
    `++<Identifier>`
  - Post
    `<Identifier>++`

```c#
int friends = 150;

++friends;
Console.WriteLine(friends); // 151

// Pre
Console.WriteLine(++friends); // 152

// Post
Console.WriteLine(friends++); // 152
Console.WriteLine(friends); // 153
```

- Decrement
  - Pre
    `--<Identifier>`
  - Post
    `<Identifier>--`

```c#
int friends = 150;

--friends;
Console.WriteLine(friends); // 149

// Pre
Console.WriteLine(--friends); // 148

// Post
Console.WriteLine(friends--); // 148
Console.WriteLine(friends); // 147
```

5. Object instantiation

`<Object> <identifier> = new <Object>`

### SELECTION (IF, SWITCH)

#### If

- without curly braces if have one action

```C#
if (<condition>) <action>
else if (<condition>) <action>
else <action>
```

- with curly braces if have one action or more

```c#
if (<condition>)
{
  <action>
}
else if (<condition>)
{
  <action>
}
else
{
  <action>
}
```

- Nested if

```c#
if (<condition>)
{
  if (<condition>)
  {
    if (<condition>)
    {
      <action>
    }
  }
}
else if (<condition>)
{
  if (<condition>)
  {
    <action>
  }
}
else
{
  <action>
}
```

#### Switch

```c#
switch (switch_on)
{
    case <value>:
        <action>
        break;
    default:
        <action>
        break;
}
```

- U can use curly braces

```c#
switch (switch_on)
{
    case <value>:
        {
          <action>
          break;
        }
    default:
        {
          <action>
          break;
        }
}
```

- If there are many case that do the same thing

```c#
switch (switch_on)
{
    case <value>:
    case <value>:
    case <value>:
    case <value>:
        <action>
        break;
    default:
        <action>
        break;
}
```

- Switch on types

```c#
switch (switch_on)
{
    case <type> <identifier>:
        <action>
        break;
    case <type> <identifier>:
        <action>
        break;
    case <type> <identifier>:
        <action>
        break;
    default:
        <action>
        break;
}
```

- Predict switch

```c#
switch (switch_on)
{
    case <type> <identifier> when (<identifier> expr):
        <action>
        break;
    case <type> <identifier> when (<identifier> expr):
        <action>
        break;
}
```

```c#
int degree = 85;
switch (degree)
{
    case int i when i >= 65 && i < 75:
        Console.WriteLine("Good");
        break;
    case int i when i >= 75 && i < 85:
        Console.WriteLine("Very Good");
        break;
    case int i when i >= 85:
        Console.WriteLine("Excellent");
        break;
}
```

- Switch Expression `c# 8`

```c#
<type> <identifier> = switch_on switch
{
    <value> => <returned_value_of_type>,
    <value> => <returned_value_of_type>,
    <value> => <returned_value_of_type>,
    <value> => <returned_value_of_type>,
    _ => <returned_value_of_type> // `_` Mean anything else
};
```

```c#
int cardNo = 13;
string cardName = cardNo switch
{
    1 => "ACE",
    13 => "KING",
    12 => "QUEEN",
    10 => "JACK",
    _ => cardNo.ToString() // `_` Mean anything else
};
```

### ITERATION (WHILE, FOR, FOREACH)

#### While

- check first then decide whether to continue or break
- May never evaluated

```c#
while (<Logical_expr>)
{
  <action>
}
```

```c#
int counter = 0;
while (counter < 10)
{
  Console.Write(counter + " ");
  ++counter;
}
```

#### Do While

- Do first then check the condition whether to continue or break
- Should evaluate at least one time

```c#
do
{
  <action>
} while (<Logical_expr>)
```

```c#
int counter = 0;
do
{
  Console.Write(counter + " ");
  ++counter;
}while (counter < 10)
```

#### For Loop

```c#
for (int i = 0; i < length; i++) {
  <action>(i)
}
```

```c#
for (int i = 0; i < length; i++) {
  Console.Write(i + " ");
}
```

Fibonacci

```c#
for (int i = 0, prev = 0, current = 1; i < 12; i++)
{
    Console.Write(prev + " ");
    int newFibonacci = prev + current;
    prev = current;
    current = newFibonacci;
}

// 0 1 1 2 3 5 8 13 21 34 55 89
```

infinite loop with for

```c#
for ( ; ; ) {
  Console.Write(i + " ");
}
```

#### For Each Loop

- More readable than for but less in performance

```c#
foreach (var item in Iterable)
{
    <action>(item)
}
```

```c#
foreach (var c in "CSharp Fundamentals")
{
    Console.Write(c + " ");
}

// C S h a r p   F u n d a m e n t a l s
```

### JUMP STATEMENTS

#### break;

- End Loop cycles

#### continue;

- Skip or ignore certain cycle in loop cycles

#### goto

```c#
int i = 0;
start: // label
if(i<5)
{
    Console.Write(i + " ");
    i++;

    goto start; // goto label
}
```

#### return

## 007 Casting / Type Conversion

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_007/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=9)

- Content
  - Data types are object
  - Implicit / Explicit casting
  - Boxing / Unboxing
  - Convert class vs parse
  - Try parse
  - Bit converter and valve types

### Data types are object

`Object` is the root of everything in dotNET

- `short` is an alias for `Int16`
- `ushort` is an alias for `UInt16`
- `int` is an alias for `Int32`
- `long` is an alias for `Int64`

```c#
Int32 x = 7;
// same as
int x1 = 7;
```

### Implicit / Explicit casting

- Implicit

Implicit casting occurs when there is no risk of data loss during the conversion, and the compiler can automatically perform the conversion. This is allowed when the target data type can fully represent all possible values of the source data type. For example:

```c#
int intValue = 10;
double doubleValue = intValue; // Implicit casting from int to double
```

- Explicit

Explicit casting is required when there is a risk of data loss or when the conversion is not automatically performed by the compiler. It is necessary to inform the compiler about the conversion intention explicitly. For example:

```c#
double d = 1.0;
int i = (int)d;
```

### Boxing / Unboxing

- Boxing

Converting from `Data Type Value` to `Data Type Reference`

the conversion done Implicitly

```c#
int x = 10; // Value Type
Object obj; // Reference Type

obj = x;    // Implicit Conversion (Boxing)
```

- unBoxing

Converting from `Data Type Reference` to `Data Type Value`

the conversion done Explicitly

```c#
int x = 10; // Value Type
Object obj; // Reference Type

obj = x;    // Implicit Conversion (Boxing)

int y = (int)obj;// Must be converted Explicitly (unBoxing)
```

### Convert class vs parse

- Parse

```c#
num.Parse(); // int.Parse() , double.Parse() ....
```

```c#
string value = "150";
int i = int.Parse(value);

value = "9999999999";
int j = int.Parse(value); // Throw Overflow Exception

value = "w150";
int j = int.Parse(value); // Throw Format Exception
```

- Convert
  - Less performance than `Parse`

```c#
Convert.type()
```

```c#
string value = "150";
var i = Convert.toInt32(value);

value = "9999999999";
int j = Convert.toInt32(value); // Throw Overflow Exception

value = "w150";
int j = Convert.toInt32(value); // Throw Format Exception
```

### Try parse

```c#
num.TryParse(stringVal, out num <identifier>); // return bool
```

```c#
num <identifier>;
num.TryParse(stringVal, out <identifier>); // return bool
```

```c#
string value = "9999999999";

if (int.TryParse(value, out int k))
{
    Console.WriteLine(k);
}
```

### Bit converter and valve types

- convert primitive types to list of bytes

```c#
BitConverter.GetBytes(<primitive_type>); // return list of bytes
```

- convert to base

```c#
Convert.ToString(<Byte>, <Base>);
// <Base> 2  or 16
```

- using specifier to convert to hexadecimal

```c#
Console.Write($"{num:x}"); // num:x Convert to Hexadecimal
```

- Convert from hex to string

```c#
string[] hexVa1ues = { "49", "73", "73", "61", "6d"};

foreach (var hex in hexVa1ues)
{
  int value = convert.ToIInt32(hex, 16);

  // 01
  var stringVa1ue = Char.ConvertFromUtf32(value);
  Console.WriteLine( stringVa1ue);

  // 02
  var ch = (char)value;
  Console.WriteLine(ch);
}
```

- convert from hex to int32

using `System.Globalization.NumberStyles`

```c#
var hexVal = "6D";
var converted = Int32.Parse(hexVal, System.Globalization.NumberStyles.HexNumber);
Console.WriteLine(converted);
```

### New String Interpolation

`:x` Convert to Hexadecimal

```c#
Console.Write($"{num:x}"); // num:x Convert to Hexadecimal
```

## 008 Field & Constant

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_008/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=10)

- Content
  - INTRODUCTION
  - DEFINITION
  - CLASS VS. OBJECT
  - CLASS MODIFIERS
  - ACCESS MODIFIERS
  - FIELD CONSTANT

### INTRODUCTION

### DEFINITION

OBJECT-ORIENTED PROGRAMMING (OOP)
is a programming paradigm that allows you to package
together data states and functionality

- OOP 4 Pillars
  - Encapsulation
  - Polymorphism
  - Inheritance
  - Abstraction

### CLASS MODIFIERS

- internal (default)
- public ...

### ACCESS MODIFIERS

- public
- private
- protected

### CLASS VS. OBJECT

Class is a reference type

```c#
<ClassModifier> class <ClassName>
{
  class block
}
```

```c#
public class Employee
{

}
```

class is a blueprint or a prototype or the template we use to build our objects

Object Syntax;

- Declaration

```c#
  <Class> <ObjectName>;
```

- Assignment

```c#
  <ObjectName> = new <Class>();
```

- Initialization

```c#
  <Class> <ObjectName> = new <Class>();
```

```c#
// Declaration
Employee employee1;
// Assignment
employee01 = new Employee();

// Initialization
Employee employee2 = new Employee();
```

### Class Members

- Fields
- Constants / FIELD CONSTANT
- Properties
- Methods
- Events
- Operators
- Indexers
- Constructors
- Finalizers
- Nested Types

#### Fields

```c#
<AccessModifier> <DataType> <FieldName> = <InitialValue>;
```

- AccessModifier
  - public
  - private
  - protected

You can make initial value or just declare it

```c#
public class Employee
{
  public string FName;
  public string LName;
  public double Wage;
  public double LoggedHours;
}
```

#### Constants / FIELD CONSTANT

- Best practice put in top of the class
- You must give it a value
- Use capitalization with const

```c#
<AccessModifier> const <DataType> <FIELDNAME> = <Value>;
```

```c#
public class Employee
{
  public const double TAX = 0.03;

  public string FName;
  public string LName;
  public double Wage;
  public double LoggedHours;
}
```

- to use constant call from object
- it's not accessible from object instance

```c#
Employee emp = new Employee();

emp.TAX //wrong
Employee.TAX //right
```

## 009 Methods

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_009/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=11)

- Content
  - INSTANCE VS. STATIC MEMBER
  - METHOD SIGNATURE
  - EXPRESSION BODIED METHOD
  - METHOD OVERLOAD
  - PASS PARAMETER VALVE / REF.
  - LOCAL METHOD

### INSTANCE VS. STATIC MEMBER

- Both const and static stored in memory in place called `High Frequency Heap`
- const

  constant is a promise that can not be changed after it has been initialized

- static

  static member a shared variable that can be changed after it has been initialized

```c#
<AccessModifier> static <DataType> <FieldName> = <Value>;
```

```c#
public class Employee
{
  public static double TAX = 0.03;

  public string FName;
  public string LName;
  public double Wage;
  public double LoggedHours;
}
```

### Method Syntax(simple)

```c#
<AccessModifier> (<Data Typ> / void) MethodName (<Parameter List>)
{
  // series of statement
}
```

Example

```c#
class Demo
{
  // Also Called Callee
  public void DoSomething ()
  {
    // something
  }

  // Also is called: Callee
  // amount is called: parameter
  public void DoSomething2 (int amount)
  {
    // something
  }
}
```

```c#
Demo d = new Demo();

// Called Caller
d.DoSomething();

// Called Caller
// 5 is called: passed argument
d.DoSomething2(5);
```

### PASS PARAMETER VALVE / REF.

- pass by value means

  you are making a copy in memory of the actual parameter's value ,that is passed in

- pass by reference means

  you are passing the reference so any change happen to passed argument will be reflected to the original variable

Signature

```c#
<AccessModifier> (<Data Typ> / void) MethodName (ref <Parameter List>)
{
  // series of statement
}
```

- Both `caller` and `callee` should have `ref` keyword
- Passed argument must be initialized before passed

Example

```c#
class Demo
{
  // Also Called Callee
  public void AddToAge (ref int age)
  {
    age = age + 5;
  }
}
```

```c#
Demo d = new Demo();

int age = 15;
d.AddToAge(ref age);
Console.Write(age) // 20;

int age2;
d.AddToAge(ref age2); //wrong age2 must be initialized before passed
```

#### Using `out` Keyword

Signature

```c#
<AccessModifier> (<Data Typ> / void) MethodName (out <Parameter List>)
{
  // must initialize out params before use it

  // series of statement
}
```

- Both `caller` and `callee` should have `out` keyword
- unlike `ref` keyword Passed argument with `out` can be not initialized
  Example
- You must initialize out params in callee body before using it

```c#
class Demo
{
  // Also Called Callee
  public void AddToAge (out int age)
  {
    age = 0;          // init first
    age = age + 5;    // then use
  }
}
```

```c#
Demo d = new Demo();

int age2;
d.AddToAge(out age2);
```

### METHOD SIGNATURE

```c#
<Method Name> <Params Type> <Params Order>
```

- params names doesn't affect
- method return type doesn't affect

### METHOD OVERLOAD

Method Overloading (Common way of implementing **Polymorphism**)

```c#
{
  public void Promote(double amount)
  {
    Console.WriteLine($"You 've got a promotion of ${amount}");
  }

  public void promote(double amount, string trip)
  {
    Console.WriteLine($"You 've got a promotion of ${amount} and a trip {trip}");
  }

  public void promote(double amount, string trip, string hotel)
  {
    Console.WriteLine($"You 've got a promotion of ${amount} and a trip {trip} with {hotel}");
  }
}
```

### EXPRESSION BODIED METHOD

Signature

```c#
<AccessModifier> (<Data Typ> / void) MethodName (<Parameter List>) => /*EXPRESSION*/;
```

when your method body have single expression

### LOCAL METHOD

method in method

```c#
<AccessModifier> (<Data Typ> / void) MethodName (<Parameter List>)
{
  // Caller
  LocalMethod();

  // Callee
  (<Data Typ> / void) LocalMethod (<Parameter List>)
  {

  }
}
```

### STATIC METHOD

```c#
class ClassName
{
  <AccessModifier> static (<Data Typ> / void) MethodName (<Parameter List>)
  {
    // Expr
  }
}
```

Call with class

```c#
ClassName.MethodName();
```

- static only deals with static

## 010 Constructor

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_010/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=12)

- Content

  - IMPLICIT CONSTRUCTOR
  - OVERLOADED CONSTRUCTOR
  - THIS KEYWORD
  - NON PUBLIC CONSTRUCTOR
  - OBJECT INITIALIZER
  - READONLY FIELD

### Naming Convention

- Private Field:
  - lowerCase OR prefix with `_`
  - use only one of them in the entire project

```c#
class ClassName
{
  private int privateFiledInClass;
  private int _privateFiledInClass;
}
```

- Public Field:
  - CapitalCase

```c#
class ClassName
{
  public int PublicFiledInClass;
}
```

- Const Field:
  - Uppercase

```c#
class ClassName
{
  public int STATICFILEDINCLASS;
}
```

### Constructor syntax

```c#
class <ClassName>
{
  <AccessModifier> <ClassName> (<Parameter List>)
  {
    // Expr
  }
}
```

```c#
class Date
{
    public int Day;
    public int Month;
    public int Year;

    public Date (int day,int month,int year)
    {
      Day = day;
      Month = month;
      Year = year;
    }
}
```

### IMPLICIT CONSTRUCTOR

Every class in `.NET` by default have a public constructor that take `0 argument`

### THIS KEYWORD

- Use to eliminate ambagious between class field and other variables

```c#
class Date
{
    private int day;
    private int month;
    private int year;

    public Date (int day,int month,int year)
    {
      this.day = day;
      this.month = month;
      this.year = year;
    }
}
```

### READONLY FIELD

- Field that cannot be changed
- `readonly` Fields can change inside constructor

```c#
class Date
{
    private readonly int day = 01;
    private readonly int month = 01;
    private readonly int year = 01;

    public Date (int day,int month,int year)
    {
      this.day = day;
      this.month = month;
      this.year = year;
    }
}
```

### OVERLOADED CONSTRUCTOR

- You can create overloading constructor
- when params

  - list count are different
  - types are different
  - params order are different

- U can use logic inside other constructor using

```c#
class <ClassName>
{
  <AccessModifier> <ClassName> (<Parameter List>)
  {
    // Expr
  }

  <AccessModifier> <ClassName> (<Parameter List>) : this(<Parameter List of required constructor>)
  {
  }
}
```

Example

```c#
class Date
{
    private int day = 01;
    private int month = 01;
    private int year = 01;

    public Date (int day,int month,int year)
    {
      // validation steps
      this.day = day;
      this.month = month;
      this.year = year;
    }

    public Date (int month,int year) : this(01, month, year)
    {
    }

    public Date (int year) : this(01, year)
    {
    }
}
```

### OBJECT INITIALIZER

```c#
public class Employee
{
    public int Id;
    public string FName;
    public string LName;

    public Employee(int id)
    {
      Id = id;
    }
}
```

- First Way

```c#
Employee employee = new Employee();
employee.Id = 1;
employee.FName = "Ali";
employee.LName = "Ahmed";
```

- Second Way
  - popular

```c#
Employee employee = new Employee
{
    Id = 1,
    FName = "Ali",
    LName = "Ahmed",
};

// or
Employee employee = new Employee()
{
    Id = 1,
    FName = "Ali",
    LName = "Ahmed",
};
```

If constructor take arguments

```c#
Employee employee2 = new Employee(1)
{
    FName = "Ali",
    LName = "Ahmed",
};
```

### NON PUBLIC CONSTRUCTOR

Private constructor u can create class only inside class and use for example static method to create this class

```c#
public class Employee
{
    private int id;
    private string fName;
    private string lName;

    private Employee()
    {
    }

    private Employee(int id,string fName,string lName)
    {
      this.id = id;
      this.fName = fName;
      this.lName = lName;
    }

    public static Employee create(int id,string fName,string lName){
      return Employee(id,fName,lName);
    }
}
```

```c#
Employee emp = Employee.create(1,"Ali","Ahmed");
```

## 011 Properties

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_011/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=13)

- Content

  - PROPERTY AND ENCAPSULATION
  - PROPERTY
  - GET AND SET Accessor
  - PROPERTY/BACKING FIELD
  - PROPERTY AND ACCESSIBILITY
  - AUTOMATIC PROPERTY
  - PROPERTY INTERNALLY

- public way to access private field

### PROPERTY AND ENCAPSULATION

- it promote encapsulation

### PROPERTY

- `BACKING FIELD`

  - the private field we deal with

- `get` Accessor

  - return the field or value you want to return

- set Accessor

  - to set field with a reserved keyword called `value`
  - `value` keyword have the value which client assign to property

- Client
  - The code that use our code

```c#
class Dollar
{
    // BACKING FIELD
    private decimal _amount;

    public decimal Amount
    {
        get
        {
          return _amount;
        }
        set
        {
          _amount = value;
        }
    }
}
```

### GET AND SET Accessor

u can use get only

```c#
class Dollar
{
    // BACKING FIELD
    private decimal _amount;

    public decimal Amount
    {
        get
        {
          return _amount;
        }
    }
}
```

u can use set only

```c#
class Dollar
{
    // BACKING FIELD
    private decimal _amount;

    public decimal Amount
    {
        set
        {
          _amount = value;
        }
    }
}
```

u can use property without backing field

```c#
class Dollar
{
    public decimal Amount
    {
        get;
        set;
    };
}
```

u can assign initial value to property in initialization

```c#
class Dollar
{
    public decimal Amount
    {
        get;
        set;
    } = 10.0m;
}
```

### PROPERTY AND ACCESSIBILITY

u can use accesses modifiers like private

```c#
class Dollar
{
    // BACKING FIELD
    private decimal _amount;

    public decimal Amount
    {
        get
        {
          return _amount;
        }
        private set
        {
          _amount = value;
        }
    }
}
```

### PROPERTY INTERNALLY

.NET CLR convert property to get and set method `Sugar Syntax`

In C#, class properties are actually implemented as special methods known as "accessors."

Properties provide a way to encapsulate data within a class and define how that data is read from and written to.

There are two types of accessors for properties: the get accessor (getter) and the set accessor (setter).

### AUTOMATIC PROPERTY

If u have a property that just get and set without any type of validation or any background process

like: in the following code Amount property just `get` and `set` `_amount`

```c#
class Dollar
{
    // BACKING FIELD
    private decimal _amount;

    public decimal Amount
    {
        get
        {
          return _amount;
        }
        set
        {
          _amount = value;
        }
    }
}
```

then we can use automatic property

```c#
class Dollar
{
    public decimal Amount  { get; set;}
}
```

#### Why not to use field? `ChatGPT`

Using properties instead of fields in C# classes offers several advantages in terms of encapsulation, maintainability, and flexibility. While it might seem tempting to use fields directly, properties provide a level of abstraction that promotes better coding practices. Here are some reasons why you should prefer properties over fields:

- Encapsulation: Properties allow you to control the access to the underlying data. You can enforce validation rules, perform additional logic (e.g., logging, lazy initialization), or restrict access to certain parts of the class. Fields, on the other hand, provide no encapsulation; they are directly accessible from anywhere in the code, making it harder to maintain a consistent and valid state.

- Read-Only and Write-Only Properties: With properties, you can define read-only and write-only properties, where you can expose a value for reading but prevent external code from modifying it directly. This enables you to create immutable objects or control specific parts of your class's state.

- Versioning and Compatibility: When you use fields directly, changing the implementation details of the class (e.g., renaming the field, changing the data type) might require changes to the code that uses that class. However, with properties, you have more control over the internal representation, and you can change the implementation without breaking the external API of the class.

- Data Validation: Properties provide a convenient place to validate data before setting it or returning it. You can add checks to ensure the data meets certain criteria, thus preventing invalid or unexpected values from being stored.

- Debugging and Logging: By using properties, you can add debugging or logging statements inside the getter and setter methods to monitor data changes, perform debugging tasks, or track usage.

- Data Binding and Serialization: Properties are crucial when working with data binding frameworks or serialization libraries since they allow these frameworks to access the data through getter and setter methods instead of directly accessing the fields.

- Lazy Loading: Properties allow you to implement lazy loading, where the data is loaded only when it's accessed for the first time. This can be helpful when dealing with resource-intensive data or expensive calculations.

- Consistency: Consistently using properties throughout your codebase helps maintain a clear and standard approach to data access and manipulation, improving code readability and maintainability.

While using fields directly might be acceptable for very simple classes or data structures, it is generally considered a better practice to use properties to gain the benefits of encapsulation and flexibility that they offer.

## 012 Indexers

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_012/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=14)

- Content
  - WHAT IS INDEXERS
  - SCENARIOS WHEN TO USE
  - INDEXER SYNTAX
  - SINGLE DIMENSIONAL MAP
  - MULTI-DIMENSIONAL MAPS
  - SUDOKU EXAMPLE

### WHAT IS INDEXERS

`ChatGPT`

In C#, an indexer is a special property that allows you to access elements or values in an object as if the object were an array. It provides a way to treat an object as a collection and access its elements using index syntax (square brackets []). An indexer is a member of a class or struct and is defined similar to a property but with an additional parameter for the index.

To define an indexer, you use the this keyword followed by the index parameter type and name inside square brackets. Here's the basic syntax:

### SCENARIOS WHEN TO USE

`ChatGPT`

Indexers are commonly used in classes that encapsulate collections or provide indexed access to their internal data. They allow you to create more intuitive and convenient APIs for working with your custom collections or data structures.

Note: Indexers can be defined with multiple parameters if your collection requires more than one index to access its elements. However, it is essential to design your indexer carefully to ensure it behaves consistently and adheres to the principles of a well-behaved collection.

### INDEXER SYNTAX

Indexer can be

- readonly use `get` only

```c#
class <ClassName>
{
  // indexer
  <AccessModifier> <unit of dataType of collection> this[int index]
  {
    get
    {
      if(/*validation*/) return -1;

      return <collection>[index];
    }
    set
    {
      if(/*validation*/) return; // don't set

      <collection>[index] = value;
    }
  }

  <AccessModifier> <ClassName> (<Parameter List>)
  {
    // Expr
  }

}
```

Example

```c#
public class Ip
{

  private int[] segments = new int[4];

  // indexer
  public int this[int index]
  {
    get
    {
      return segments[index];
    }
    set
    {
      segments[index] = value;
    }
  }

  public Ip (int sge1,int sge2,int sge3,int sge4)
  {
    segments[0] = sge1;
    segments[1] = sge2;
    segments[2] = sge3;
    segments[3] = sge4;
  }
}
```

### SINGLE DIMENSIONAL MAP

```c#
public class SingleDimensionalMap
{
    private int[] data; // The underlying data storage

    public SingleDimensionalMap(int size)
    {
        data = new int[size];
    }

    // Indexer for single-dimensional map
    public int this[int index]
    {
        get
        {
            return data[index];
        }
        set
        {
            data[index] = value;
        }
    }
}
```

### MULTI-DIMENSIONAL MAPS

```c#
public class MultiDimensionalMap
{
    private int[,] data; // The underlying data storage

    public MultiDimensionalMap(int rows, int columns)
    {
        data = new int[rows, columns];
    }

    // Indexer for multi-dimensional map
    public int this[int row, int column]
    {
        get
        {
            return data[row, column];
        }
        set
        {
            data[row, column] = value;
        }
    }
}
```

### SUDOKU EXAMPLE

```c#
public class Sudoku
{
    private int[,] board;

    public Sudoku(int[,] board)
    {
        this.board = board;
    }

    public int this[int row, int column]
    {
        get
        {
            return board[row, column];
        }
        set
        {
            board[row, column] = value;
        }
    }
}
```

## 013 Delegate

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_013/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=15)

- Content
  - WHAT IS DELEGATE
  - SCENARIOS WHEN TO USE
  - WHEN TO APPLY DELEGATE
  - ANTONYMOUS DELEGATE
  - LAMBDA EXPRESSION
  - MULTICAST DELEGATE

### WHAT IS DELEGATE

Object that points to `method` that changed at runtime

- Reference type
- Can be inside or outside the class

- why not a property?

As delegate have a logical process

### SCENARIOS WHEN TO USE && WHEN TO APPLY DELEGATE

`ChatGPT`

In C#, delegates provide a powerful way to decouple method calls from their implementation, enabling more flexible and extensible code. Here are some specific scenarios where you can use delegates in C#:

- Event Handling: Delegates are commonly used in event-driven programming to handle events. They allow you to define event signatures and register event handler methods that will be invoked when an event is raised.

- Callbacks: When you need to define a method that performs a particular task and allows the caller to specify additional behavior, you can use delegates as callback parameters. The caller can pass a method (delegate) that will be invoked by the original method to execute the additional behavior.

- LINQ (Language-Integrated Query): LINQ extensively uses delegates to enable querying collections and other data sources using a consistent and expressive syntax. Delegates are used to represent predicates, projections, and other operations in LINQ queries.

- Asynchronous Programming: Delegates can be used to implement asynchronous programming patterns like the Asynchronous Programming Model (APM) and the Event-based Asynchronous Pattern (EAP). In these patterns, delegates are used to represent asynchronous operations and provide methods for initiating and handling the completion of those operations.

- Custom Sorting: When sorting elements in a custom way (e.g., sorting custom objects based on specific properties), you can use delegates to pass custom comparison logic to the sorting algorithm.

- Dependency Injection: Delegates can be used to implement dependency injection, where a method or constructor takes a delegate parameter representing a service or dependency. The caller can provide the appropriate implementation of the delegate, allowing the method to work with different services or dependencies.

- Strategy Pattern: Delegates can be used to implement the Strategy design pattern, where you can define different algorithms (strategies) as separate methods and pass them as delegates to a context object, which can then switch between different strategies at runtime.

- Dynamic Behavior: Delegates allow you to dynamically change the behavior of methods at runtime, which can be useful in scenarios where you need to modify functionality based on user input or other dynamic factors.

- Parallel Processing: Delegates can be utilized in parallel processing scenarios, such as with the Parallel.ForEach method, to specify the action that needs to be performed in parallel on each item in a collection.

Overall, delegates are a fundamental tool for creating more modular, maintainable, and reusable code. They offer great flexibility in designing code that can adapt to different situations and allows for separation of concerns, improving the overall design of your application.

### Syntax

same as method but

- Have `delegate` keyword in its signature
- Doesn't have a body

```c#
<AccessModifier> delegate (<DataType> Result Delegate return) DelegateName ((<ParameterList> to process));
```

Example

```c#
public delegate bool EligibleSales (Employee emp);
```

```c#
public class Report
{
    public delegate bool EligibleSales(Employee emp);

    public void Process(Employee[] emps, string title, EligibleSales isEligible)
    {
        Console.WriteLine(title);
        Console.WriteLine("=======================");

        foreach (var e in emps)
        {
            if (isEligible(e))
            {
                Console.WriteLine(e.ToString();
            }
        }
    }
}
```

How to use?

```c#
{
  Employee[] emps = {/*dummy*/};

  Report report = new Report();

  report.Process(emps,"Emps EligiblePlus60K",EligiblePlus60K);
  report.Process(emps,"Emps EligibleRange60KTo30K",EligibleRange60KTo30K);
  report.Process(emps,"Emps EligibleLess30K",EligibleLess30K);
}

bool EligiblePlus60K(Employee emp) => emp.TotalSales > 60_000m;
bool EligibleRange60KTo30K(Employee emp) =>  emp.TotalSales > 30_000m && emp.TotalSales <= 60_000m;
bool EligibleLess30K(Employee emp) =>  emp.TotalSales < 30_000m;
```

### ANTONYMOUS DELEGATE `After .NET framework 2`

```c#
{
  Employee[] emps = {/*dummy*/};

  Report report = new Report();

  report.Process(emps,"Emps EligiblePlus60K", delegate (Employee emp) {return emp.TotalSales > 60_000m;});
  report.Process(emps,"Emps EligibleRange60KTo30K", delegate (Employee emp) {return emp.TotalSales > 30_000m && emp.TotalSales <= 60_000m;});
  report.Process(emps,"Emps EligibleLess30K", delegate (Employee emp) {return emp.TotalSales < 30_000m;});
}
```

### LAMBDA EXPRESSION `After .NET 3`

After .NET 3 we have body expression

```c#
{
  Employee[] emps = {/*dummy*/};

  Report report = new Report();

  report.Process(emps,"Emps EligiblePlus60K", (Employee emp)=> emp.TotalSales > 60_000m;);
  report.Process(emps,"Emps EligibleRange60KTo30K", (Employee emp)=> emp.TotalSales > 30_000m && emp.TotalSales <= 60_000m);
  report.Process(emps,"Emps EligibleLess30K", (Employee emp)=> emp.TotalSales < 30_000m);
}
```

- As delegate know that it will receive Employee you could remove it
- You could also remove brackets

```c#
{
  Employee[] emps = {/*dummy*/};

  Report report = new Report();

  report.Process(emps,"Emps EligiblePlus60K", emp => emp.TotalSales > 60_000m;);
  report.Process(emps,"Emps EligibleRange60KTo30K", emp => emp.TotalSales > 30_000m && emp.TotalSales <= 60_000m);
  report.Process(emps,"Emps EligibleLess30K",emp => emp.TotalSales < 30_000m);
}
```

### MULTICAST DELEGATE

Delegate that point more than one method

- Means you can subscribe to method

  - that has delegate signature
  - same params list

- Subscribe / Register use `<delegate> += <method>`
- Unsubscribe / Unregister use `<delegate> -= <method>`

```c#
public class RectHelper
{
    public void getArea(double width,double height)
    {
        var result = width * height;
        Console.WriteLine( $"Rect Area: {width} * {height} = {result}");
    }

    public void getPerimeter(double width,double height)
    {
        var result = 2 * (width + height);
        Console.WriteLine( $"Rect Area: 2 * ({width} + {height}) = {result}");
    }
}
```

```c#
public delegate void RectDelegate(double width, double height);

{
  var helper = new RectHelper();

  RectDelegate rect;
  rect = helper.getArea; // Assign
  rect += helper.getPerimeter; // Subscribe

  rect(10,10); // will do both getArea and getPerimeter

  rect -= helper.getPerimeter; // Unsubscribe

  rect(10,10); // will do getArea only
}
```

## 014 Events

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_014/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=16)

- Content
  - WHAT IS EVENT
  - EVENT AND DELEGATE
  - EVENT PUBLISHER
  - SUBSCRIBE VS UNSUBSCRIBE
  - EVENT HANDLER
  - LAMBDA EXPRESSION HANDLER

### WHAT IS EVENT

Events enable a class or object to notify other classes or objects when something of interest occurs

- When use event use must link it with delegate

- Event name always in passive `changed | occurred | ...`

### EVENT PUBLISHER

The class the have event inside it called publisher

- Stock Class called publisher

The class that use event `subscribed | registered` called Subscriber

- for example Program class called Subscriber

### EVENT AND DELEGATE

```c#
<AccessModifier> event <Delegate> EventName;
```

Example

```c#
public event StockPriceChangedHandler onPriceChanged;
```

Full Example

```c#
public delegate void StockPriceChangedHandler(Stock stock, decimal price);

// Publisher
public class Stock
{
    public event StockPriceChangedHandler OnStockPriceChanged;

    private string name;
    private decimal price;

    public string Name => name;
    public decimal Price
    {
        get { return this.price; }
        set { this.price = value; }
    }

    public Stock(string name)
    {
        this.name = name;
    }

    public void changeStockPriceBy(decimal percent)
    {
        decimal oldPrice = this.price;
        this.price += Math.Round(price * percent , 2);

        // First check that event have subscribers
        if (OnStockPriceChanged != null)
        {
            OnStockPriceChanged(this, oldPrice); // Fire the event
        }
    }
}
```

```c#
// Subscriber
class Program
{
  public static void Main(string[] args)
  {
    Stock stock = new Stock("Amazon");
    stock.Price = 100;

    // Subscribe to event
    stock.OnStockPriceChanged += Stock_OnPriceChanged;

    stock.changeStockPriceBy(0.05m);
    stock.changeStockPriceBy(-0.02m);
    stock.changeStockPriceBy(0.00m);

    // Unsubscribe event
    stock.OnStockPriceChanged -= Stock_OnPriceChanged;

    stock.changeStockPriceBy(0.05m);  // Nothing will be print to console
    stock.changeStockPriceBy(-0.02m); // Nothing will be print to console
    stock.changeStockPriceBy(0.00m);  // Nothing will be print to console
  }

  // Method will fired when event fired
  public static void StockPriceChangedHandler(Stock stock, decimal price)
  {
    if(stock.Price > oldPrice)
    {
      Console.ForegroundColor = ConsoleColor.Green;
    }
    else if(stock.Price > oldPrice)
    {
      Console.ForegroundColor = ConsoleColor.Red;
    }
    else
    {
      Console.ForegroundColor = ConsoleColor.Grey;
    }

    Console.WriteLine($"{stock.Name}: {stock.Price}");
  }
}
```

### SUBSCRIBE VS UNSUBSCRIBE

- Subscribe

```c#
    // Subscribe to event
    stock.OnStockPriceChanged += Stock_OnPriceChanged;

    stock.changeStockPriceBy(0.05m);
    stock.changeStockPriceBy(-0.02m);
    stock.changeStockPriceBy(0.00m);
```

- Unsubscribe

```c#
    // Unsubscribe event
    stock.OnStockPriceChanged -= Stock_OnPriceChanged;

    stock.changeStockPriceBy(0.05m);  // Nothing will be print to console
    stock.changeStockPriceBy(-0.02m); // Nothing will be print to console
    stock.changeStockPriceBy(0.00m);  // Nothing will be print to console
```

### LAMBDA EXPRESSION HANDLER

```c#
// Subscriber
class Program
{
  public static void Main(string[] args)
  {
    Stock stock = new Stock("Amazon");
    stock.Price = 100;

    // Subscribe to event
    stock.OnStockPriceChanged += (Stock stock, decimal price) =>
    {
      if(stock.Price > oldPrice)
      {
        Console.ForegroundColor = ConsoleColor.Green;
      }
      else if(stock.Price > oldPrice)
      {
        Console.ForegroundColor = ConsoleColor.Red;
      }
      else
      {
        Console.ForegroundColor = ConsoleColor.Grey;
      }

      Console.WriteLine($"{stock.Name}: {stock.Price}");
    };

    stock.changeStockPriceBy(0.05m);
    stock.changeStockPriceBy(-0.02m);
    stock.changeStockPriceBy(0.00m);
  }
}
```

## 015 Operator Overloading

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_015/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=17)

- Content

  - DEFINITION
  - UNARY VS. BINARY OPERATORS
  - SUPPORTED OPERATORS
  - OVERLOADED OPERATOR SYNTAX
  - MUST OVERLOADED IN PAIR

- Important in Domain-Driven-Design World

### DEFINITION

User defined type that can overload predefined operators

```c#
public class Money
{
    private decimal amount;

    public decimal Amount => amount;

    public Money(decimal amount)
    {
        this.amount = amount;
    }
}

Money m1 = new Money(20);
Money m2 = new Money(40);

Money m3 = m1 + m2; // Error
```

### UNARY VS. BINARY OPERATORS

- BINARY

  Take/Deal with two variable

  Example

  `+` `-` `*` `\` `>` `<`

- UNARY

  Take/Deal with two variable

  `!`

### SUPPORTED OPERATORS

- Arithmetic Operators

  `+` `-` `*` `\` ...etc

- Comparison Operators

  `>` `<` `<=` `>=` ..etc

- Boolean Operators

  `&` `&&` `|` `||` `!`

### OVERLOADED OPERATOR SYNTAX

```c#
{
  <AccessModifier> static (<DataTyp>) operator <Operator>(<ParamsList for Operator>)
  {
    // series of statement
    return (<DataTyp>);
  }
}
```

- `<ParamsList for Operator>` Depend on type of operator if
  - Unary it will be one param
  - Binary it will be two params

Example

```c#
{
  public static Money operator +(Money m1, Money m2)
  {
    return new Money(m1.Amount + m2.Amount);
  }
}
```

Full Example

```c#
public class Money
{
    private decimal amount;

    public decimal Amount => amount;

    public Money(decimal amount)
    {
        this.amount = amount;
    }

    public static Money operator +(Money m1, Money m2)
    {
        var result = m1.Amount + m2.Amount;
        return new Money(result);
    }


    public static Money operator -(Money m1, Money m2)
    {
        var result = m1.Amount - m2.Amount;
        return new Money(result);
    }

}

Money m1 = new Money(20);
Money m2 = new Money(40);

Money m3 = m1 + m2;
Money m4 = m1 - m2;
```

### MUST OVERLOADED IN PAIR

Comparison Operators must overloaded in pair

```c#
    public static bool operator >(Money m1, Money m2)
    {
        return m1.Amount > m2.Amount;
    }
```

```c#
Money m1 = new Money(10);
Money m2 = new Money(20);

if(m1 > m2) // Here check if m1 > m2 |or| m2 < m1
{
  /*Logic*/
}
```

```c#
    public static bool operator >(Money m1, Money m2)
    {
        return m1.Amount > m2.Amount;
    }

    public static bool operator <(Money m1, Money m2)
    {
        return m1.Amount < m2.Amount;
    }
```

```c#
public class Money
{
    private decimal amount;

    public decimal Amount => amount;

    public Money(decimal amount)
    {
        this.amount = amount;
    }

    public static Money operator +(Money m1, Money m2)
    {
        var result = m1.Amount + m2.Amount;
        return new Money(result);
    }

    public static Money operator -(Money m1, Money m2)
    {
        var result = m1.Amount - m2.Amount;
        return new Money(result);
    }

    public static bool operator >(Money m1, Money m2)
    {
        return m1.Amount > m2.Amount;
    }

    public static bool operator <(Money m1, Money m2)
    {
        return m1.Amount < m2.Amount;
    }

    public static bool operator >=(Money m1, Money m2)
    {
        return m1.Amount >= m2.Amount;
    }

    public static bool operator <=(Money m1, Money m2)
    {
        return m1.Amount <= m2.Amount;
    }

    public static bool operator ==(Money m1, Money m2)
    {
        return m1.Amount == m2.Amount;
    }

    public static bool operator !=(Money m1, Money m2)
    {
        return m1.Amount != m2.Amount;
    }

    public static Money operator ++(Money m)
    {
        var result = m.Amount;
        return new Money(++result);
    }

    public static Money operator --(Money m)
    {
        var result = m.Amount;
        return new Money(--result);
    }
}
```

## 016 Finalizers / Destructors

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_016/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=18)

- Content
  - DEFINITION
  - WHY FINALIZERS
  - GARBAGE COLLECTOR
  - IMPLICIT VS EXPLICIT
  - GC.COLLECT()

### DEFINITION

A special method inside our class used to destroy instance of that class

- Used when our instance `destroyed` / `disposed` / `died`

- `~` Tilde

```c#
  ~<ClassName>()
  {
      // Action to do when class destroyed
  }
```

```c#
public class Person
{
    public string Name {set; get;};

    public Person(string Name)
    {
        Console.WriteLine($"Person Named: {Name} has been created");
        this.Name = name;
    }

    ~Person()
    {
        Console.WriteLine($"Person Named: {Name} has been Destroyed");
    }
}
```

### Note

- Object flagged to be destroyed when end of its scope reached
- Garbage collector destroy objects that is flagged to be destroyed

`ChatGPT`

The two statements you provided are not entirely accurate.

In summary, C# uses a garbage collector to manage memory and automatically clean up objects that are no longer in use. Objects are not flagged for destruction when their scope ends; rather, the garbage collector decides when to reclaim memory based on the reachability of objects. This automatic memory management system in C# is one of the key features that make the language memory-safe and developer-friendly.

### WHY FINALIZERS

### GARBAGE COLLECTOR

Automatic Memory Management

### IMPLICIT VS EXPLICIT

OBJECT WHEN GET DISPOSED?

- End of program execution `IMPLICIT`
- Memory full `IMPLICIT`
- Call `GC.Collect();` `EXPLICIT`

### GC.COLLECT()

Explicit way to collect garbage from the app

```c#
GC.Collect();
```

- We have method called `GC.GetTotalMemory(false);` that get memory used by our app

  - `false` to tell GC not to collect app garbage
  - size return in bytes

```c#
GC.GetTotalMemory(false);
```

### New String Interpolation

- `:N0`

  - Convert number from 9999999 => 9,999,999

- `:N`

  - Convert number from 9999999 => 9,999,999.0

### Note

- We haven't finished yet

- We will take how to implement `IDisposable` to our class in `Inheritance` Lesson

- How to use `using` statement that make automatic dispose to class if it applies `IDisposable`

## 017 Nested Types

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_017/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=19)

- Content

  - DEFINITION
  - WHY NESTED TYPES
  - PRIVATE/PUBLIC/INTERNAL
  - COMPOSITE OBJECTS
  - INITIALIZE NESTED OBJECTS
  - CHECKLIST

### DEFINITION

type defined within a class

### WHY NESTED TYPES

### PRIVATE/PUBLIC/INTERNAL

#### INTERNAL

`internal` member is public within the assembly / `project`.

#### PUBLIC

`public` member is public within the entire solution.

#### PRIVATE

You can't define a private class in the namespace directly

If you have `ClassB` that is only used by `ClassA` and no one else used it or you want the client not to have an access to `ClassB` You can put `ClassB` inside `ClassA`

```c#
public class ClassA
{

    private int a;

    class ClassB
    {
        public void BMethod()
        {
            ClassA aClass = new ClassA();
            aClass.a; // have access to private member of A
        }
    }

    public void ClassAMethod()
    {
        ClassB bClass = new ClassB();
    }
}
```

- It does not pollute the global scope | Client only see classes that he can use

- THE METHODS OF `ClassB` IMPLICITLY HAVE ACCESS TO PRIVATE MEMBERS of `ClassA`
- `ClassA` is the container of `ClassB`

`ChatGPT`

In C#, you can indeed have a private class. A private class is a class that is only accessible within the containing class or struct. This means that the private class cannot be accessed or used from outside the containing class, including other classes in the same namespace.

```c#
public class OuterClass
{
    // Private nested class
    private class InnerClass
    {
        // Private class members
        private int privateField;
        private void PrivateMethod()
        {
            // Some implementation...
        }
    }

    // Outer class members
    private int outerField;

    public void OuterMethod()
    {
        // Create an instance of the private class
        InnerClass inner = new InnerClass();
        // Access private members of the private class
        inner.privateField = 10;
        inner.PrivateMethod();
    }
}
```

The primary use case for private classes is encapsulation and organization of code. By making a class private, you are restricting its visibility and usage to only the containing class. This helps to hide implementation details and keep the codebase clean and maintainable.

Private classes are often used in scenarios where you have a small utility class or a helper class that is tightly related to the containing class and doesn't need to be exposed to other parts of the application.

Another common use case is when you need to implement a design pattern like the Factory Method or Abstract Factory pattern. In these cases, you might have nested private classes to encapsulate the creation of specific objects or provide different variations of a product.

Overall, using private classes helps to minimize the risk of accidental misuse and improves the clarity and maintainability of your code. By using access modifiers like private, public, protected, etc., you can control the visibility and accessibility of classes and members, allowing you to design a well-organized and secure code structure.

### COMPOSITE OBJECTS && INITIALIZE NESTED OBJECTS

COMPOSITION IS TYPE OF RELATIONSHIP BETWEEN CLASSES

```c#
    class Employee
    {
        public int Id { get; set; }
        public string Name { get; set; }

        public Insurance insurance { get; set; } // Composite
    }

    class Insurance
    {
        public int PolicyId { get; set; }
        public string CompanyName { get; set; }
    }
```

If `Employee` is the only class that use `Insurance` when can but `Insurance` inside `Employee`

```c#
    class Employee
    {
        public int Id { get; set; }
        public string Name { get; set; }

        public Insurance insurance { get; set; }

        public Employee()
        {
            // INITIALIZE NESTED OBJECTS
            insurance = new Insurance() { CompanyName = "N/A", PolicyId = -1 };
        }

        public class Insurance
        {
            public int PolicyId { get; set; }
            public string CompanyName { get; set; }
        }
    }

```

Now we can't make `insurance` member inside `Employee` public unless we make `Insurance` Class public

but this doesn't mean that `Insurance` Class become accessible to the client

### CHECKLIST

- Class Members
  1. Fields
  2. Constants
  3. properties
  4. Methods
  5. Events
  6. Operators
  7. Indexers
  8. Constructors
  9. Finalizers
  10. Nested Types

## 018 TROUBLESHOOTING / DEBUGGING

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_018/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=20)

- CONTENT
  - TYPE OF ERRORS
  - SYNTAX ERRORS
  - RUNTIME ERRORS
  - LOGICAL ERRORS
  - TRY CATCH FINALLY
  - DEBUGGING

### TYPE OF ERRORS

- syntax errors
- runtime errors
- logical errors

Every error have a unique code like `CS1002` , `CS0103`

### SYNTAX ERRORS

Easiest Error To Solve

```C#
  static void Main              // Syntax Error
  (                             // Syntax Error
      int x == 10;              // Syntax Error
      While(x >= 0)             // Syntax Error
      {
          Console.WriteLine(x)  // Syntax Error
      ]                         // Syntax Error
      Console..ReadKey();       // Syntax Error
  };                            // Syntax Error
```

```C#
  static void Main(string[] args)
  {
      int x = 10;
      while(x >= 0)
      {
          Console.WriteLine(x);
      }
      Console.ReadKey();
  }
```

- We can handle it using IDE errors list

### RUNTIME ERRORS

Improper user inputs, Improper design logic or system errors

- We can handle it using `try/catch`

### TRY CATCH FINALLY

- `Exception:`

  Is an event, which occurs during the execution of a program, that disrupts the normal flow of the program's instructions

- Syntax

```c#
  try
  {
      /*Code that may have exception*/
  }
  catch(Exception ex)
  {
      // Optional
      /*Handle incoming Exception*/
      // ex.Message
  }
  finally
  {
      // Optional
      /*After Code End*/
      // CleanUp
  }
```

- Process `try` block if exception happen go to `catch` block if not or if try done go to `finally` block
- Both of `catch` and `finally` Block are optional but one of them must be exist

### LOGICAL ERRORS

Errors occur when the program is written fine but it does not produce desired result

- Handle with tracing

### DEBUGGING

#### Break Point

- **STEP OVER** `F10`

  Advances the debugger without stepping into functions

- **STEP INTO** `F11`

  Advances the app execution one statement at a time

- **STEP OUT** `SHIFT + F11`

  Advance the debugger all the way through the current function

- Add Watch `VS IDE`

  Add statement to watch when process

  Modify statement without changing source code and show its value after change

#### Note

After stepping, Debugger will allow you to hover over a variable and it will display it's current value

## 019 Struct

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_019/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=21)

- Content

  - WHAT IS STRUCT
  - WHY STRUCT
  - REFERENCE VS. VALVE
  - CLASS OR STRUCT
  - READONLY STRUCT
  - DATETIME CLASS

### CLASS OR STRUCT

<div align= "center">

| All | Sub |                            | Class           | Struct           |
| --- | --- | -------------------------- | --------------- | ---------------- |
| 01  | 01  | User Defined Type          | ✔               | ✔                |
| 02  | 02  | Start With                 | `class` keyword | `struct` Keyword |
|     |     |                            |                 |                  |
| <<  | <<  | Class Members Comparison   | <<<<<<<<<       | <<<<<<<<<        |
|     |     |                            |                 |                  |
| 03  | 01  | Constructor                | ✔               | ✔ Restrictions   |
|     | ►   | Param less Constructor     | ✔               | ❌               |
| 04  | 02  | Fields                     | ✔               | ✔ Restrictions   |
|     | ►   | Fields Initializer         | ✔               | ❌               |
| 05  | 03  | Properties                 | ✔               | ✔                |
| 06  | 04  | Methods                    | ✔               | ✔                |
| 07  | 05  | Indexers                   | ✔               | ✔                |
| 08  | 06  | Events                     | ✔               | ✔                |
| 09  | 07  | Operator Overloading       | ✔               | ✔                |
| 10  | 08  | Finalizers / Deconstructs  | ✔               | ❌               |
| 11  | 09  | Nested Types               | ✔               | ✔                |
| 12  | 10  | Constants                  | ✔               | ✔                |
|     |     |                            |                 |                  |
| 13  | 01  | Inheritance                | ✔               | ❌               |
| 14  | 02  | Recommended For Large Data | ✔               | ❌               |
| 15  | 03  | Value Semantic             | Reference Type  | Value Type       |
|     | ►   | Memory Location            | Heap            | Stack            |
| 16  | 04  | Creating use `new` keyword | Mandatory       | Not Mandatory    |

</div>

`Class`

`Struct`

- Constructor:
  - cannot have constructor with empty params list
  - params less constructor exist implicitly inside struct
- Fields
  - cannot initialize with value
- Inheritance
  - Doesn't support `protected` keyword
  - Doesn't support `virtual` keyword
  - Struct implicitly inherits `Object` base class as all thing in c# inherit from `Object` class
- Recommended For Large Data
  - Maximum 16 Bytes => Size of 4 int `Int32`
  - Don't put reference type inside struct
- Creating use `new` keyword

  ```c#
    struct MyStruct
    {
        public void Print()
        {
            Console.WriteLine("Struct Print");
        }
    }

    MyStruct s1 = new MyStruct(); // Normal
    s1.Print();

    MyStruct s2; // Initialize without new
    s2.Print();
  ```

  But if Struct have private field that require constructor u must use `new`

  If struct have public field and u will not initialize it u must use `new`

  using implicit construct give all fields its default value

  ```c#
    struct MyStruct
    {
        public int Id;
        public void Print()
        {
            Console.WriteLine("Struct Print");
        }
    }

    MyStruct s1 = new MyStruct(); // Normal
    s1.Print();

    MyStruct s2; // Initialize without new
    s2.Id = 4;
    s2.Print();

    MyStruct s3; // Wrong
    s3.Print();

    MyStruct s3 = new MyStruct(); // ✔
    s3.Print();
  ```

### WHAT IS STRUCT

Immutable objects mean that once the constructor for an object has completed its execution, that instance can't be altered

### WHY STRUCT

`ChatGPT` Structs in C# offer several advantages and use cases, which make them a valuable tool in certain scenarios:

- Value Type Semantics: Structs are value types, and when you assign a struct to another variable or pass it as a method parameter, a copy of the struct's value is made. This can lead to better memory locality and performance in certain situations compared to reference types (classes).

- Stack Allocation: Structs are typically allocated on the stack, which can be more efficient than heap allocation used for reference types. This is especially beneficial for small and lightweight objects that are frequently created and destroyed.

- Memory Efficiency: If you have small data structures that don't need reference semantics or additional overhead, using structs can be more memory-efficient than using classes.

- Immutable Structs: As mentioned earlier, you can create immutable structs, which are particularly useful for representing simple data without the need for mutation. Immutable structs can help in writing safer and more predictable code.

- Performance-Critical Applications: In performance-critical applications, such as game development or real-time systems, using structs can be beneficial to reduce memory overhead and improve performance.

- Interoperability: Structs are useful when working with low-level or platform-specific code or when you need to interface with unmanaged code. They can help with data marshaling and provide control over memory layout.

- Encapsulation: Structs can be used to group related data fields together, offering a way to encapsulate data and behavior within a single entity.

Despite their advantages, it's essential to be mindful of the limitations and characteristics of structs:

- Larger structs: If a struct becomes too large, copying it can become expensive, and it might be more efficient to use a class instead.
- Reference semantics: Structs don't support reference semantics like classes, so be cautious when using them to represent entities with shared data and behavior.
- Initialization overhead: Structs require proper initialization of all their fields, as they don't have default constructors like classes.

In conclusion, structs are a powerful tool in C#, offering better performance and memory efficiency for certain use cases. However, the decision to use structs or classes should be based on careful consideration of the specific requirements and characteristics of your application. For most scenarios involving complex behavior or shared data, classes are more suitable, while structs excel in simple, lightweight, and performance-critical situations.

### REFERENCE VS. VALVE

### READONLY STRUCT

If your struct fields are `readonly` then you can mark struct to be `readonly` to enforce `readonly`

```c#
  readonly struct Point
  {
      // Read-only fields
      public readonly int X;
      public readonly int Y;

      // Constructor to initialize fields
      public Point(int x, int y)
      {
          X = x;
          Y = y;
      }
  }
```

U cannot mark class as `readonly`

```c#
  readonly class Point // wrong
  {
      // Read-only fields
      public readonly int X;
      public readonly int Y;

      // Constructor to initialize fields
      public Point(int x, int y)
      {
          X = x;
          Y = y;
      }
  }
```

### DATETIME CLASS

### Note

- All value type are `struct`
  - int
  - bool
  - double
  - ...etc

`ChatGPT` In C#, structs are value types, and their nature is not inherently immutable. By default, the fields of a struct are not read-only, meaning their values can be modified after the struct is created.

When you create a struct in C#, it behaves like any other value type, such as int, float, or DateTime. If you assign a struct to another variable or pass it as a parameter to a method, a copy of the struct's value is made, and modifications to one instance of the struct will not affect the other.

However, you can choose to create an immutable struct in C# by following certain guidelines and making the fields read-only, as mentioned in the previous response. By using read-only fields and ensuring that the struct's members cannot be modified after initialization, you can create an immutable-like behavior for the struct.

Here's an example of an immutable-like struct:

```c#
public struct ImmutablePoint
{
    // Read-only fields
    public readonly int X;
    public readonly int Y;

    // Constructor to initialize fields
    public ImmutablePoint(int x, int y)
    {
        X = x;
        Y = y;
    }
}
```

With this implementation, the ImmutablePoint struct behaves like an immutable type because its fields are read-only, and their values cannot be changed after the struct is created.

However, it's important to note that C# structs are not true reference types like classes. Immutable structs do not offer the same advantages as true immutable reference types in terms of thread safety and sharing of references. Therefore, you should carefully consider the use of immutable structs based on the specific requirements and characteristics of your application.

## 020 Enums

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_020/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=22)

- Content
  - WHAT IS ENUMERATION
  - WHY ENUMERATION
  - SIMPLE ENUM
  - FLAG ENUM
  - HOW TO PARSE ENUM
  - LOOP ON ENUM

### WHAT IS ENUMERATION

- Increase code readability
- Strongly typed named constants

### WHY ENUMERATION

- Group related const variable

```c#
cont int JAN = 1;
cont int FEB = 2;
cont int MAR = 3;
cont int APR = 4;
cont int MAY = 5;
cont int JUN = 6;
cont int JUL = 7;
cont int AUG = 8;
cont int SEP = 9;
cont int OCT = 10;
cont int NOV = 11;
cont int DEC = 12;
```

### SIMPLE ENUM

- Enum values by default start with zero and increase by one follow the definition text order

```c#
  enum Month
  {
      JAN,  // 0
      FEB,  // 1
      MAR,  // 2
      APR,  // 3
      MAY,  // 4
      JUN,  // 5
      JUL,  // 6
      AUG,  // 7
      SEP,  // 8
      OCT,  // 9
      NOV,  // 10
      DEC   // 11
  }
```

- If u assign value at start the following will be incremented

```c#
  enum Month
  {
      JAN = 101,  // 101
      FEB,        // 102
      MAR,        // 103
      APR,        // 104
      ...
  }
```

- Enum type by default is int

you can explicitly specify any other integral numeric type

`long` `short` `byte` ...etc

```c#
  enum Month : long
  {
      JAN = 1234567890123,
      FEB,
      MAR,
      ...
  }
```

### FLAG ENUM

`FLAG` => 0 and 1

Enum value have list of possible values

```c#
  [Flags]
  enum DAY
  {
      NONE = 0b_0000_0000, // 0
      MONDAY = 0b_0000_0001, // 1
      TUESDAY = 0b_0000_0010, // 2
      WEDNESDAY = 0b_0000_0100, // 4
      THURSDAY = 0b_0000_1000, // 8
      FRIDAY = 0b_0001_0000, // 16
      SATURDAY = 0b_0010_0000, // 32
      SUNDAY = 0b_0100_0000, // 64
      WEEKEND = SUNDAY | SATURDAY,
      BUSDAY = MONDAY | TUESDAY | WEDNESDAY | THURSDAY | FRIDAY ,
  }

  var day = (DAY.SATURDAY | DAY.SUNDAY);

  if(day.HasFlag(DAY.WEEKEND))
  {
    Console.WriteLine("Enjoy weekend");
  }
```

### HOW TO PARSE ENUM

#### Get value using cast

```c#
var day = DAY.SATURDAY ;

Console.WriteLine((int)day);
```

#### Get name

```c#
var day = DAY.SATURDAY ;

day.ToString();
```

#### Convert string to enum

- `Enum.Parse()`
  Enum is case sensitive

  ```c#
  var d = "MONDAY";

  var dEnum = Enum.Parse(typeof(DAY), d);
  ```

- `Enum.TryParse()`

  ```c#
  if(Enum.TryParse(typeof(DAY),out DAY d))
  {
      Console.WriteLine(d);
  }
  ```

- `Enum.IsDefined()`
  Deal with string and value
  ```c#
  var toParse = 3;
  if(Enum.IsDefined(typeof(DAY),toParse))
  {
      var dEnum = Enum.Parse(typeof(DAY), toParse);
      Console.WriteLine(d);
  }
  ```

### Note

- `typeof(<Object>)` return type of given object

### LOOP ON ENUM

- Iterate Enum Names`Enum.GetNames(typeof(<RequiredEnum>))`

```c#
foreach (var day in Enum.GetNames(typeof(DAY)))
{
    Console.WriteLine(day); // day is a string value
}
```

- Iterate Enum Values `Enum.GetValues(typeof(<RequiredEnum>))`

```c#
foreach (var day in Enum.GetNames(typeof(DAY)))
{
    Console.GetValues(day); // day is a object value
}
```

### Represent Binary in c#

```c#
int a = 0b_0000_0000; // 0
int b = 0b_0000_0001; // 1
int c = 0b_0000_0010; // 2
```

## 021 Inheritance | Inheritance

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_021/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=23)

- Content

  - WHAT, WHY AND HOM
  - CASTING AND CONVERSION
  - ABSTRACT/SEALED/VIRTUAL
  - POLYMORPHISM
  - CONSTRUCTOR AND INHERITANCE
  - OBJECT CLASS

### WHAT, WHY AND HOM

- **WHAT**

  Technique which let a type acquire all the properties and behaviors its parent automatically

- **WHY**

  - REUSABILITY
  - MAINTAINABILITY
  - EXTENSIBILITY

- **HOW**

```c#
  class Animal
  {
      public void Move()
      {
          Console.WriteLine("Moving");
      }
  }

  class Eagle
  {
      public void Move()
      {
          Console.WriteLine("Moving");
      }

      public void Fly()
      {
          Console.WriteLine("Flying");
      }
  }
```

In `Eagle` class there is repeated method called move from `Animal` class

so we `Eagle` can inherit `Animal` class

```c#
  class Animal
  {
      public void Move()
      {
          Console.WriteLine("Moving");
      }
  }

  class Eagle : Animal
  {
      public void Fly()
      {
          Console.WriteLine("Flying");
      }
  }
```

- So Now Eagle can see any member in Animal class which is

  - public
  - internal
  - protected : A protected member is accessible within
    its class and by derived class instances

### RESTRICTION

Class can inherit from only a single class

```c#
class Person {}
class Person2 {}

class Employee : Person {}           // Fine

class Employee : Person , Person2 {} // Wrong
```

Class can be inherited by many classes

```c#
class Animal {}

class Bird : Animal {}

class Mammals : Animal {}
```

### CASTING AND CONVERSION

- UP CASTING

  CREATES A BASE CLASS REFERENCE FROM A SUBCLASS REFERENCE

  ```C#
  Eagle e = new Eagle();
  Animal a = e; // UP CASTING
  ```

- DOWN CASTING

  CREATES A SUBCLASS REFERENCE FROM A BASE CLASS REFERENCE

  Must be Explicit

  ```C#
  Eagle e = new Eagle();
  Animal a = e;         // UP CASTING

  Eagle e2 = (Eagle)a; // DOWN CASTING
  ```

#### Casting with `as` keyword

```c#
class Animal {}

class Bird : Animal {}

class Eagle : Bird {}

class Falcon : Bird {}
```

```c#
  Eagle eagle = new Eagle();
  Animal animal = eagle;         // UP CASTING

  Falcon falcon = (Falcon)animal; // Wrong | Exception
```

You cannot convert `Eagle` to `Falcon`

To avoid this case we use `as` if conversion failed it will return null

```c#
  Eagle eagle = new Eagle();
  Animal animal = eagle;         // UP CASTING

  Falcon falcon = animal as Falcon;
```

#### Check type with `is` keyword

```c#
  Eagle eagle = new Eagle();
  Animal animal = eagle;         // UP CASTING

  if(animal is Falcon)
  {
      Console.WriteLine("animal is Falcon");
  }
  else
  {
      Console.WriteLine("animal is not a Falcon");
  }
```

### ABSTRACT | SEALED CLASS

#### ABSTRACT CLASS

- Abstracted class cannot be instantiated directly

- If u have a class that is not supposed to create instance with

- Always has abstracted members

For example `Animal` class nothing will be animal

```c#
Animal a = new Animal(); // we want to prevent this behavior
```

To do that we use `abstract` keyword

```c#
abstract class Animal {}

abstract class Bird : Animal {}

class Eagle : Bird {}

class Falcon : Bird {}
```

Now `Animal` and `Bird` exist only to be inherited

#### SEALED CLASS

- Sealed class cannot be inherited

```c#
abstract class Animal {}

abstract class Bird : Animal {}

class Eagle : Bird {}

sealed class EgyptianEagle : Eagle {}

class AmericanEagle : EgyptianEagle {} // wrong you cannot inherit EgyptianEagle
```

### VIRTUAL | ABSTRACT | SEALED MEMBERS

- VIRTUAL MEMBER OVERRIDE

  - First Condition: Base Class Declare Member as `virtual` (has default implementation)
  - Second Condition: Add `override` keyword to the override method to (may override)

```c#
abstract class Animal {
  // default implementation
  public virtual void Speak()
  {
      Console.WriteLine("Animal is Speaking...");
  }
}

class Dog : Animal {
  // override is optional
  public override void Speak()
  {
      // calling base is optional
      base.Speak();
      Console.WriteLine("Park!...");
  }
}

class Cat : Animal {
  // override is optional
  public override void Speak()
  {
      // calling base is optional
      base.Speak();
      Console.WriteLine("Meow!...");
  }
}

Dog dog = new Dog();
dog.Speak(); // "Animal is Speaking..." \n "Park!..."

Cat cat = new Cat();
cat.Speak(); // "Animal is Speaking..." \n "Meow!..."
```

- ABSTRACT MEMBER OVERRIDE
  - First Condition: abstract member must be in abstract class and it has to default implementation
  - Second Condition: Add Override keyword to the override method to and overriding is mandatory

```c#
abstract class Animal {
  // has no default implementation
  public abstract void Speak();
}

class Dog : Animal {
  // override is Mandatory
  public override void Speak()
  {
      Console.WriteLine("Park!...");
  }
}

class Cat : Animal {
  // override is Mandatory
  public override void Speak()
  {
      Console.WriteLine("Meow!...");
  }
}

Dog dog = new Dog();
dog.Speak(); // "Animal is Speaking..." \n "Park!..."

Cat cat = new Cat();
cat.Speak(); // "Animal is Speaking..." \n "Meow!..."
```

- SEALED MEMBERS
  - Sealed Member can not be overridden in the derived class

```c#
abstract class Animal {
  public abstract void Speak();
}

class Cat : Animal {
  public sealed override void Speak()
  {
      Console.WriteLine("Meow!...");
  }
}

class EgyptianCat : Cat {
  // Wrong cannot be overridden
  public override void Speak()
  {
      Console.WriteLine("Meow!...");
  }
}
```

### POLYMORPHISM

When we inherit from class we can access its public and internal and protected members

But what if i want to modify the behavior?

In the following example

```c#
abstract class Animal {
  public void Speak()
  {
      Console.WriteLine("Animal is Speaking...");
  }
}

class Dog : Animal {}
class Cat : Animal {}

Dog dog = new Dog();
dog.Speak(); // "Animal is Speaking..."

Cat cat = new Cat();
cat.Speak(); // "Animal is Speaking..."
```

I want cat to `Meow` and Dog to `Park` and Here come `polymorphism`

how to implement that?

#### Using Virtual | Override

Using `virtual` with class members means that subclasses that inherit from the base can modify and change the behavior of that member

we use `override` to override `virtual` members inside subclasses

- First Condition: Base Class Declare Member as `virtual` (has default implementation)
- Second Condition: Add `override` keyword to the overrided method to (may override)

```c#
abstract class Animal {
  public virtual void Speak()
  {
      Console.WriteLine("Animal is Speaking...");
  }
}

class Dog : Animal {
  public override void Speak()
  {
      base.Speak();
      Console.WriteLine("Park!...");
  }
}

class Cat : Animal {
  public override void Speak()
  {
      base.Speak();
      Console.WriteLine("Meow!...");
  }
}

Dog dog = new Dog();
dog.Speak(); // "Animal is Speaking..." \n "Park!..."

Cat cat = new Cat();
cat.Speak(); // "Animal is Speaking..." \n "Meow!..."
```

#### THIS VS BASE

- this

  Call any member inside the class

- base

  Call any member inside the base class

  ```c#
  class Dog : Animal {
    public virtual void Speak()
    {
        base.Speak();
        Console.WriteLine("Park!...");
    }
  }
  ```

  Removing the `base` keyword inside the method will change the behavior of the method and result in a `StackOverflowException`.

  ```c#
  class Dog : Animal {
    public virtual void Speak()
    {
        Speak(); // Recursion
        Console.WriteLine("Park!...");
    }
  }

  Dog dog = new Dog();
  dog.Speak(); // StackOverflowException
  ```

  `Q:` Is base Syntax Sugar?

  `Answer By ChatGPT:` "base" is not syntactic sugar in C#. It is a keyword used for explicit reference to members (methods or constructors) of the base class. It is an essential aspect of inheritance and polymorphism in object-oriented programming.

### OBJECT CLASS

The ultimate base class for all `.NET` types

#### TO STRING

Default textual representation to our object

By Default it output `NameSpace.ClassName`

#### GET TYPE

Return the type of our instance

### CONSTRUCTOR AND INHERITANCE

THE BASE CLASS'S CONSTRUCTORS ARE ACCESSIBLE TO THE DERIVED CLASS BUT ARE NEVER AUTOMATICALLY INHERITED

```c#
class MyBase
{
    public int x;

    public MyBase() {}

    public MyBase(int x)
    {
        this.x = x;
    }
}

class MySub : MyBase
{
}
```

```c#
MyBase myBase = new MyBase();
MyBase myBase2 = new MyBase(10);

MySub mySub = new MySub();      // Default
MySub mySub2 = new MySub(10);   // Wrong
```

Everything is inherited except for constructor it should be called from derived class constructor

using `: base(<ParamList>)`

```c#
class MySub : MyBase
{
    public MySub(int x) : base(x)
    {}
}
```

```c#
MyBase myBase = new MyBase();
MyBase myBase2 = new MyBase(10);

MySub mySub = new MySub();      // Wrong
MySub mySub2 = new MySub(10);   // Valid
```

The default constructor now is not exist

```c#
class MySub : MyBase
{
    public MySub()
    {}

    public MySub(int x) : base(x)
    {}
}
```

```c#
MyBase myBase = new MyBase();
MyBase myBase2 = new MyBase(10);

MySub mySub = new MySub();      // Valid
MySub mySub2 = new MySub(10);   // Valid
```

**IMPORTANT**

BASE-CLASS constructors always execute first this ensures that base initialization occurs before specialized initialization

### HIDING INHERITED MEMBERS

A base class and a subclass can define identical members sub class will hide the implementation of the parent

```c#
class MyBase
{
    public string Name = "Base";
}

class MySub : MyBase
{
  public string Name = "Sub"; // u will find warning here that this member hide a member in base
}

MySub sub = new MySub();

Console.WriteLine(sub.Name); // Sub
```

To rid of warning use `new` keyword

```c#
class MySub : MyBase
{
  public new string Name = "Sub";
}
```

## 022 Interface

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_022/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=24)

- Content

  - DEFINITION
  - IMPLEMENTING INTERFACE
  - INTERFACE VS ABSTRACT CLASS
  - ABSTRACT VS CONCRETE
  - TIGHT / LOOSE COUPLING
  - REAL WORLD EXAMPLE

### DEFINITION

- Only have a Behavior
- Not have a state
- Same as class but doesn't have fields
- Interface is a contract

  An interface defines a contract. Any class or struct that implements that contract must provide an implementation of the members defined in the interface

- Class can inherit one or more interface

```c#
  abstract class Vehicle
  {
      protected string Brand;
      protected string Model;
      protected int Year;

      public Vehicle(string brand, string model, int year)
      {
          Brand = brand;
          Model = model;
          Year = year;
      }
  }

  interface ILoader
  {
      void Load();
      void Unload();
  }

  interface IDrivable
  {
      void Move();
      void Stop();
  }
```

```c#
  class Caterpillar : Vehicle, ILoader, IDrivable
  {
      public Honda(string brand, string model, int year)
          : base(brand, model, year)
      {}

      void Load() {}

      void Unload() {}

      void Move() {}

      void Stop() {}
  }
```

#### Naming convention for best practices

Interfaces start with `I`

```c#
  interface ILoader
  {
      void Load();
      void Unload();
  }
```

### IMPLEMENTING INTERFACE

- We have two ways to impl interfaces
  - Implicit
  - Explicit

#### Implicit

```c#
  abstract class Vehicle
  {
      protected string Brand;
      protected string Model;
      protected int Year;

      public Vehicle(string brand, string model, int year)
      {
          Brand = brand;
          Model = model;
          Year = year;
      }
  }

  interface ILoader
  {
      void Load();
      void Unload();
  }

  interface IDrivable
  {
      void Move();
      void Stop();
  }
```

```c#
  class Caterpillar : Vehicle, ILoader, IDrivable
  {
      public Honda(string brand, string model, int year)
          : base(brand, model, year)
      {}

      void Load() {}

      void Unload() {}

      void Move()  {}

      void Stop() {}
  }
```

#### Explicit

What if i have two interfaces that have methods with identical names?

```c#
  interface IMove
  {
      void Move();
  }

  interface IDisplace
  {
      void Move();
  }
```

In this case we use explicit implementation

```c#
  class Vehicle: IMove, IDisplace
  {
      void IMove.Move()
      {}

      void IDisplace.Move()
      {}
  }
```

#### Default Implementation `c# 8`

```c#
  interface IMove
  {
      void Move();
      void Turn()
      {
          Console.WriteLine("Turning...");
      }
  }
```

### INTERFACE VS ABSTRACT CLASS

#### Abstract

An abstract class is meant to be used as the base class from which other classes are derived.

The derived class is expected to provide implementations for the member functions that are not implemented in the base class. A derived class that implements all the missing

### ABSTRACT VS CONCRETE TYPE

- ABSTRACT

```c#
abstract class Vehicle // ABSTRACT
{
    protected string Brand;
    protected string Model;
    protected int Year;

    public Vehicle(string brand, string model, int year)
    {
        Brand = brand;
        Model = model;
        Year = year;
    }
}
```

- CONCRETE

```c#
class Honda : Vehicle // CONCRETE
{
    public Honda(string brand, string model, int year)
        : base(brand, model, year)
    {
    }
}
```

#### What use with `new` keyword?

After `new` we only use concrete type

```c#
Vehicle honda = new Vehicle("","",2021); // Not Valid

Vehicle honda = new Honda("","",2021); // Valid
Honda honda = new Honda("","",2021); // Valid
```

### TIGHT / LOOSE COUPLING

#### Tight Coupling

Tight coupling occurs when two or more components are strongly dependent on each other.

In this scenario, changes in one component often require changes in the dependent component, making the code more brittle and harder to maintain.

Tight coupling can lead to code that is difficult to modify, test, and extend.

#### Loose Coupling

Loose coupling, on the other hand, reduces the dependency between components by ensuring that they interact through well-defined interfaces.

In this approach, each component operates independently and knows very little about the internal workings of other components.

Loose coupling makes the code more flexible, maintainable, and easier to understand.

#### Summary

- Tight coupling means one class is dependent on another class

- Loose coupling means one class is dependent on interface rather than class

### REAL WORLD EXAMPLE

```c#
  class Cashier
  {
      private IPayment payment;

      public Cashier(IPayment payment)
      {
          this.payment = payment;
      }

      public void CheckOut(decimal amount)
      {
          payment.Pay(amount);
      }
  }

  interface IPayment
  {
      void Pay(decimal amount);
  }

  class MasterCard : IPayment
  {
      public void Pay(decimal amount)
      {
          Console.WriteLine($"MasterCard Pay ${amount:N0}");
      }
  }

  class Visa : IPayment
  {
      public void Pay(decimal amount)
      {
          Console.WriteLine($"Visa Pay ${amount:N0}");
      }
  }

  class Cash : IPayment
  {
      public void Pay(decimal amount)
      {
          Console.WriteLine($"Cash Pay ${amount:N0}");
      }
  }
```

```c#
IPayment payment = new Visa();
payment = new MasterCard();
payment = new Cash();

Cashier cashier = new Cashier(payment);
cashier.CheckOut(1000);
```

## 023 Generics

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_023/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=25)

- Content
  - BEFORE GENERICS
  - WHAT WHY AND HOW
  - GENERICS METHOD
  - GENERICS CLASS
  - GENERICS CONSTRAINTS
  - .NET GENERICS/COLLECTIONS

### BEFORE GENERICS

### WHAT WHY AND HOW

#### WHAT

#### WHY

- Performance

  No boxing or unboxing happen

- Reusability
- Type safety
- Avoid mistakes

#### HOW

### GENERICS METHOD

A method declared with the type parameters for its return type or parameters is called a generic method. data type will be determined by the consumer

```c#
void print(int value)
{
    Console.WriteLine(value);
}
void print(String value)
{
    Console.WriteLine(value);
}
void print(decimal value)
{
    Console.WriteLine(value);
}
```

Using generics

```c#
void print<T>(T value)
{
    Console.WriteLine(value);
}

print(10);                // Valid: Implicit
print<int>(10);           // Valid: Explicit

print("10");              // Valid: Implicit
print<string>("10");      // Valid: Explicit
```

`<T>` is called Type parameter

### GENERICS CLASS

Defined using a type parameter in an angle brackets after the class

```c#
  class MyList<T>
  {
      T[] _items;

      public void Add(T value)
      {
          if (_items == null)
          {
              _items = new T[1];
              _items[0] = value;
          }
          else
          {
              var dst = new T[_items.Length + 1];

              for (int i = 0; i < _items.Length ; i++)
              {
                  dst[i] = _items[i];
              }

              dst[_items.Length] = value;

              _items = dst;
          }
      }

      public void RemoveAt(int pos)
      {
          if (pos < 0 || pos > _items.Length) return;

          var index = 0;
          var dst = new T[_items.Length - 1];

          for (int i = 0; i < _items.Length; i++)
          {
              if (i == pos) continue;
              dst[index++] = _items[i];
          }

          _items = dst;
      }

      public bool IsEmpty => _items is null || _items.Length == 0;
      public int Count => _items is null ? 0 : _items.Length;

      public void Display()
      {
          Console.Write("{");

          for (int i = 0; i < _items.Length; i++)
          {
              Console.Write(_items[i]);

              if (i < _items.Length - 1) Console.Write(", ");
          }

          Console.WriteLine("}");
      }
  }
```

```c#
  var list = new MyList<int>();
  list.Add(1);
  list.Add(2);
  list.Add(3);
  list.Add(4);
  list.Display();

  list.RemoveAt(0);
  list.RemoveAt(0);

  list.Display();

  Console.WriteLine($"List IsEmpty: {list.IsEmpty}");
  Console.WriteLine($"List Count: {list.Count}");
```

### GENERICS CONSTRAINTS

Allows you to use constraints to restrict client code to specify certain types while instantiating generic types. it will give a compile-time error to instantiate a generic type using a is not .allowed by the specified constraints

#### where T: constraint1, constraint2, constraint3

- `class` For Reference Type
  For Example

  ```c#
    class MyList<T> where T: class
    {
        T[] _items;

        ...
    }
  ```

  This prevent client create MyList of type which is not a class `Reference Type`

  for example client cannot create MyList of int or decimal and so on..

  ```c#
  class Dummy
  {
      public Dummy()
      {}

      public Dummy(int a)
      {}
  }

  class Person
  {
      public Person(String fName, String lName)
      {}
  }
  ```

  ```c#
    var list = new MyList<int>(); // Error
    var list = new MyList<bool>(); // Error
    var list = new MyList<double>(); // Error

    var list = new MyList<string>();
    var list = new MyList<Person>();
    var list = new MyList<Dummy>();
  ```

- `new()` For ParameterLess Constructor
  For Example

  ```c#
    class MyList<T> where T: class, new()
    {
        T[] _items;

        ...
    }
  ```

  Client can only create MyList of `Reference Type` and must init with `new()` without params

  ```c#
  class Dummy
  {
      public Dummy()
      {}

      public Dummy(int a)
      {}
  }

  class Person
  {
      public Person(String fName, String lName)
      {}
  }
  ```

  ```c#
    var list = new MyList<int>(); // Error
    var list = new MyList<bool>(); // Error
    var list = new MyList<double>(); // Error

    var list = new MyList<string>(); // Error
    var list = new MyList<Person>(); // Error
    var list = new MyList<Dummy>();
  ```

### .NET GENERICS/COLLECTIONS

### System.Collections.Generic

```c#
System.Collections.Generic ;
```

Ready predefined collections form microsoft

```c#
  var list = new List<int>();
  list.Add(3);      // Valid
  list.Add(3);      // Valid
  list.Add(3m);     // Not Valid
  list.Add("3");    // Not Valid
  list.Add(true);   // Not Valid
```

### System.Collections

Not type safe

```c#
System.Collections.Generic ;
```

```c#
  var list = new ArrayList();
  list.Add(3);      // Valid
  list.Add(3);      // Valid
  list.Add(3m);     // Valid
  list.Add("3");    // Valid
  list.Add(true);   // Valid
```

### Note

- SANITY CHECK

  is a common phrase used in software development and other fields to refer to a basic and straightforward validation or verification process. It involves performing a quick evaluation or test to ensure that something appears to be reasonable, correct, or in good working order.

## 024 Generic Delegate Type

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_024/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=26)

- Content
  - WHAT, WHY AND HOW
  - ACTION DELEGATE
  - FUNC DELEGATE
  - PREDICATE DELEGATE
  - REAL WORLD EXAMPLE

### WHAT, WHY AND HOW

When you want to create a delegate that can work with multiple methods with different parameter types or return types, a generic delegate is the way to go. It saves you from having to create multiple delegate types for various method signatures, promoting code reusability and maintainability.

#### How

```c#
public delegate bool Filter<T>(T n);
```

#### using `in`

`<in T>`

Mean that param of type `T` only use as input

```c#
public delegate bool Filter<in T>(T n);
```

#### using `out`

`<out T>`

Mean that param of type `T` only use as output / return type

```c#
public delegate T2 Filter<in T, out T2>(T n);
```

### ACTION DELEGATE

- Take up to 16 input
- Doesn't have return a value

```c#
Action<in T1,in T2....,in T16> ActionName = <Method>
```

```c#
Action<string> printAction = Print;

printAction("Anything");

void Print(string)
{
  /*Print*/
}
```

### FUNC DELEGATE

- Take up to 16 input
- Have a return value

```c#
Action<in T1,in T2....,in T16,out TResult> ActionName = <Method>
```

```c#
Func<int, int, int> addFunc = Add;

int value = addFunc(2,5);

int Add(int num1, int num2)
{
  return num1 + num2;
}
```

### PREDICATE DELEGATE

- Take 1 input
- Return bool only

```c#
Predicate<in T1> PredicateName = <Method>
```

```c#
Predicate<int> isEvenPredicate = isEven;

bool value = isEvenPredicate(5);

bool isEven(int n)=> 2 % 2 == 0;
```

### REAL WORLD EXAMPLE

### Note

- SPAGHETTI CODE:
  IS THE CODE THAT IS DIFFICULT TO MAINTAIN

## 025 Exceptions

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_025/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=27)

- Content

  - EXCEPTION CLASS
  - BUILT-IN EXCEPTIONS
  - CUSTOM EXCEPTIONS
  - HANDLE EXCEPTION TRY/CATCH
  - SWALLOW/DUCK EXCEPTION
  - EXCEPTION FILTER `c# 6`

- `Exception:`

  Is an event, which occurs during the execution of a program, that disrupts the normal flow of the program's instructions

### EXCEPTION CLASS

Is the super class of every exception in c#

### HANDLE EXCEPTION TRY/CATCH

Syntax

```c#
  try
  {
      /*Code that may have exception*/
  }
  catch(<Class Of Type Exception> ex)
  {
      // Optional
      /*Handle incoming Exception*/
      // ex.Message
  }
  /*
  catch
  {
  }
  */
  finally
  {
      // Optional
      /*After Code End*/
      // CleanUp
  }
```

1. Process `try` block if exception happen go to `catch` block if not or if try done go to `finally` block
2. Both of `catch` and `finally` Block are optional but one of them must be exist

You can handle as many exception as u want and treat every one as needed

```c#
  try
  {

  }
  catch (DivideByZeroException ex)
  {
      /*TODO*/
  }
  catch (AccessViolationException ex)
  {
      /*TODO*/
  }
  catch
  {
      /*TODO if not of the above*/
  }
  finally
  {
      /*TODO when finish*/
  }
```

### EXCEPTION FILTER `c# 6`

```c#
  try
  {

  }
  catch (DivideByZeroException ex) when (/*Condition*/)
  {
      /*TODO*/
  }
```

```c#
  try
  {

  }
  catch (DivideByZeroException ex) when (ex.Source = "")
  {
      /*TODO*/
  }
```

### BUILT-IN EXCEPTIONS

[See BUILT-IN EXCEPTIONS](https://learn.microsoft.com/en-us/dotnet/api/system.exception?view=net-7.0)

### CUSTOM EXCEPTIONS

Naming convenient custom exception end with `Exception`

```c#
  public class AccidentException :Exception
  {

      public string Location { get; set; }

      public AccidentException(string location, string message)
      : base(message)
      {
        Location = location;
      }
  }
```

### SWALLOW/DUCK EXCEPTION

#### SWALLOW

Catch the exception without doing any logic to be handled

```c#
  try
  {

  }
  catch (DivideByZeroException ex) when (ex.Source = "")
  {
      /*No Thing*/
  }
```

Avoid swallow and make at least one of these

- Inform the user
- Log the exception
- Ducking (rethrowing)

#### DUCK

To rethrow the exception

```c#
  try
  {

  }
  catch (DivideByZeroException ex) when (ex.Source = "")
  {
      throw;
  }
```

### Note

- `LOGGING`

  Is keeping a record of all data input, processes, data output, and final
  results in a program

- `FAKING / MOCKING`

## 026 Enumerators Iterators

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_026/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=28)

- Content

  - IENUMERATOR VS. IENUMERABLE
  - EQUALS()
  - GetHashCode()
  - YIELD KEYWORD
  - ICOMPARABLE

### EQUALS()

- `==`

  Check if reference are equals

  to change this behavior for objects we use operator overloading and override Equals()

- `.Equals()`

  Check content of objects but by default it check references so we override it

```c#
class Any
{
  public int Id {get; set;};

  public override bool Equals(Object object)
  {
    if(object == null || !(object is Any))
      return false

    return object.Id == this.Id;
  }

  public static bool operator ==(Any left, Any right)
  {
    return left.Equals(right);
  }

  public static bool operator !=(Any left, Any right)
  {
    return !left.Equals(right);
  }
}
```

### GetHashCode()

A hash code a numeric value which is used to insert and identify an object in a hash-based collection

- Every object has a unique hash code

- We can override this code
  It's recommended to use prime numbers to reduce collisions

```c#
public override int GetHashCode()
{
  int hash = 13
  hash = (hash * 7) + Id.GetHashCode();
  hash = (hash * 7) + Name.GetHashCode();
  hash = (hash * 7) + Salary.GetHashCode();
  return hash;
}
```

#### Note

- If two things are equal then they must return the same value for `GetHashCode()`

- If the `GetHashCode()` is equal, it is not necessary for them to be the same

- This is a collision, and equals will be decide

### IENUMERATOR VS. IENUMERABLE `Old Way`

To make iteration over you object possible u have to inherit from `IEnumerable`

For example I have class that contains private list inside

```c#
  public class Employees
  {
      private string[] _list;

      public Employees(string[] emps)
      {
          _list = emps;
      }
  }
```

So how to impalement that

```c#
  public class Employees : IEnumerable
  {
      private string[] _list;

      public Employees(string[] emps)
      {
          _list = emps;
      }

      public IEnumerator GetEnumerator() => new Enumerator(this);

      class Enumerator : IEnumerator
      {
          int currentIndex = -1;
          Employees _employees;

          public Enumerator(Employees employees)
          {
              _employees = employees;
          }

          public object Current
          {
              get
              {
                  if (currentIndex == -1) throw new InvalidOperationException("Not started yet");
                  if (currentIndex > _employees._list.Length) throw new InvalidOperationException("Out the boundary");
                  return _employees._list[currentIndex];
              }
          }

          public bool MoveNext()
          {
              if(currentIndex >= _employees._list.Length - 1) return false;
              return ++currentIndex < _employees._list.Length - 1;
          }

          public void Reset() => currentIndex = -1;
      }
  }
```

### YIELD KEYWORD `New Way`

Yield automate the process of enumeration for you

```c#
  public class Employees : IEnumerable
  {
      private string[] _list;

      public Employees(string[] emps)
      {
          _list = emps;
      }

      public IEnumerator GetEnumerator()
      {
          foreach (var item in _list)
          {
              yield return item;
          }
      }
  }
```

### ICOMPARABLE

If you want to compare objects together or you want to sort then you can implement the `IComparable` interface

the u have to make `int CompareTo(Object obj) {}`

- 1 =>`this > obj`
- 0 =>`this == obj`
- -1 =>`this < obj`

```c#
class Temperature : IComparable
{
    private int _value;
    public Temperature(int temp)
    {
        _value = temp;
    }
    public int CompareTo(object? obj)
    {
        if(obj == null) return -1;
        var temp = obj as Temperature;
        if (temp == null) throw new ArgumentException("Provide Temperature Object");

       return this._value.CompareTo(temp._value);
    }
}
```

## 027 XML Documentation

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_027/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=29)

- Content

  - WHAT, WHY AND HOW
  - COMMENT Vs XML DOCUMENTATION
  - STANDARD DOCUMENTATION TAGs
  - EXTERNAL XML DOCUMENT
  - BEST PRACTICES

### NameOF `c# 6`

In C#, `nameof` is an operator that allows you to obtain the name of a variable, type, or member as a constant string at compile-time. It was introduced in C# 6.0 to simplify code and avoid hardcoding strings for names, reducing the risk of errors when refactoring.

Usage:
The `nameof` operator is followed by the element (variable, type, or member) for which you want to retrieve the name. The syntax is as follows:

```c#
public class Program
{
    public static void Main()
    {
        // Using nameof with variables
        int age = 30;
        string name = "John";

        Console.WriteLine(nameof(age));  // Output: "age"
        Console.WriteLine(nameof(name)); // Output: "name"

        // Using nameof with types
        Console.WriteLine(nameof(int));    // Output: "int"
        Console.WriteLine(nameof(string)); // Output: "string"

        // Using nameof with members (properties or methods)
        Console.WriteLine(nameof(Person.Age));       // Output: "Age"
        Console.WriteLine(nameof(Person.GetName));   // Output: "GetName"
    }
}

public class Person
{
    public int Age { get; set; }

    public string GetName()
    {
        return "John";
    }
}

```

### WHAT, WHY AND HOW

### COMMENT Vs XML DOCUMENTATION

```c#
/// <summary>
///
/// </summary>
```

### STANDARD DOCUMENTATION TAGs

- remarks

  ```c#
  /// <summary>
  ///
  /// </summary>
  /// <remarks>
  ///
  /// </remarks>
  ```

- value

  ```c#
  /// <value>
  ///
  /// </value>
  ```

- param

  ```c#
  /// <param name= "ParamName"> </param>
  ```

- paramref

  refer to method params

  ```c#
  /// <paramref name= "ParamName"> </paramref>
  ```

- returns

  ```c#
  /// <returns> </returns>
  ```

- list

  ```c#
  /// <list type="bullet">
  /// ..items
  /// </list>
  ```

- item

  ```c#
  /// <item>
  /// <term></term>
  /// <description></description>
  /// </item>
  ```

- example

  ```c#
  /// <example>
  ///
  /// </example>
  ```

- code

  will help developers how to call this method

  ```c#
  /// <code>
  /// ...c# code
  /// </code>
  ```

- exception

  document the exceptions that may thrown from your method

  ```c#
  /// <exception cref="System.InvalidOperationException">Thrown when  <paramref name="fname"/> is null</exception>
  ```

- See

  Refer another method

  ```c#
  /// See <see cref="Generator.GenerateRandomPassword( int ) "/> to Generate Random_password
  ```

### EXTERNAL XML DOCUMENT

```c#
/// < include file="Generator.xm1" path='docs/members[@name="generator"]/Generator/*'/>
```

`/*` mean include everything

### BEST PRACTICES

- Any public member should be documented
- Less is more

## 028 Extension Methods

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_028/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=30)

- Content

  - What How and Why
  - Extension Method
  - Method Chaining vs Instance Method
  - Static Class and Extension Method

### What How and Why

### Static Class and Extension Method

```c#
public static class DateTimeHelper
{
    public static bool IsWeekEnd(DateTime value)
    {
        return value.DayOfWeek == DayOfWeek.Saturday || value.DayOfWeek == DayOfWeek.Sunday;
    }

    public static bool IsWeekDay(DateTime value)
    {
        return !IsWeekEnd(value);
    }
}
```

```c#
bool isWeekEnd = DateTimeHelper.IsWeekEnd(DateTime.Now);
```

### Extension Method

- Must be in static class

- The method should be static method
- Use `this` with type in method params list

By using `this` keyword with param list it's now become an extension method

```c#
public static class DateTimeExtension
{
    public static bool IsWeekEnd(this DateTime value)
    {
        return value.DayOfWeek == DayOfWeek.Saturday || value.DayOfWeek == DayOfWeek.Sunday;
    }

    public static bool IsWeekDay(this DateTime value)
    {
        return !IsWeekEnd(value);
    }
}
```

Call directly on the instance

- Recommended

```c#
bool isWeekEnd = DateTime.Now.IsWeekEnd();
```

U still can call the class name but you have to provide the instance to the method

```c#
bool isWeekEnd2 = DateTimeExtension.IsWeekEnd(DateTime.Now);
```

### Method Chaining vs Instance Method

When an extension method returns a value that has the same type as its this argument, it can be used to "chain" one or more method calls with a compatible signature

`Fluent API`

### Ambiguity

In case you have an extension method that have a method and the same signature already exist in instance definition

The instance definition will be executed

to solve this rename one of two

## 029 Assemblies

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_029/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=31)

- Content

  - ASSEMBLY DEFINITION
  - FRAMEWORKS AND ASSEMBLIES
  - IL VS. JIT
  - ILDASM / ILASM
  - HOW TO ACCESS METADATA
  - EMBEDDING RESOURCES

### ASSEMBLY DEFINITION

AN ASSEMBLY IS THE BASIC UNIT OF DEPLOYMENT IN .NET CORE

### FRAMEWORKS AND ASSEMBLIES

- OLD

  Assembly & Launcher ProjectName.exe

- NEW

  Assembly: ProjectName.dll

  Launcher: ProjectName.exe

### IL VS. JIT

- Il

  Intermediate Language

### Process Image

![](https://raw.githubusercontent.com/Courses-journey/dotnet/main/Metigator/01_mastering_csharp/assets/029_Assemblies.jpg)

### ILDASM / ILASM

- ILDASM

  Convert `dll` to `IL` code

  ```
  ildasm CAAssemblies.dll
  ```

- ILASM

  Convert `Il` code to `dll` and `exe`

  ```
  ilasm CAAssemblies.il /dll /exe
  ```

### HOW TO ACCESS METADATA

- METADATA

  To exchange data between assemblies

Accessing Metadata

```c#
var type = typeof(Employee);
var assembly = type.Assembly;
Console.WriteLine(assembly.FullName) ;
```

Using Reflection

```c#
var assembly = Assembly.GetExecutingAssembly();
Console.WriteLine(assembly.FullName) ;
```

### EMBEDDING RESOURCES

#### How to create

- Create Folder if u want
- Add your resource
- Right Click and choose Properties
- Build Action: Embedded resource
- Copy to Output Directory: Always Copy

#### How to access

For Example in our assembly called `CAAssemblies`

We create `data` folder

And put `countries.json` in it

```c#
var stream =
assembly. GetManifestResourceStream( "CAAssemblies.data.countries.json") ;
```

Another way

```c#
var stream =
assembly. GetManifestResourceStream(type, "data.countries.json") ;
```

Until now we get the stream we need to get data from it

```c#
// ReadBytes take int
// stream.Length of type Long
// Might have exception if length bigger than int max
var data = new BinaryReader(stream).ReadBytes((int)stream.Length);
```

After we finish what we want from stream we have to close it

```c#
stream.Close();
```

## 030 Reflection And Metadata

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_030/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=32)

- Content

  - WHAT, WHY AND HOM
  - OBTAIN TYPES
  - ACTIVATE TYPES
  - REFLECTION & MEMBERS
  - INVOKING MEMBERS
  - REFLECTING ASSEMBLIES

### WHAT, WHY AND HOM

- Reflection

  inspecting metadata and compiled code in the assembly at runtime

### OBTAIN TYPES

At runtime

```c#
Type t1 = DateTime.Now.GetType();
Console.WriteLine(t1);
```

At compile time

```c#
Type t2 = typeof(DateTime);
Console.WriteLine(t2);
```

#### FullName

Get Namespace.TypeName

```c#
Console.WriteLine(t1.FullName);
```

#### Namespace

Get Namespace

```c#
Console.WriteLine(t1.Namespace);
```

#### Name

Get TypeName

```c#
Console.WriteLine(t1.Name);
```

#### BaseType

Get BaseType `value` type or `object` type

```c#
Console.WriteLine(t1.BaseType);
```

### ACTIVATE TYPES

To instantiate class with reflection

- Params Less constructor

  ```c#
    Activator.CreateInstance(<Type to create from>); // return object
  ```

  For Example

  ```c#
    int i = (int) Activator.CreateInstance(typeof(int));
  ```

  We have to cast the result to the type we want as the result is object

- Params constructor

  ```c#
    Activator.CreateInstance(<Type to create from>,<ParamsList>); // return object
  ```

  For Example

  ```c#
    DateTime i = (DateTime) Activator.CreateInstance(typeof(DateTime), 2023,01,01);
  ```

  We have to cast the result to the type we want as the result is object

### REFLECTION & MEMBERS

#### Members

To access members use `GetMembers()`

By default it will return all public members

```c#
MemberInfo[] members = typeof(BankAccount).GetMembers();
```

TO get private and more stuff use `BindingFlags`

to mix use Bitwise or `|`

```c#
MemberInfo[] members = typeof(BankAccount).GetMembers(BindingFlags.NonPublic | BindingFlags.Instance | BindingFlags.Public);
```

#### Fields

To access fields use `GetFields()`

By default it will return all public Fields

```c#
FieldInfo[] fields = typeof(BankAccount).GetFields();
```

To get private and more stuff use `BindingFlags`

to mix use Bitwise or `|`

```c#
FieldInfo[] fields = typeof(BankAccount).GetFields(BindingFlags.NonPublic | BindingFlags.Instance | BindingFlags.Public);
```

- Events considered to be a field

#### Property

To access properties use `GetProperty()`

By default it will return all public Property

```c#
PropertyInfo[] properties = typeof(BankAccount).GetProperties();
```

To get private and more stuff use `BindingFlags`

to mix use Bitwise or `|`

```c#
PropertyInfo[] properties = typeof(BankAccount).GetProperties(BindingFlags.NonPublic | BindingFlags.Instance | BindingFlags.Public);
```

#### Event

To access events use `GetEvents()`

By default it will return all public Property

```c#
EventInfo[] events = typeof(BankAccount).GetEvents();
```

To get private and more stuff use `BindingFlags`

to mix use Bitwise or `|`

```c#
EventInfo[] events = typeof(BankAccount).GetEvents(BindingFlags.NonPublic | BindingFlags.Instance | BindingFlags.Public);
```

#### Constructor

To access constructors use `GetEvents()`

By default it will return all public Property

```c#
ConstructorInfo[] constructors = typeof(BankAccount).GetConstructors();
```

To get private and more stuff use `BindingFlags`

to mix use Bitwise or `|`

```c#
ConstructorInfo[] constructors = typeof(BankAccount).GetConstructors();
```

#### GetMember

Get members by providing its name

```c#
MemberInfo[] constructors = typeof(BankAccount).GetMember(".ctor");
```

### INVOKING MEMBERS

```c#
var account =  new BankAccount("A123", "Ali", 0);
Type t = typeof(BankAccount);
// account. Deposit (10);


Type[] parametersType = { typeof(decimal) };
MethodInfo method = t.GetMethod("Deposit");
method.Invoke( new object[] { 500m});

Console.WriteLine( account ) ;
```

### REFLECTING ASSEMBLIES

- First store the full path of `dll` file

use `\\` to escape `\`

```c#
var path = "a:\\b\\d\\z.dll";
```

or u can prefix string with `@`

```c#
var path = @"a:\b\d\z.dll";
```

- Then loadFile

```c#
var assembly = Assembly.LoadFile(path);
```

## 031 Attributes

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_031/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=33)

- Content

  - WHAT, WHY AND HOM
  - WHERE TO APPLY
  - COMMON ATTRIBUTES
  - CUSTOM ATTRIBUTES
  - ATTRIBUTES USAGE
  - REFLECTION AND ATTRIBUTES

### WHAT, WHY AND HOM

All attributes should inherits directly n indirectly from attribute class

We specify an attribute by placing it above the declaration for the element
between square brackets

```c#
  [Obsolete("Msg", false)]
  void SomethingMethod()
  {

  }
```

### WHERE TO APPLY

We specify an attribute by placing it above the declaration for the element between square brackets

U can treat them as methods and properties

By convention, all attribute names end with the word "attribute -
attribute

Attributes are assigned in in assembly at compile time but they
can be accessed at runtime using reflection

### COMMON ATTRIBUTES

- `ObsoleteAttribute`

  This attribute is attached to members that are not to be used any longer.

- `Flags`

  use with `enum` to make flags enum

- `DebuggerDisplay`

  To show custom string of class in debug mode

  ```c#
    [DebuggerDisplay("No: {no}, Title: {title}")]

    class Something
    {
        private int no;
        private int title;
    }
  ```

- `UsageAttribute`

  Make attribute for cretin target

  ```c#
  [UsageAttribute(AttributeTargets.Property)]
  class MyCustomAttribute : Attribute
  {

  }
  ```

  `AttributeTargets` is a flag enum

  `AllowMultiple` Ability to put multiple attributes above the target

  - Default value is: false

  ```c#
  [UsageAttribute(AttributeTargets.Property, AllowMultiple = true)]
  class MyCustomAttribute : Attribute
  {

  }
  ```

  `Inherited` Ability to inherit attributes

  - Default value is: false

### CUSTOM ATTRIBUTES

- Create class inherited from Attribute class
- Define properties that acts like metadata

### ATTRIBUTES USAGE

- Check Lesson Repo

### REFLECTION AND ATTRIBUTES

```c#
var ski11Attribute = prop.GetCustomAttribute<SkillAttribute>();
```

## 032 Lists And Dictionaries

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_032/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=34)

- Content
  - DEFINITIONS
  - ADD, INSERT AND REMOVE
  - COUNT AND CAPACITY
  - DICTIONARY<TKey, TValue>
  - ToDictionary()

### Criteria

- **Accessability**
- **Availability**

  Stay in memory

- **Storage Type**

  store contiguous or not

### CheckList

<div align= "center">

|                                 | List | Collection |
| ------------------------------- | ---- | ---------- |
| Discard After Processing        | ❌   | ❌         |
| Fast Removal/Retrieval          | ❌   | ❌         |
| Sequential Access               | ❌   | ❌         |
| Order Of Access                 | ❌   | ❌         |
| Random Access                   | ✔    | ✔          |
| Kept In Memory After Processing | ✔    | ✔          |
| Contiguous Memory               | ✔    | ✔          |

</div>

### DEFINITIONS

### LIST

#### Constructor

- Param Less

  ```c#
  List<T> myList = new List<T>();
  ```

- Control Initial Capacity

  ```c#
  List<T> myList = new List<T>(7); // Initial Capacity is 7
  ```

  The list will extend by the initial value u provided

#### Properties

- Count

  Count is the number of elements that are actually in the `List<T>`

  ```c#
  myList.Count;
  ```

- Capacity

  Capacity is the number of elements that the `List<T>` can store before resizing is required,

  capacity is always greater than or equal to count

  internally controlled from List class

  u can control initial capacity when u creating list

  ```c#
  myList.Count;
  ```

#### Methods

- Add() `o(1)` Performant

  ```c#
  myList.Add(T);
  ```

- AddRange() `o(1)` Performant

  ```c#
  myList.AddRange(T[]);
  ```

- Insert() `o(n)` Less Performant

  ```c#
  myList.Insert(index, T);
  ```

- InsertRange() `o(n)` Less Performant

  ```c#
  myList.InsertRange(index, T[]);
  ```

- RemoveAll(`<Predict>`)

  ```c#
  myList.RemoveAll(x => x == "");
  ```

- Remove(T)

  ```c#
  myList.Remove(T);
  ```

  To remove the passing T it should be a value not a new instance

  put if u want to pass new instance same with one in the list u must override hash code and equal methods in its class

- RemoveAt(index)
  ```c#
  myList.Remove(index);
  ```
- FirstOrDefault(Func)
  ```c#
  myList.FirstOrDefault(Func);
  ```

### DICTIONARY<TKey, TValue>

```c#
Dictionary<char, List<string>> lettersDictionary = new Dictionary<char, List<string>>()
```

#### Constructor

- Param Less

  ```c#
  Dictionary<char, List<string>> lettersDictionary = new Dictionary<char, List<string>>()
  ```

- Control Initial Capacity

  ```c#
  Dictionary<char, List<string>> lettersDictionary = new Dictionary<char, List<string>>(7) // Initial Capacity is 7
  ```

#### Properties

#### Methods

- ContainsKey(key)

  check dic if have cretin key

  ```c#
  lettersDictionary.ContainsKey(key);
  ```

- Add(key,value)

  ```c#
  lettersDictionary.Add(key,value);
  ```

- [key]

  access dic value by its key

  ```c#
  lettersDictionary[key];
  ```

### ToDictionary()

When you have list of items and want to convert it to dic and pair them with cretin property

`Using Linq`

- GroupBy

  ```c#
  list.GroupBy(Func);
  ```

- ToLookup

  return ILookup

  ```c#
  list.ToLookup(Func);
  ```

### Note

- `unchecked`

  to ignore overflow

  ```c#
    unchecked
    {

    }
  ```

- using `is null` than `== null`
- using `is not null` and newer `is {}`

- StringComparison

  ```c#
  this.Name.IsEquals(country.Name, StringComparison.OrdinalIgnoreCase);
  ```

- Char.ToLower(char)
- Nullable int `int?`
  - mean the default value will be null instead of 0 when using `int`
  - You can assign ull to this variable

## 033 Stack and Queue

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_033/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=35)

- Content
  - DEFINITION
  - STACK CONSTRUCTOR
  - STACK METHODS
  - STACK PROPERTIES
  - QUEUE CONSTRUCTOR
  - QUEUE METHODS
  - QUEUE PROPERTIES

### DEFINITION

### CheckList

<div align= "center">

|                                 | STACK | QUEUE |
| ------------------------------- | ----- | ----- |
| Discard After Processing        | ✔     | ✔     |
| Fast Removal/Retrieval          | ✔     | ✔     |
| Sequential Access               | ✔     | ✔     |
| Order Of Access                 | ✔     | ✔     |
| Random Access                   | ❌    | ❌    |
| Kept In Memory After Processing | ❌    | ❌    |
| Contiguous Memory               | ✔     | ✔     |

</div>

### STACK

`LIFO` Last in first out

- Example
  - History undo and redo
  - Browser Navigation back/forward

#### CONSTRUCTOR

- Param Less

  ```c#
  Stack<T> stack = new Stack<T>();
  ```

- IEnumerable

  ```c#
  Stack<T> stack = new Stack<T>(IEnumerable);
  ```

- Capacity

  ```c#
  Stack<T> stack = new Stack<T>(Capacity);
  ```

#### METHODS

- `Push`

  Add Item

  ```c#
  stack.Push(T);
  ```

- `Pop`

  Get last item and remove it

  ```c#
  stack.Pop();
  ```

- `Peek`

  Get last item without removing it

  keep item inside the memory and do whatever process you want and after finish processing we remove it manually using `pop` and this process known as `Two Phase Process`

  ```c#
  stack.Peek();
  ```

- `TryPeek` && `TryPop`

#### PROPERTIES

- `Count` the actual number of items

### QUEUE

`FIFO` First in first out

- Example
  - Printing

#### CONSTRUCTOR

- Param Less

  ```c#
  Queue<T> queue = new Queue<T>();
  ```

- IEnumerable

  ```c#
  Queue<T> queue = new Queue<T>(IEnumerable);
  ```

- Capacity

  ```c#
  Queue<T> queue = new Queue<T>(Capacity);
  ```

#### METHODS

- `Enqueue`

  Add new item

  ```c#
  queue.Enqueue(T);
  ```

- `Dequeue`

  Get first item and remove it

  ```c#
  queue.Dequeue();
  ```

- `Peek`

  Get first item without removing it

  ```c#
  queue.Peek();
  ```

- `TryPeek` && `TryDequeue`

#### PROPERTIES

### Note

There is two ways to deals with collections

- Generic

  Recommended from microsoft

- Non Generic

  Not recommended as it's expensive due to boxing and unboxing process

## 034 LinkedList HashSet SortedSet

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_034/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=36)

- Content

  - WHAT, WHY LINKED LIST
  - LINKED LIST NODE
  - REAL EXAMPLE LINKED LIST
  - HASH SET
  - SORTED LIST
  - COMPARISON AND EQUALITY

### CheckList

<div align= "center">

|                                 | LINKED LIST |
| ------------------------------- | ----------- |
| Discard After Processing        | ❌          |
| Fast Removal/Retrieval          | ✔           |
| Sequential Access               | ✔           |
| Order Of Access                 | ❌          |
| Random Access                   | ❌          |
| Kept In Memory After Processing | ✔           |
| Contiguous Memory               | ❌          |

</div>

### WHAT, WHY LINKED LIST

Consists of linked list node

- Example
  - Playlist

#### Property

- First

  Readonly

- Last

  Readonly

#### Constructor

- Param Less

  ```c#
  LinkedList<T> playlist = new LinkedList<T>();
  ```

- IEnumerable

  ```c#
  LinkedList<T> playlist = new LinkedList<T>(IEnumerable);
  ```

#### Method

- `AddFirst(T)`
  Either to add `T` directly or add `LinkedListNode`

- `AddLast(T)`
  Either to add `T` directly or add `LinkedListNode`

- `AddAfter(LinkedListNode, T)`
  Either to add `T` directly or add `LinkedListNode`

### LINKED LIST NODE

[`Previous`][`Item`][`Next`]

- If no `previous` return null
- If no `next` return null

### REAL EXAMPLE LINKED LIST

- Playlist
- Check Lesson Repo

### CheckList

<div align= "center">

|                                 | HASH SET | SORTED LIST |
| ------------------------------- | -------- | ----------- |
| Discard After Processing        | ❌       | ❌          |
| Fast Removal/Retrieval          | ✔        | ❌          |
| Sequential Access               | ❌       | ❌          |
| Order Of Access                 | ❌       | ❌          |
| Random Access                   | ✔        | ✔           |
| Kept In Memory After Processing | ✔        | ✔           |
| Contiguous Memory               | ✔        | ✔           |
| Contiguous Memory               | ✔        | ✔           |

</div>

### HASH SET

- Internally Hash table
- Hash based Lookups
- Stores Key Only
- No Duplication
- No Indexing

#### HASH SET `VS` Dictionary in store

- HASH SET: Only store the key
- Dictionary: Store both key and value

#### Method

- `UnionWith`

- `IntersectWith`

- `ExceptWith`

### SORTED LIST

- Internally Linear search
- No Duplication
- No Indexing
- Keeps elements in order
- Slower than hash set

#### Note

- It can sort primitive type like int, double ...
- If you want to sort ref type u should have a sort mechanism inherit `IComparable`

### COMPARISON AND EQUALITY

## 035 Stream I⧸O

- Data
  - [Github](https://github.com/metigator/CSharp_Lesson_035/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=37)
- Content

  - STREAM ARCHITECTURE
  - MANAGED / UNMANAGED CODE
  - FILE STREAM (BACK STORE)
  - STREAM READER/WRITER (ADAPTER)
  - DEFLATE STREAM (DECORATOR)
  - FILE CLASS

```
It's attention to detail that makes the difference between average and stunning

FRANCIS ATTERBURY
```

```
You can tell whether a man is clever by his answers. you can tell whether a man is wise by his questions

Naguib Mahfouz
```

### MANAGED / UNMANAGED CODE

#### MANAGED CODE

##### Flow

```
Flow Of Managed Code
ــــــــــــــــ
  |- Source Code
  |- Language Compiler
  |- Intermediate Language (IL)
  |- Common Language Runtime (CLR)
  |- Just In Time Compiler (JIT)
  |- Machine Code
```

CLR manage memory

#### UNMANAGED CODE

##### Flow

```
Flow Of Managed Code
ــــــــــــــــ
  |- Source Code
  |- Language Compiler
  |- Machine Code
```

### STREAM ARCHITECTURE

`System.IO`

- Divided into 3 parts

  - Back Store: Direct relation with external resources

    - File Stream
    - Network Stream

    These two deal with bytes so we have adapters

  - Adapters

    - Text Reader
    - Text Writer

    Return text to app but in back stage it deals with bytes

  - Decorator

    Transformation for content and change it

    it's not to change the representation

    - DeflateStream : Compress and Decompress the data

![](https://raw.githubusercontent.com/Courses-journey/dotnet/main/Metigator/01_mastering_csharp/assets/035_Stream.jpg)

### IDisposable

Any class that inherit from it is unmanaged code and you have to manually clean up

Like HttpClient

#### How to cleanup

- First inherit `IDisposable`
- Apply `Dispose()` method

```c#
public void Dispose()
{

}
```

- Make protected virtual `Dispose(bool disposing)` method

```c#
protected void Dispose(bool disposing)
{
  // Clean up code
}
```

disposing : `true` => dispose (managed + unmanaged)
disposing : `false` => dispose ( unmanaged + large fields)

when need to do dispose only one time

so we can add bool field to track that

```c#
private bool _disposed = false;

protected void Dispose(bool disposing)
{
  if(_disposed) return;

  // Clean up code
  if(disposing)
  {
    // dispose (managed + unmanaged)
  }

  // dispose ( unmanaged + large fields)
  // set large fields to null

  _disposed = true;
}

public void Dispose()
{
  Dispose(true);
}
```

#### Recommendation

- try/catch

  Recommended use dispose with try/catch and call `Dispose()` from finally

  ```c#
  CurrencyService currencyService = null;
  try
  {
    currencyService = new CurrencyService();
    var result = currencyService.GetCurrencies();
    Console.WriteLine(result);
  }
  catch(Ex)
  {

  }
  finally
  {
    currencyService?.Dispose();
  }
  ```

- using `.Net framework 2+`

  Highly recommended

  ```c#
  using (CurrencyService currencyService = new CurrencyService())
  {
    var result = currencyService.GetCurrencies();
    Console.WriteLine(result);
  }
  ```

  this code will be converted as same as try/catch method in the `IL` code

- using with no block `c# 8`

  ```c#
  using CurrencyService currencyService = new CurrencyService();
  var result = currencyService.GetCurrencies();
  Console.WriteLine(result);
  ```

#### What if user forgot to call `Dispose`?

We implement Dispose into class Finalizer

```c#
  ~IDisposable()
  {
    Dispose(false);
  }
```

- Q: Why using false?

  Answer: As the compiler reach finalizer that mean the managed code will be clean up using `GC` and we want to ensure that our unmanaged code will be clean up as well

```c#
class MyClass : IDisposable
{
  private bool _disposed = false;

  ~IDisposable()
  {
    Dispose(false);
  }

  protected void Dispose(bool disposing)
  {
    if(_disposed) return;

    // Clean up code
    if(disposing)
    {
      // dispose (managed + unmanaged)
    }

    // dispose ( unmanaged + large fields)
    // set large fields to null

    _disposed = true;
  }

  public void Dispose()
  {
    Dispose(true);
  }
}
```

what if the client was smart enough and call `Dispose()` then we don't need to call finalizer any more

to do that we call

```c#
  public void Dispose()
  {
    Dispose(true);
    GC.SuppressFinalizer(this);
  }
```

<!-- TODO Write Code -->

### FILE STREAM (BACK STORE)

```c#
  string path = @"path\a.txt";

  using(var fs = new FileStream(path, FileMode.Open, FileAccess.Write))
  {
    ///
  }
```

#### Properties

- `Length` size of file
- `Position` Position of cursor

#### Methods

### STREAM READER/WRITER (ADAPTER)

### FILE CLASS

### DEFLATE STREAM (DECORATOR)

## 036 Nuget Packages and Packaging

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_036/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=38)

- Content

  - DEFINITIONS
  - NUGET PACKAGE MANGER
  - INSTALL UNINSTALL PACKAGE IN VS
  - UPDATE NUGET PACKAGE IN VS
  - DEBUG VS. RELEASE MODE
  - PUBLISH A PACKAGE IN VS

### DEFINITIONS

The smallest unit of deployment Compiled output (dll/exe) + Metadata

### NUGET PACKAGE MANGER

Official Package manager for .NET Easy to share Packages

`Do not Re invent the wheel`

### INSTALL UNINSTALL PACKAGE IN VS

### UPDATE NUGET PACKAGE IN VS

### DEBUG VS. RELEASE MODE

- Preprocessor

```c#
  #if DEBUG
  // Code that will run in debug mode only
  #endif
```

- debug => for development

  preprocessor debug code + stack trace

- release =>for production

  preprocessor debug code removed + performance + no stack trace

### PUBLISH A PACKAGE IN VS

- RMB `Right Mouse Button` on the package project
- Click Pack
- `..\ProjectFolder\bin\Release\**.nupkg`
- Go to `nuget.org`

## 037 Threading

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_037/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=39)

- Content

  - PROCESS VS THREAD
  - START AND JOIN THREAD
  - MULTI THREADING
  - RACE CONDITION
  - DEADLOCK
  - THREAD POOL

### Introduction

Application starts on windows => a process id is created CLR creates a single thread to execute code design

- `Thread`

  Is the basic to which the operation system allocates processor time

- Process can have one or more thread

- `Thread Scheduler`

  Scheduler is responsible for scheduling threads on processors

- `Thread.Sleep(mills)`

  method can be used to pause the execution of current thread for specified time in milliseconds

- Naming Thread

  It's useful to name you thread

  Naming Thread Helps in debugging and Tracing

  `Debug -> windows -> Threads`

  ```c#
  Thread.CurrentThread.Name = "Name";
  ```

### Foreground vs Background Thread

- Foreground thread

  They keep the application alive for as long as any one of them is running

- Background threads / Daemon Process

  - Which don't keep the application alive on their own

  - Terminating immediately onc all foreground threads have ended
  - Killed by OS

TO check whether it's background or not

```c#
thread.IsBackground
```

### PROCESS VS THREAD

### START AND JOIN THREAD

#### Start thread

```c#
Thread t1 = new Thread(wallet.RunRandomTransaction);
t1.Name = "T1";
t1.Start();


// TO get thread state
// t1.ThreadState
```

Another way

```c#
Thread t2 = new Thread(new ThreadStart(wallet.RunRandomTransaction));
t2.Name = "T2";
t2.Start();
```

#### Function with argument

If your function need argument then u can define with lambda

```c#
Thread t2 = new Thread(()=> wallet.debit(50));
t2.Name = "T2";
t2.Start();
```

#### Join

allows one thread to wait for the completion of another

```c#
Thread t1 = new Thread(wallet.RunRandomTransaction);
t1.Name = "T1";
t1.Start();

t1.Join(); // Wait t1 to complete

Thread t2 = new Thread(new ThreadStart(wallet.RunRandomTransaction));
t2.Name = "T2";
t2.Start();
```

- When to use?

  If u want the result from `thread 1` to start `thread 2` for example

### MULTI THREADING

They do run in parallel

- Perhaps they are too short and accidentally finish too fast
- Thread scheduler control which thread to start

If one thread happens to finish before the scheduler
decides it's time to run the other thread

### RACE CONDITION

Race Condition is a scenario where the outcome of the program is affected because of timing

#### How to avoid?

We can avoid race condition using lock which will make our logic accessible to only one thread at the same time when the first finish the next one can enter

Any code that may cause racing condition wrap it into lock

```c#
lock (<Any Reference type>)
{
  // Our logic
}
```

Example

```c#
  private readonly object bitLock

  void Debit(decimal value)
  {
    lock (bitLock)
    {
      // Our logic
    }
  }
```

### DEADLOCK

Is a situation where two or more threads are frozen in their execution because they are waiting for each other to finish

#### How to avoid?

- Order of operations

  We cam for example compare objects id and make the first

- Using `Monitor` class

  U can use `Monitor.TryEnter` instead of `lock`

  ```c#
    if(Monitor.TryEnter(from, 1000))
    {

    }
    else
    {
      // unable to enter
    }
  ```

  used with try/catch/finally `Monitor.Exit(object)` to free the object after finishing

  ```c#
    if(Monitor.TryEnter(from, 1000))
    {
        try
        {
            // COde
        }
        catch
        {

        }
        finally
        {
            Monitor.Exit(from);
        }
    }
    else
    {
      // unable to enter
    }
  ```

### THREAD POOL

Pool of pre created recyclable threads

- You can not name a thread

- Pooled Thread always background

- Ideal for short running process

#### why?

- Thread has overhead in time and memory
- helps mitigate the issue of performance by reducing the number of threads

#### How?

- First Way

```c#
ThreadPool.QueueWorkItem(new WaitCallback(delegateThatTakeObject));
```

- Second Way

```c#
Task.Run(delegateThatTakeNoArgument)
```

### NOte

- `Manager Class`

  Used to manage a set of objects of another class

## 038 Asynchronous Programming

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_038/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=40)

- Content

  - THREAD VS TASKS
  - HOW TO IMPLEMENT
  - ASYNCHRONOUS VS SYNCHRONOUS
  - ASYNCHRONOUS FUNCTION
  - CANCELLATION TOKEN
  - REPORTING A PROGRESS
  - CONCURRENCY VS PARALLELISM

### THREAD VS TASKS

<div align="center">

| CRITERIA               | THREAD                  | TASK        | Advantages          |
| ---------------------- | ----------------------- | ----------- | ------------------- |
| Concept                | Low Level               | Abstraction | Less Details        |
| Leveraging Thread Pool | ❌                      | ✔           | Performance         |
| Return Value           | ❌                      | ✔           | Less Code           |
| Chaining               | ❌                      | ✔           | Order / Readability |
| Exception Propagation  | ❌                      | ✔           | Parent Catch It     |
| Task Type              | Foreground / Background | Background  | Process Termination |
| Support Cancellation   | ❌                      | ✔           | Save Resources      |

</div>

### Return Value

There is two type of task generic and non generic

To return result we use generic and specify the type we want to return

```c#
Task<string> task = Task.Run(() =>
  {
      Thread.Sleep(2000);

      return "Done!";
  });

Console.WriteLine("Print Directly");

/// ********************
/// Out put
/// ********************
// Print Directly
```

To receive the result we call `Result`

```c#
Task<string> task = Task.Run(() =>
  {
      Thread.Sleep(2000);

      return "Done!";
  });


Console.WriteLine(task.Result);
Console.WriteLine("Print Directly");

/// ********************
/// Out put
/// ********************
/// The app will await 2 seconds then will print
// Done!
// Print Directly
```

Calling `Result` will block the thread

We have another way to make that

```c#
task.GetAwaiter().GetResult();
```

#### Thread block

we mean that the method (operation) that the thread calls, put or take, is blocking the thread from proceeding to execute the next line of code

### Long Running Task

You can distinguish short-running and long-running

The comparison between their start-up time and run time

- start up time: Thread require (memory + cpu time) to start
  - start time < execution time : short running -> use Thread pool
  - start time > execution time : long running -> don't use se thread pool

To Create long running task

```c#
var task = Task.Factory.StartNew(()=> RunLongTask(), TaskCreationOptions.LongRunning)
```

### HOW TO IMPLEMENT

### Handling exception | Thread vs Task

- An exception propagates from method to method, up the call stack, until it's caught
- The thread that have the exception have the responsibility to handle and catch it
- It's difficult to propagate the exception from thread to do that we need to use task

### Task Continuation

- Using `Result`

  ```c#
  Task<int> task = Task.Run(()=> CountPrimeNumberInARange(2, 3_000_000));
  Console.WriteLine(task.Result); // bad it blocks the thead
  ```

  we can use this with task that take short time to complete

- Using `Awaiter` `OnComplete`

  ```c#
  Task<int> task = Task.Run(()=> CountPrimeNumberInARange(2, 3_000_000));
  var awaiter = task.GetAwaiter();
  awaiter.OnComplete(()=>{
    Console.WriteLine(awaiter.GetResult()); // it block the thread but task is completed
  });
  ```

- Using `ContinueWith`

  ```c#
  Task<int> task = Task.Run(()=> CountPrimeNumberInARange(2, 3_000_000));
  task.ContinueWith((x)=> Console.WriteLine(x.Result));
  ```

### Task Delay

- `Task.Delay()`

  Make a logical delay without blocking the parent thread

- `Thread.Sleep()`

  Block the thread for specific time

### ASYNCHRONOUS VS SYNCHRONOUS

#### SYNCHRONOUS

A SYNCHRONOUS OPERATION DOES ITS WORK BEFORE Returning TO THE CALLER

#### ASYNCHRONOUS

AN ASYNCHRONOUS OPERATION CAN DO (MOST OR ALL OF) LTS WORK AFTER Returning TO THE CALLER

### ASYNCHRONOUS FUNCTION

- From DotNet 3.5

- Old way

  ```c#

  static void Main(string[] args)
  {
    var task = Task. Run(() => ReadContent("https:/(www.youtube.com/c/Metigator"));
    var awaiter = task.GetAwaiter();
    awaiter.OnCompleted(() Console. WriteLine(awaiter.GetResult()));
    Console.ReadKey();
  }

  static Task<string> ReadContent(string url)
  {
    var client = new HttpClient();
    var task = client.GetStringAsync(ur1);
    return task;
  }
  ```

- `async` `await` created to simplify attaching the continuation task
- Impl

  - To make an async function we put `async` keyword in function signature
  - Also it's recommended to make function name end with async
  - when we do that the function become an object with its state machine to track progress
  - `await` dose not block the thread unlike `.Wait`

- `Task<T>` is a promise to return T value

```c#
  static async Task<string> ReadContentAsync(string url)
  {
    var client = new HttpClient();
    var content = await client.GetStringAsync(url);
    // content now is a string not a task
    return content;
  }
```

- in c# 6 `Main` function can be marked as `async`
  - before that u can use task run

### CANCELLATION TOKEN

The ability to cancel any task at anytime

- In Thread u have to make your custom solution
- In Task there is a `cancellation Token` cancel the request all the way from bottom to the top

```c#
CancellationTokenSource cancellationTokenSource = new CancellationTokenSource();
```

- Common use in `ASP` `WPF` or any UI Framework

- `CancellationTokenSource` apply `IDisposable`

  - So we have to Dispose it
  - in UI Frameworks the base classes which views inherits from make this for us
  - but if u use it with console app u have to do it on your own

- To check if cancel requested

  ```c#
    bool isCancelled = cancellationTokenSource.Token.IsCancellationRequested
  ```

- U can pass `CancellationToken` to any async function like `delay`
  - we pass `token` of `CancellationTokenSource`
  ```c#
  Task.Delay(5000, cancellationTokenSource.Token);
  ```

### REPORTING A PROGRESS

Using Action Delegate

### Combinator

```c#
static Task<string> Has1000Subscriber()
{
    Task.Delay(4000).Wait();
    return Task.FromResult("congratulation !! you have 1000 subscribers");
}

static Task<string> Has4000ViewHours()
{
    Task.Delay(3000).Wait();
    return Task.FromResult("congratulation !! you have 4000 view hours");
}
```

- `Task.WhenAny`
  - Any task who end first will be the result

```c#
static async Task Main(string[] args)
{
    var has1000SubscriberTask = Task.Run(() => Has1000Subscriber());
    var has4000ViewHoursTask = Task.Run(() => Has4000ViewHours());
    Console.WriteLine("Using WhenAny()");
    Console.WriteLine("---------------");

    var any = await Task.WhenAny(has1000SubscriberTask, has4000ViewHoursTask);
    Console.WriteLine(any.Result);

    Console.ReadKey();
}
```

- `Task.WhenAll`
  - return array of tasks
  - all task has to complete
  - put in try catch

```c#
static async Task Main(string[] args)
{
    var has1000SubscriberTask = Task.Run(() => Has1000Subscriber());
    var has4000ViewHoursTask = Task.Run(() => Has4000ViewHours());

    var all = await Task.WhenAll(has1000SubscriberTask, has4000ViewHoursTask);
    foreach (var t in all)
    {
        Console.WriteLine(t);

    }
    Console.ReadKey();
}
```

### Async Pattern

- Returns a `Task` or `Task<T>` -- always
- Has an "async suffix -- except/task combinator
- Cancellation and/or progress reporting
- Returns quickly to the caller synchronous phase
- Does not tie up a thread if `I/O-bound` "such as networking or file system reading"

### CONCURRENCY VS PARALLELISM

- CONCURRENCY

  - Is when two tasks can start. Run and complete in overlapping time periods

```c#
static Task ProcessThingsInConcurrent(IEnumerable<DailyDuty> things)
{
    foreach (var thing in things)
    {
        thing.Process();
    }
    return Task.CompletedTask;
}
```

- PARALLELISM
  - parallelism is when tasks literally run at the same time (EG. on a multi-core processor)

```c#
static Task ProcessThingsInParallel(IEnumerable<DailyDuty> things)
{
    Parallel.ForEach(things, thing => thing.Process());
    return Task.CompletedTask;
}
```

### Note

## 039 Serialization

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_039/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=40)

- Content

  - WHAT, WHY
  - WHAT is XML, Json
  - BINARY SERIALIZATION
  - XML SERIALIZATION
  - JSON SERIALIZATION
  - JSON AND HTTPClient

### WHAT, WHY

- What
  - **Serialization** is the process of converting the state of an object into a form that can be persisted or transported. (memory, file or database)
  - **Deserialization** is recreate the object from the serialized format

### WHAT is XML, Json

- `Json` Javascript object notation
- `XML` Extensible Markup Language

- C# Object

  ```c#
  public class Employee
  {
    public int Id { get; set; }

    public string FName { get; set};

    public string LName { get; set};

    public List<string> Benefits { get; set; } = new List<string>();
  }
  ```

Object Instance

```c#
Employee el = new Employee
{
  ld = 100,
  FName = "Issam"
  LName = "A." ,
  Benefits = {
  " Pension",
  "Health Insurance"
  }
}
```

Instance XML

```xml
<Employee>
    <Id>100</Id>
    <FirstName>Issam</FirstName>
    <LastName>A.</LastName>
    <Benefits>
        <string>Pension</string>
        <string>Health Insurance</string>
    </Benefits>
</Employee>
```

Instance Json

```json
{
  "Id": 100,
  "FirstName": "Issam",
  "LastName": "A.",
  "Benefits": ["Pension", "Health Insurance"]
}
```

| XML                       | JSON                        | BINARY                            |
| ------------------------- | --------------------------- | --------------------------------- |
| Human Readable            | Human Readable              | Not Human Readable                |
| Array Concept Not Declare | Array Concept               | Support Complex Object (circular) |
| Difficult To Parse        | JavaScript Can Parse It     | -                                 |
| -                         | Code Like                   | -                                 |
| -                         | Shorten and Faster Than XML | -                                 |
| -                         | -                           | Not portable                      |
| -                         | -                           | Can Be Dangerous                  |

### XML SERIALIZATION

```c#
private static string SerializeToXmlString(Employee e1)
{
    var result = "";
    var xmlSerializer = new XmlSerializer(e1.GetType());
    using (var sw = new StringWriter())
    {
        using (var writer = XmlWriter.Create(sw, new XmlWriterSettings { Indent = false }))
        {
            xmlSerializer.Serialize(writer, e1);
            result = sw.ToString();
        }
    }
    return result;
}
```

```c#
private static Employee DeserializeFromXmlString(string xmlContent)
{
    Employee employee = null;
    var xmlSerializer = new XmlSerializer(typeof(Employee));
    using (TextReader reader = new StringReader(xmlContent))
    {
        // Remember that cast with as is safe as it will return null if an exception happened
        employee = xmlSerializer.Deserialize(reader) as Employee;
    }
    return employee;
}
```

```c#
static void Main(string[] args)
{
    var e1 = new Employee {
        Id = 1001,
        Fname = "Issam",
        Lname = "A.",
        Benefits = { "Pension",  "Health Insurance" }
    };

    var xmlContent = SerializeToXmlString(e1);
    Console.WriteLine(xmlContent);
    // Remember Files without specific path created in app dir
    File.WriteAllText("xmlDocument.xml", xmlContent);

    var xmlContent2 = File.ReadAllText("xmlDocument.xml");
    Employee e2 = DeserializeFromXmlString(xmlContent2);

    Console.ReadKey();
}
```

### BINARY SERIALIZATION

- Class must be mark as `[Serializable]`
- U can mark any property in this class as `[NonSerialized]` if u don't want to serialize it

```c#
private static string NonSerializeToBinaryString(Employee employee)
{
    using(var stream = new MemoryStream())
    {
        var binaryFormatter = new BinaryFormatter();
        binaryFormatter.Serialize(stream, employee);
        stream.Flush();
        stream.Position = 0;
        return Convert.ToBase64String(stream.ToArray());
    }
}
```

```c#
private static Employee DeserializeFromBinaryContent(string binaryContent)
{
    byte[] bytes = Convert.FromBase64String(binaryContent);
    using(var stream = new MemoryStream (bytes))
    {
        var binaryFormatter = new BinaryFormatter();
        stream.Seek(0, SeekOrigin.Begin);
        return binaryFormatter.Deserialize(stream) as Employee;

    }
}
```

```c#
static void Main(string[] args)
{
    var e1 = new Employee
    {
        Id = 1001,
        Fname = "Issam",
        Lname = "A.",
        Benefits = { "Pension", "Health Insurance" }
    };

    string binaryContent = NonSerializeToBinaryString(e1);
    Console.WriteLine(binaryContent);

    Employee e2 = DeserializeFromBinaryContent(binaryContent);
    Console.ReadKey();
}
```

### JSON SERIALIZATION

- Old way is use third part library `Newtonsoft.Json` used until today
- until .Net 3 Microsoft add `Json.Net`

#### Newtonsoft.Json

```c#
static string SerializeToJsonStringUsingNewSoftJson(Employee employee)
{
    var result = "";
    result = JsonConvert.SerializeObject(employee , Formatting.Indented);

    return result;
}
```

```c#
static Employee DeserializeToJsonStringNewSoftJson(string jsonContent)
{
    Employee employee = null ;
    employee = JsonConvert.DeserializeObject<Employee>(jsonContent);
    return employee;
}
```

#### Json.Net

```c#
static string SerializeToJsonStringUsingJSONNET(Employee employee)
{
    var result = "";
    result =  System.Text.Json.JsonSerializer.Serialize(employee,
        new JsonSerializerOptions { WriteIndented = true });

    return result;
}
```

```c#
static Employee DeserializeToJsonStringJSONNET(string jsonContent)
{
    Employee employee = null;
    employee = JsonConvert.DeserializeObject<Employee>(jsonContent);
    return employee;
}
```

### JSON AND HTTPClient

- Create the class that handle the incoming json

  - DO it manually
  - In Visual Studio u can generate it automatically using `Edit -> Paste Special -> Paste Json as  Classes`

```c#
public class Todo
{
    public int Id { get; set; }
    public int UserId { get; set; }
    public string Title { get; set; }
    public bool Completed { get; set; }


    public override string ToString()
    {
        return $"\n [{Id} - UserId: {UserId}] -  {Title} {(Completed ? "completed" : "not completed")}";
    }
}
```

- It's recommended to make `HttpClient` shared in the class

```c#
class Program
{
    private readonly static HttpClient httpClient = new HttpClient();
    static async Task Main(string[] args)
    {

    }
}
```

```c#
static async Task Main(string[] args)
{
    var todoesJsonContent = await httpClient.GetStringAsync("https://jsonplaceholder.typicode.com/todos");

    var todoes = JsonSerializer.Deserialize<List<Todo>>(todoesJsonContent
        , new JsonSerializerOptions {PropertyNameCaseInsensitive = true });

    foreach (var item in todoes)
        Console.WriteLine(item);

    Console.ReadKey();
}
```

### Note

#### Marshal by Reference or MarshalByRefObject

`Note: This answer from GPT`

In .NET. `MarshalByRefObject` is a class that can be used to create remote objects, allowing two applications to communicate by invoking methods on objects residing in different application domains or even on different machines in a distributed environment.

- App01

```c#
using System;
using System.Runtime.Remoting;
using System.Runtime.Remoting.Channels;
using System.Runtime.Remoting.Channels.Tcp;

public class RemoteObject : MarshalByRefObject
{
    public string SayHello()
    {
        return "Hello from Application 1 (Server)!";
    }
}

class Program
{
    static void Main()
    {
        TcpChannel channel = new TcpChannel(12345); // Specify a port number for communication
        ChannelServices.RegisterChannel(channel, false);

        RemotingConfiguration.RegisterWellKnownServiceType(
            typeof(RemoteObject),
            "RemoteObject",
            WellKnownObjectMode.Singleton
        );

        Console.WriteLine("Server is ready. Press Enter to exit.");
        Console.ReadLine();
    }
}

```

- App02

```c#
using System;
using System.Runtime.Remoting;
using System.Runtime.Remoting.Channels;
using System.Runtime.Remoting.Channels.Tcp;

class Program
{
    static void Main()
    {
        TcpChannel channel = new TcpChannel();
        ChannelServices.RegisterChannel(channel, false);

        RemoteObject remoteObject = (RemoteObject)Activator.GetObject(
            typeof(RemoteObject),
            "tcp://localhost:12345/RemoteObject"
        );

        if (remoteObject != null)
        {
            string message = remoteObject.SayHello();
            Console.WriteLine("Message from Server: " + message);
        }
        else
        {
            Console.WriteLine("Failed to connect to the remote object.");
        }

        Console.WriteLine("Press Enter to exit.");
        Console.ReadLine();
    }
}
```

- In this example:

  - Application 1 (Server) creates a remote object `RemoteObject` that derives from `MarshalByRefObject`. It registers this object as a well-known service type with a given name and listens on a specified port.

  - Application 2 (Client) registers a channel for communication, then connects to the remote object hosted by Application 1 using the URL `tcp://localhost:12345/RemoteObject`. It then invokes the `SayHello` method on the remote object.

  - Make sure to run Application 1 (Server) before running Application 2 (Client). When you run the client, it will communicate with the server application and display the message received from the remote object.

- Note

  - The technique of using "MarshalByRefObject" and .NET Remoting for remote object communication in the .NET Framework was developed by Microsoft. .NET Remoting was introduced as a technology for building distributed applications in the early versions of the .NET Framework, specifically in .NET Framework 1.0 and 1.1.

  - .NET Remoting allowed developers to create distributed applications by enabling objects in one application domain to interact with objects in another application domain, even across different processes or machines. It provided a way to pass objects by reference between application domains, using the "MarshalByRefObject" base class to facilitate this remote communication.

  - Please note that .NET Remoting has been largely replaced by more modern communication technologies in recent versions of the .NET Framework, such as Windows Communication Foundation (WCF) and ASP.NET Web API (now part of ASP.NET Core). These technologies provide more flexibility and are better suited for building distributed and web-based applications.

## 040 Foreach / Yield Deep Dive

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_040/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=41)

- Content
  - `IEnumerable` | `IEnumerable<T>` | `IEnumerator` | `IEnumerator<T>`
  - foreach
  - yield

### `IEnumerable` | `IEnumerable<T>` | `IEnumerator` | `IEnumerator<T>`

- Any Collection in c# extend `IEnumerable` or `IEnumerable<T>`
- Then we have `IEnumerator` and `IEnumerator<T>`
- `IEnumerator<T>` have `IDisposable` to release resource

In C#, collections often implement either `IEnumerable` or `IEnumerable<T>`, depending on whether they are non-generic or generic collections, respectively. These interfaces allow you to iterate over the elements in the collection using a foreach loop or other iteration methods.

- `IEnumerable`:
  Represents a non-generic collection of objects that can be enumerated.
  It provides a non-generic `GetEnumerator` method that returns an `IEnumerator` interface for iterating through the collection.
  Elements retrieved from an `IEnumerable` collection must be cast to their actual data types.

- `IEnumerable<T>`:
  Represents a generic collection of objects that can be enumerated.
  It provides a generic `GetEnumerator` method that returns an `IEnumerator<T>` interface for iterating through the collection.
  Elements retrieved from an `IEnumerable<T>` collection are of the specified type without the need for casting.

- `IEnumerator`:
  Represents an enumerator for a non-generic collection.
  It provides methods such as `MoveNext`, `Reset`, and a `Current` property for iterating through the elements of a collection.
  The `Current` property returns an `object`, so casting may be required to access the actual element.

- `IEnumerator<T>`:
  Represents an enumerator for a generic collection.
  It provides methods such as MoveNext, Reset, and a Current property for iterating through the elements of a collection.
  The Current property returns the element of type T directly, so casting is not necessary.

- `IDisposable`:
  Represents a mechanism for releasing unmanaged resources.
  `IEnumerator<T>` implements `IDisposable` to allow you to explicitly release any resources held by the enumerator, such as file handles or network connections, when you are done with it. It's used to ensure proper resource cleanup.

When iterating over collections that implement IEnumerator<T> and use IDisposable, it's a good practice to use the using statement to ensure that the enumerator's resources are properly released after the enumeration is complete

### foreach

When you use `foreach` in your C# code, the C# compiler generates code that uses `IEnumerator` or `IEnumerator<T>` under the hood to iterate over collections. This generated code is part of the compiled assembly (IL or Intermediate Language code) and is executed by the CLR.

```c#
  var numbers = new [] {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};

  Console.WriteLine("\n\n Using Foreach");
  foreach (var n in numbers)
  {
      Console.Write($" {n}");
  }
```

- Code generated under the hood

```c#
static void Foreach<T> (IEnumerable<T> source)
{
    IEnumerator<T> enumerator = source.GetEnumerator();
    IDisposable disposable;
    try
    {
        T item;
        while (enumerator.MoveNext())
        {
            // code
            item = enumerator.Current;
            Console.Write($" {item}");
        }
    }
    finally
    {
        disposable = (IDisposable)enumerator;
        disposable.Dispose();
    }
}
```

```c#
  var numbers = new [] {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
  Foreach(numbers);
```

- u can for example use action to pass what to do on every item

```c#
static void Foreach<T> (IEnumerable<T> source, Action<T> action)
{
    IEnumerator<T> enumerator = source.GetEnumerator();
    IDisposable disposable;
    try
    {
        T item;
        while (enumerator.MoveNext())
        {
            // code
            item = enumerator.Current;
            action(item);
        }
    }
    finally
    {
        disposable = (IDisposable)enumerator;
        disposable.Dispose();
    }
}
```

```c#
  var numbers = new [] {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
 Foreach(numbers,num => Console.Write($" {num}"));
```

#### foreach vs for

- When u have array use `for`
- When u have collection use `foreach` specially with linq

### yield

- After .Net framework 2
- Before that u have to implement class with state machine
- Signal the compiler the block in which it appears is an iterator block

```c#
static IEnumerable<int> GenerateV1()
{
    var result = new List<int>();
    for (int i = 1; i <= 5; i++)
    {
        result.Add(i);
    }
    return result;
}
```

Notice that with yield I return is a single item

```c#
static IEnumerable<int> GenerateV1()
{
    var result = new List<int>();
    for (int i = 1; i <= 5; i++)
    {
        yield return i;
    }
}
```

Also remember that any code after `return` keyword is a dead code

but with `yield` u can return as many u want

like `return` any code after `yield break` will be unreachable code

```c#
static IEnumerable<int> GenerateV1()
{
    yield return 1;
    yield return 2;
    yield return 3;
    yield return 4;
    yield break;
    yield return 5; // won't be return
    yield return 6; // ..
}
```

U can see clearly that items return one by one

```c#
static void Main(string[] args)
{
    foreach (var item in GenerateV1())
    {
    Console.WriteLine(item);
    }
    Console.ReadKey();
}

static IEnumerable<int> GenerateV1()
{
    yield return 1;
    Thread.Sleep(1000);
    yield return 2;
    Thread.Sleep(1000);
    yield return 3;
    Thread.Sleep(1000);
    yield return 4;
}
```

When we call methods with `yield` keyword an `Enumerator` start an call `moveNext` until it reach `yield` keyword then the value with the `yield` become our `currentValue` then it return it to the `caller`

After that `Enumerator` continue code after the last `yield` and repeat the process until there is no `yield` or there is `yield break`

#### Usage

- inside method
- get accessor in property
- operator overloading

- cannot use in anonymous method

## 041 Records

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_041/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=42)

- Content

  - Reference Vs. Value based Equality
  - Object hash code
  - Override Equals

- 2020 `c# 9.0` Record Reference Type
- 2021 `c# 10.0` Record Value Type using record struct

### Reference Vs. Value based Equality

#### Value based

- Like numeric data types
- Also struct

Two objects are considered equal if their content is the same, regardless of whether they are separate instances in memory.

```c#
struct Point
{
  public int X;
  public int Y;

  public Point(int x, int y)
  {
      X = x;
      Y = y;
  }
}
```

```c#
static void Main(string[] args)
{
  var p1 = new Point(2, 3);
  var p2 = new Point(2, 3);

  Console.WriteLine($"p1: ({p1.X}, {p1.Y})"); // p1: (2, 3)
  Console.WriteLine($"p2: ({p2.X}, {p2.Y})");

  Console.WriteLine($"p1.Equals(p2) = {p1.Equals(p2)}"); // True

  Console.ReadKey();
}
```

#### Reference based

In reference-based equality, two objects are considered equal if they reference the same memory location or object in memory. In other words, they are the same instance in memory.

```c#
class Point
{
    public int X;
    public int Y;

    public Point(int x, int y)
    {
        X = x;
        Y = y;
    }
}
```

```c#
static void Main(string[] args)
{
    var p1 = new Point(2, 3);
    var p2 = new Point(2, 3);

    Console.WriteLine($"p1: ({p1.X}, {p1.Y})"); // p1: (2, 3)
    Console.WriteLine($"p2: ({p2.X}, {p2.Y})");

    Console.WriteLine($"p1.Equals(p2) = {p1.Equals(p2)}");    // False
    Console.WriteLine($"Object.ReferenceEquals(p1, p2) =" +
        $"{Object.ReferenceEquals(p1, p2)}");                 // False

    p1 = p2;

    Console.WriteLine($"p1.Equals(p2) = {p1.Equals(p2)}");    // False
    Console.WriteLine($"Object.ReferenceEquals(p1, p2) =" +
        $"{Object.ReferenceEquals(p1, p2)}");                 // True

    Console.ReadKey();
}
```

### Object hash code

`Object.GetHashCode()`

Default Behavior: The default implementation of `GetHashCode` in the Object class generates a hash code based on the object's reference in memory.

In other words, objects that occupy different memory locations will have different hash codes, even if their content is identical.

- Value type will have same HashCode if they have identical content

```c#
class Employee
{
    public int Id { get; set; }
    public string Name { get; set; }
}
```

```c#
struct Customer
{
    public int Id { get; set; }
    public string Name { get; set; }
}
```

```c#
static void Main(string[] args)
{
    var e1 = new Employee { Id = 100, Name = "Issam" };
    var e2 = new Employee { Id = 100, Name = "Issam" };
    Console.WriteLine($"e1.GetHashCode() = {e1.GetHashCode()}"); // Different HashCode as Object is ref type
    Console.WriteLine($"e2.GetHashCode() = {e2.GetHashCode()}"); // Different HashCode as Object is ref type

    var c1 = new Customer { Id = 100, Name = "Issam" };
    var c2 = new Customer { Id = 100, Name = "Issam" };
    Console.WriteLine($"c1.GetHashCode() = {c1.GetHashCode()}");  // Identical HashCode as struct is value type
    Console.WriteLine($"c2.GetHashCode() = {c2.GetHashCode()}");  // Identical HashCode as struct is value type

    Console.WriteLine(100.GetHashCode());

    Console.ReadKey();
}
```

### Override Equals

Override to make any ref type that have same content to be equal

```c#
public override bool Equals(object obj)
  {
    Point p = obj as Point;
    if (p is null)  return false;
    return p.X == X && p.Y == Y;
  }
```

### Override HashCode

```c#
public override int GetHashCode()
{
  int hash  = 13;
  hash  = hash * 7 + X.GetHashCode();
  hash  = hash * 7 + Y.GetHashCode();
  return hash;
}
```

There is a simple way in new framework

```c#
public override int GetHashCode()
{
  return HashCode.Combine(X,Y);
}
```

- Always use variable that u use in equality in hashCode

- Casting from value type to ref type requires converting vars from Heap to Stack

### IEquatable interface

```c#
class Point: IEquatable<Point>
{
    public int X;
    public int Y;

    public Point(int x, int y)
    {
        X = x;
        Y = y;
    }

    public override bool Equals(Object obj)
    {
      Point p = obj as Point;
      return this.Equals(p);
    }

    public bool Equals(Point other)
    {
      if (p is null)  return false;
      return p.X == X && p.Y == Y;
    }
}
```

`IEquatable` recommended to use in struct to avoid casting and increase performance

### Override Operators

```c#
class Point: IEquatable<Point>
{
    public int X;
    public int Y;

    public Point(int x, int y)
    {
        X = x;
        Y = y;
    }

    public override bool Equals(Object obj)
    {
      Point p = obj as Point;
      return this.Equals(p);
    }

    public bool Equals(Point other)
    {
      if (p is null)  return false;
      return p.X == X && p.Y == Y;
    }

    public static bool operator ==(Point lhs, Point rhs)
    {
      if (lhs is null)
      {
        if (rhs is null)
        {
          return true;
        }
        return false;
      }

      return lhs.Equals(rhs);
    }

    public static bool operator !=(Point lhs, Point rhs)
    {
      return !(lhs == rhs);
    }
}
```

when u override `==` u have to override `!=` also

### Init only setters

`Immutability` make sure that object won't change after initialization

- How to achieve?

  - we can achieve that by making class property `{get;}` this way we initializing the object and try to assign values to that property it will complains

    ```c#
    static void Main(string[] args)
    {
      var p1 = new Point(2,3);
      p1.X = 5; //error
      var p2 = new Point
      {
        X = 2,
        Y=3
      }  //error
    }

    class Point: IEquatable<Point>
    {
        public int X {get;};
        public int Y {get;};

        public Point(int x, int y)
        {
            X = x;
            Y = y;
        }

        public Point()
        {
        }

        ...
    }
    ```

  - `c# 9` u can use `init` which mean u can initialize object only onetime in object initializer and the object will be immutable

    ```c#
    static void Main(string[] args)
    {
      var p1 = new Point
      {
        X = 5,
        Y = 6,
      };

      Console.ReadKey();
    }

    class Point : IEquatable<Point>
    {
      public int X { get; init; }
      public int Y { get; init; }

      public Point() { }

      ...
    }
    ```

### Override ToString()

```c#
  class Point : IEquatable<Point>
  {
    public int X { get; init; }
    public int Y { get; init; }

    public Point() { }

    public override string ToString()
    {
      return $"{{X:{X}, Y:{Y}}}";
    }
  }
```

### Record

new reference type in c# 10

- override object `equal`
- implement `IEquatable <Point>`
- override object GetHashCode
- override `==` , `!=`
- override `ToString()`;

```c#
  record Point
  {
    public int X ;
    public int Y ;
  }
```

```c#
    static void Main(string[] args)
    {
      var p1 = new Point
      {
        X = 5,
        Y = 6,
      };

      Console.ReadKey();
    }
```

and u can use constructors

```c#
  record Point
  {
    public Point(int x, int y)
    {
      X = x;
      Y = y;
    }
    public int X ;
    public int Y ;
  }
```

```c#
    static void Main(string[] args)
    {
      var p1 = new Point(5,6);

      Console.ReadKey();
    }
```

### Immutable Record

By default record is mutable

How to make it immutable

- using `{get;}`
- or using `init` with param less constructor

```c#
  record Point
  {
    public int X {get; init;};
    public int Y {get; init;};
    public Point()
    {
    }
    public Point(int x, int y)
    {
      X = x;
      Y = y;
    }
  }
```

```c#
    static void Main(string[] args)
    {
      var p1 = new Point(5,6);
      var p2 = new Point{X = 5, Y = 6};

      Console.ReadKey();
    }
```

### Positional record

Immutable by default

- make init property
- make constructor with given params order
- deconstruct method to return single value

```c#
  record Point (int X, int Y);
```

```c#
    static void Main(string[] args)
    {
      var p1 = new Point(5,6);
      // p1.X = 10; // error

      var (x,y) = p; // deconstruct

      Console.ReadKey();
    }
```

- by default positional record doesn't allow object initializer

but u can enable that by making param less constructor and given it default values for object `:this(...values)`

```c#
  record Point(int X, int Y)
  {
    public Point():this(0,0)
    {

    }
  }
```

- Note by default record is `record class`

```c#
  record Point(int X, int Y);
```

same as

```c#
  record class Point(int X, int Y);
```

and it's mutable

### Struct record

from `c# 10`

- Value type record

- Mutable by default

```c#
  record struct Point(int X, int Y);
```

- to make immutable use `readonly` keyword

```c#
  readonly record struct Point(int X, int Y);
```

### with expression

Before this to initialize an object `A` which extend object `B`

```c#
  record struct Point(int X, int Y);
```

```c#
    static void Main(string[] args)
    {
      var p1 = new Point(5,6);
      var p2 = new Point(25,p2.Y);

      Console.ReadKey();
    }
```

But with `with`

```c#
    static void Main(string[] args)
    {
      var p1 = new Point(5,6);
      var p2 = p1 with {X = 25};
      // this mean get all [p1] content and only change
      // x to 25
      // and create p2

      Console.ReadKey();
    }
```

## 042 Top Level statement

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_042/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=43)

- Content
  - usage
  - namespaces
  - where is the `Main` method

### Usage

Simplify project entry point details

old

```c#
    static void Main(string[] args)
    {
      Console.WriteLine("Hello World");

      Console.ReadKey();
    }
```

now

```c#
  Console.WriteLine("Hello World");
```

![](https://raw.githubusercontent.com/Courses-journey/dotnet/main/Metigator/01_mastering_csharp/assets/042_Top_Level_statement.jpg)

### Main method forms

```c#
static void Main()
{
  Console.WriteLine("Metigator");
}
```

```c#
static void Main(string[] args)
{
  Console.WriteLine("Metigator");
}
```

```c#
static int Main()
{
  Console.WriteLine("Metigator");
  return 0;
}
```

```c#
static int Main(string[] args)
{
  Console.WriteLine("Metigator");
  return 0;
}
```

async main in `c# 7`

```c#
static async Task Main(string[] args)
{
  await Task.Run(()=> Console.WriteLine("Metigator"));
}
```

```c#
static async Task<int> Main(string[] args)
{
  await Task.Run(()=> Console.WriteLine("Metigator"));

  return 0;
}
```

### top level statement

Before `.Net6`

```c#
using System;

namespace X.Y
{
  internal class Program
  {
    static void Main(string[] args)
    {
      var number = 9;

      if(number % 2 == 0)
        Console.WriteLine($"{number} is Even");
      else
        Console.WriteLine($"{number} is Odd");

      Console.ReadKey();
    }
  }
}
```

From `.Net6`

```c#
var number = 9;

if(number % 2 == 0)
  Console.WriteLine($"{number} is Even");
else
  Console.WriteLine($"{number} is Odd");

Console. ReadKey();
```

Under the hood the c# complier will generate class/Main method

- but which form of main will be generated?
  - it will depend on your code

```c#
using System;
namespace X.Y
{
  internal class Program
  {
    static void Main(string[] args)
    {
      // ... code will be here
    }
  }
}
```

### Usage

- Make it easier for beginners
- Make schedules tasks

### Rules

#### Rule 01

Nothing before top level statement

namespace , types , delegates

```c#
// namespace XYZ {} //error
// Class Foo {} //error
Console.WriteLine("Hello");
```

but u can define methods

```c#
void PrintHello()
{
  Console.WriteLine("Hello from method");
}
// namespace XYZ {} //error
// Class Foo {} //error
Console.WriteLine("Hello");
PrintHello();
```

#### Rule 02

Top level Functions are Considered Local functions To `Main()`

and that means u can't for example put access modifiers with defined functions

```c#
void PrintHello()
{
  Console.WriteLine("Hello");
}
```

```c#
// error the modifier `public`
// is not valid for this item
public void PrintHello() // error
{
  Console.WriteLine("Hello");
}
```

### namespace

- exist to organize classes and types

- it's like folder and class like files in this folder

```c#
namespace Metigator.Sales
{
  internal class Customer
  {

  }

  internal class Employee
  {

  }
}
```

```c#
Sales.Employee emp = new Sales.Employee();
Sales.Customer emp = new Sales.Customer();
```

### using

instead of rewrite namespace to get the class

u can define it at top

```
using Metigator.Sales

...
{
  ...
  {
    ...
    {
      Employee emp = new Employee();
      Customer emp = new Customer();
    }
  }
}
```

### File scoped namespace

Instead of wrapping all content in curly braces

```c#
namespace Metigator.Sales
{
  internal class Customer
  {
  }

  internal class Employee
  {
  }
}
```

u can define the namespace at top of the file followed by semicolon

and this way all content below this statement will be in its scope

u can define only one namespace in the same file

u cannot nesting namespaces

```c#
namespace Metigator.Sales;

internal class Customer
{
}

internal class Employee
{
}
```

### aliasing

```c#
  Continent.Region.Area.Country.Egypt egy = new Continent.Region.Area.Country.Egypt();
```

```c#
  using CRAC = Continent.Region.Area.Country;
  CRAC.Egypt egy = new CRAC.Country.Egypt();
```

```c#
  using EGY = Continent.Region.Area.Country.Egypt;
  EGY egy = new EGY();
```

### static using

include every static member in that class

```c#
using static type
```

for example

```c#
Console.WriteLine(System.Math.Cos(45));
```

```c#
using static System.Math
Console.WriteLine(Cos(45));
```

### using statement global modifier

Starting from `c#10`

- This direct all files in our project to use any type in that scope
- must be defined at the top of our file

```c#
global using System.Text;
using ...;
using ...;
// A global using directive must
// precede all non-global using directives.
// global using X.Y; // error
```

- It's recommended to define global using in separated folder in your project

create new empty file `GlobalUsings.cs`

and for example

```c#
global using System.Text;
global using static System.Math
```

### Implicit using

```c#
Console.WriteLine(System.DateTime.Now);
Console.WriteLine(DateTime.Now); //valid
```

in `Project.csproj`

```xml
<Project>
  <PropertyGroup>
    ...
    <ImplicitUsing>enable</ImplicitUsing>
  </PropertyGroup>
</Project>
```

by default when `ImplicitUsing` is enabled c# provide u with a `GlobalUsing.cs` file that contains `global using`

```c#
// <auto-generated/>
global using global::System;
global using global::System.Collections.Generic;
global using global::System.IO;
global using global::System.Linq;
global using global::System.Net.Http;
global using global::System.Threading;
global using global::System.Threading.Tasks;
```

But what is `global::` this directive to force use language namespace and avoid calling your own implementation if you for example have namespace called `System` in your projects

u can tell project to remove or add certain `using` by modify `.csproj`

```xml
<Project>
  ...

  <ItemGroup>
    <Using Remove="System.Linq"/>
    <Using Include="System.Text"/>
  </ItemGroup>

</Project>
```

v## 043 Working with NULL

```md
I call it my billion-dollar mistake. It was the invention of
the null reference in 1965

- Tony Hoare
```

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_043/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=44)

- Content

  - Compile time vs RunTime
  - Referencing and Dereferencing

### Compile time vs RunTime

- Compile time error

very easy to solve with squiggly red lines below the error

```c#
static void Main(string[] args)
{
  string input = "123A";
  // "compile time" building source code and convert it to IL
  int num1 = input; // CS0029 can't convert string to int
  Console.ReadKey();
}
```

- Runtime error

throw exception when u executed the compiled code

```c#
static void Main(string[] args)
{
  string input = "123A";
  int num = int.Parse(input);
  Console.ReadKey();
}
```

### Referencing and Dereferencing

`default` is keyword that give you the default value based on data type

inferre the value

- Reference type

  ```c#
  string str1 = default;
  // the default value for string is null
  // string str1 = null
  ```

  - `Referencing` variable that points to an object

    like `str1`

  - `Dereferencing` following the reference pointed to by variable to access underlying object
    ```c#
    Console.WriteLine(str1.Length); // will throw null reference exception
    ```

- Value type

  ```c#
  DateTime datetime = default;
  // the default value for DateTime is
  // 0001/01/01 00:00 AM
  ```

  ```c#
  Console.WriteLine(datetime.Month); // will work fine
  ```

### Nullable Value Type

`c# 2.0+`

```c#
int mark = default; //0
```

Define nullable value using

- `Nullable<T>` where T is value type

  ```c#
  // Nullable<T> T is value type [struct]
  Nullable<int> mark2 = default // null

  if(mark2 is null)
  {
    Console.WriteLine("Not available");
  }
  else
  {
    Console.WriteLine($"Mark2: {mark2}");
  }
  ```

- using `T?`

  ```c#
  // Nullable<T> T is value type [struct]
  int? mark2 = default // null

  if(mark2 is null)
  {
    Console.WriteLine("Not available");
  }
  else
  {
    Console.WriteLine($"Mark2: {mark2}");
  }
  ```

- check data is not null

  ```c#
  if(mark2 is null)
  ```

  or using

  ```c#
  if(!mark2.HasValue)
  ```

- init nullable

  ```c#
  Nullable<int> mark2 = default; //null
  ```

  or

  ```c#
  Nullable<int> mark2 = new Nullable<int>(); //null
  ```

  or

  ```c#
  int? mark2 = default(int?); //null
  ```

  note with `new` syntax

  ```c#
  Nullable<int> mark2 = new(); //0
  ```

### Nullable Reference Type

`c# 8.0`

| Target framework | version | c# language version default |
| ---------------- | ------- | --------------------------- |
| .NET             | 7.x     | C# 11                       |
| .NET             | 6.x     | C# 10                       |
| .NET             | 5.x     | C# 9.0                      |
| .NET Core        | 3.x     | C# 8.0                      |
| .NET Core        | 2.x     | C# 7.3                      |
| .NET Standard    | 2.1     | C# 8.0                      |
| .NET Standard    | 2.0     | C# 7.3                      |
| .NET Standard    | 1.x     | C# 7.3                      |
| .NET Framework   | all     | C# 7.3                      |

Before `c# 8` All reference type are nullable

After `c# 8` All reference type are also nullable but with new way to deal with

to activate nullable in your project

go to `.csproj`

```xml
<PropertyGroup>
  ...
  <Nullable>enable</Nullable>
</PropertyGroup>
```

#### why?

`compile time effect`

![](https://raw.githubusercontent.com/Courses-journey/dotnet/main/Metigator/01_mastering_csharp/assets/043_Working_with_NULL.jpg)

when `nullable` is `disabled` or is `enabled` and convert code to intermediate language the code will be the same

#### Benefits

1. Avoid Null Reference Exception.
2. Help Compilers Detect Possible Null
   Reference Exception.
3. Better reasoning.

with `nullable` disabled the code below will compiled successfully but during runtime will throw null reference exception

```c#
static void Main(string[] args)
{
  string name = null;
  string decision = IsLongName(name) ? "long" : "short"; // will throw an exception
  Console.WriteLine($"{name} is {decision}");
  Console. ReadKey();
}

static bool IsLongName(string name)
{
  return name. Length > 10; // assumption name is not null
}
```

with `nullable` enabled the compiler will deal with reference type as they are `non-nullable`

```c#
static void Main(string[] args)
{
  // string name = null; // warning
  // Fix
  string? name = null;
  string decision = IsLongName(name) ? "long" : "short"; // will throw an exception
  Console.WriteLine($"{name} is {decision}");
  Console. ReadKey();
}

static bool IsLongName(string? name)
{
  if(name is null) return false;
  return name. Length > 10;
}
```

- u can define warnings as errors

  from `.csproj`

  `CS8600` Converting null literal or possible value to non-nullable type

  `CS8604` Possible null reference argument for parameter `XXX` in `XXX`

  ```xml
  <PropertyGroup>
    ...
    <Nullable>enable</Nullable>
    <WarningsAsErrors>CS8600, CS8604</WarningsAsErrors>
  </PropertyGroup>
  ```

- define all warning as errors

  ```xml
  <PropertyGroup>
    ...
    <Nullable>enable</Nullable>
    <TreatWarningsAsErrors>true</TreatWarningsAsErrors>
  </PropertyGroup>
  ```

### Compiler static analysis

#### non-null scenarios

- Assignment of non-null value

```c#
static bool Scenario01()
{
  string name = String.Empty; //Assignment of non-null value
  return name.Length > 10; // assumption name could be null
}
```

- Check against null

```c#
static bool Scenario02()
{
  string? name = GetName();
  if(name == null) return false; // Check against null
  return name.Length > 10; // value should be null
}
```

#### May be null scenarios

```c#
static bool Scenario03()
{
  string? name = GetName();
  return name.Length > 10; // may be null
}
```

#### Compiler dose not trace called method

```c#
public class Person
{
  public string FirstName { get; set; }

  public string LastName { get; set; }

  public Person(string firstName, string lastName)
  {
    FirstName = firstName;
    LastName = lastName;
  }
}
```

```c#
...main
{
  var person = new Person(null.null); // will give u warning
}
```

- example not working properly

```c#
public class Student : Person
{
  public string Major { get; set; }

  //warning Non-Nullable `major` must contain a non-null value when exiting constructor,
  // Consider declaring the property as nullable
  public Student(string firstName, string lastName, string major)
    : Person(firstName, lastName)
  {
    SetMajor(major);
  }


  //warning Non-Nullable `major` must contain a non-null value when exiting constructor,
  // Consider declaring the property as nullable
  public Student(string firstName, string lastName)
    : Person(firstName, lastName)
  {
    SetMajor(); //warning
  }

  // I'm sure this will return a value
  public void SetMajor(string? major)
  {
    Major = major ?? "Undeclared";
  }
}
```

To fix this warning u can use `[MemberNotNull]` attribute

`using System.Diagnostics.CodeAnalysis;`

```c#
public class Student : Person
{
  public string Major { get; set; }

  ...

  [MemberNotNull(nameof(Major))]
  public void SetMajor(string? major)
  {
    Major = major ?? "Undeclared";
  }
}
```

| Attributes        | Category | Meaning |
| ----------------- | -------- | ------- |
| AllowNull         | ...      | ...     |
| DisallowNull      | ...      | ...     |
| MaybeNull         | ...      | ...     |
| NotNull           | ...      | ...     |
| MaybeNullWhen     | ...      | ...     |
| NotNullWhen       | ...      | ...     |
| NotNullIfNotNull  | ...      | ...     |
| MemberNotNull     | ...      | ...     |
| MemberNotNullWhen | ...      | ...     |
| DoesNotReturn     | ...      | ...     |
| DoesNotReturnIf   | ...      | ...     |

### Nullable value annotations

- When to use

  - Don't care with nullable `handle exception`
  - Unit Testing
  - You know value can be null

- using `!`

  ```c#
  string fname = null; // warning
  string lname = null!; // work fine
  ```

  ```c#
  // Having Person class with nullable string FirstName
  Console.WriteLine(person.FirstName.length); // warning
  Console.WriteLine(person.FirstName!.length); // fine
  Console.WriteLine(person.FirstName?.length); // fine
  ```

- define nullable reference type

  ```c#
    Student st1 = new Student(); // non-nullable
    Student? st2 = new Student(); // nullable
    var st2 = new Student(); // nullable
  ```

### Nullable and Generics

#### in `netcoreapp3.1`

```xml
<PropertyGroup>
  <TargetFramework>netcoreapp3.1</TargetFramework>
</PropertyGroup>
```

the code below will be error as T should be struct `value type` as the reference type at that point doesn't have nullable

```c#
static T? DoSomething<T> (T source)
{
  return source;
}
```

to fix that

```c#
static T? DoSomething<T> (T source) where T : struct
{
  return source;
}
```

#### in `net6.0`

```xml
<PropertyGroup>
  <TargetFramework>net6.0</TargetFramework>
</PropertyGroup>
```

the code below will work fine

```c#
static T? DoSomething<T> (T source)
{
  return source;
}
```

### Struct and Array with reference type

#### struct

```c#
// Struct contain reference types
public struct Student
{
  public string FirstName;
  public string? MiddleName;
  public string LastName;
}
```

```c#
static void print(Student student)
{
  Console.WriteLine($"First Name: {student.FirstName.ToUpper()}");
  Console.WriteLine($"Middle Name: {student.MiddleName?.ToUpper()}");
  Console.WriteLine($"Last Name: {student.LastName.ToUpper()}");
}
```

```c#
main
{
  // the compile won't give any errors
  // throw null reference exception
  print(default);
}
```

#### Array

```c#
string[] names = new string[10];
var firstVal = names[0];

// the compile won't give any errors
// throw null reference exception
Console.WriteLine(firstValue.ToUpper());
```

### Nullable Context

| Green Field | Legacy Large Code Base Projects | Active Projects Add new Features |
| ----------- | ------------------------------- | -------------------------------- |
| New project | ------------------------------- | -------------------------------- |

- Legacy Large Code Base Projects

  ```xml
  <Nullable>disable</Nullable>
  ```

- compiler emits warning when Null reference could be thrown

  ```xml
  <Nullable>warnings</Nullable>
  ```

- Express your design intent before enabling warnings

  ```xml
  <Nullable>annotations</Nullable>
  ```

- Green field or active projects

  ```xml
  <Nullable>enable</Nullable>
  ```

- The recommended way to deal with Legacy Large Code Base Projects is

  using complier directive

  But this code at top of your file and that way u can deal with each file separately

  ```c#
  #nullable enable
  ```

  and at file bottom

  ```c#
  #nullable restore
  ```

  ```c#
  #nullable enable

  // code here

  #nullable restore
  ```

  or use annotations

  ```c#
  #nullable enable annotations

  // code here

  #nullable restore annotations
  ```

  or use warnings

  ```c#
  #nullable enable warnings

  // code here

  #nullable restore warnings
  ```

![](https://raw.githubusercontent.com/Courses-journey/dotnet/main/Metigator/01_mastering_csharp/assets/043_Working_with_NULL_01.jpg)

## 044 Strings in c#

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_044/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=45)

- Content

### How data stored

![](https://raw.githubusercontent.com/Courses-journey/dotnet/main/Metigator/01_mastering_csharp/assets/044_Strings_01.jpg)

```
abcdefghijklmnopqrstuvwxyz0123456789

```

| Size | Type            | Supported       |
| ---- | --------------- | --------------- |
| 26   | letters (a-z)   | -               |
| 10   | digit (0-9)     | -               |
| 1    | CR Cargo Return | Windows - Macos |
| 1    | LF Line Feed    | Windows - Linux |

### ASCII VS. Extended ASCII

- `ASCII` 128 chars
- `Extended ASCII`256 chars

```c#
for (byte c = 0; c < 255; ++c)
{
  char ch = (char)c;
  string dec = c.ToString().PadLeft(3, '0');
  string hex = c.ToString("X");
  string binary = Convert.ToString(c, 2). PadLeft(8, '0');
  Console.WriteLine($"{de|,-12} {binary,-12} {hex,-12} {ch,-12}");
}
```

### Text Encodings and Unicode

- `Unicode`

  - up to `million` chars
  - used `100,000` chars

- ASCII Encoding

  ```c#
    static async Task GetDataASCIIFormat()
    {
      var path = $"{Environment.GetFolderPath(Environment.SpecialFolder.Desktop)}";
      var filePath = $"{path}\\asciiNewsContent.txt";
      using (var client = new HttpClient())
      {
        Uri uri = new Uri("https://website.com");
        using (HttpResponseMessage response = await client.GetAsync(uri))
        {
          var byteArray = await response.Content.ReadAsByteArrayAsync();
          string result = Encoding.ASCII.GetString(byteArray);
          File.WriteAllText(filePath, result);
        }
      }
    }
  ```

  ```c#
    private static void Main(string[] args)
    {
      Task.Run(() => GetDataASCIIFormat()).Wait();
      Console.WriteLine("Done");
      Console.ReadKey();
    }
  ```

- UTF8 Encoding

  ```c#
    static async Task GetDataUTF8Format()
    {
      var path = $"{Environment.GetFolderPath(Environment.SpecialFolder.Desktop)}";
      var filePath = $"{path}\\utf8NewsContent.txt";
      using (var client = new HttpClient())
      {
        Uri uri = new Uri("https://website.com");
        using (HttpResponseMessage response = await client.GetAsync(uri))
        {
          var byteArray = await response.Content.ReadAsByteArrayAsync();
          string result = Encoding.UTF8.GetString(byteArray);
          File.WriteAllText(filePath, result);
        }
      }
    }
  ```

  ```c#
    private static void Main(string[] args)
    {
      Task.Run(() => GetDataUTF8Format()).Wait();
      Console.WriteLine("Done");
      Console.ReadKey();
    }
  ```

### String Instantiation

#### Using Quoted String Literals

```c#
string str = "Metigator";
```

#### Using String Constructor

```c#
char[] letters = {'M','e','t','i','g','a','t','o','r'};
string str = new string(letters);
```

#### Using Repeating Character

```c#
string str = new string('M',8); //repeat M 8 times
```

#### Using Pointer To Signed Byte

```c#
private static void UsingPointerToSignedByte()
{

  // [4] Create a string from a pointer to a signed byte array.
  //               'M'   'e'   't'   'i'    'g'  'a'    't'   'o'    'r'
  sbyte[] bytes = { 0x4D, 0x65, 0x74, 0x69, 0x67, 0x61, 0x74, 0x6F, 0x72 };
  string str = null;
  // safe context (use pointer, allocation memory block,
  // call method using function pointer
  unsafe
  {
    // Pin the buffer to a fixed location in memory.
    fixed (sbyte* ptr = bytes)

    str = new string(ptr);
    Console. WriteLine(str);
  }

}
```

- Safe Context

Area where u can use pointers `allocation memory block`

or call method that use function pointer

in `csproj`

```xml
<PropertyGroup>
  <AllowUnsafeBlocks>true</AllowUnsafeBlocks>
</PropertyGroup>
```

#### Using A Pointer To Character Array

```c#
private static void UsingAPointerToCharacterArray()
{
  // [5] Create a string from a pointer to a character array.
  char[] letters = { 'M', 'e', 't', 'i', 'g', 'a', 't', 'o', 'r'};

  string str = null;
  unsafe
  {
    fixed (char* pchars = letters)

    // Create a string from a pointer to a character array.
    str = new string(pchars);
    Console. WriteLine(str);
  }
}
```

#### Using Concatenation

```c#
private static void UsingConcatenation()
{
  // [5] Using concatenation
  string str1 = "Meti" + "gator";
  string str2 = $"{"Meti"}{"gator"}";

  Console. WriteLine($"str1 = {str1}");
  Console. WriteLine($"str2 = {str2}");
}
```

#### Using Calling Method That Returns String

```c#
private static void UsingCallingMethodThatReturnsString()
{
  string sentence = "I Love Metigator channel.";

  int startPos = sentence. IndexOf("Metigator"); // 7

  string str = sentence. Substring(startPos, 9); // string from 7,

  Console.WriteLine(str);
}
```

#### Using Formatted String

```c#
private static void UsingFormattedString()
{
  // using formatted str
  string customer = "Issam A";
  DateTime shippingDate = DateTime.Now; // yyyy-MM-dd hh :mm
  DateTime expectedDelivery = shippingDate.AddDays(7); // yyyy-MM-dd hh:mm
  decimal shippingCost = 29.99m;

  string str = String. Format(
  "\nDear {o}.," +
  "\n\nAt {1:t} on {1:D}, the order is on its way to you" +
  "\nIt's expected to be delivered at {2:t} on {2:D}, the order is on its way to you"
  "\nShipping cost {3:c}. "+
  "\n\t\t\tThanks for shopping with us!",

  // 0          1                   2         3
  customer, shippingDate, expectedDelivery, shippingCost);

  Console.WriteLine(str);
}
```

output

```
Dear Issam A.,

At 4:26 PM on August 21, 2022, the order is on its way to you
It's expected to be delivered at 4:26 PM on August 28, 2022, the order is on its way to you
Shipping cost $29.99.

      Thanks for shopping with us!
```

- Parameters specifiers

  - `{1:t}` show only time

  - `{1:D}` show Date only

  - `{1:c}` currency

#### Using Verbatim With String Interpolation

```c#
private static void UsingVerbatimWithStringInterpolation()
{
    string customer = "Issam A";
    DateTime shippingDate = DateTime.Now;
    DateTime expectedDelivery = shippingDate.AddDays(7);
    decimal shippingCost = 29.99m;

    string str = $@"Dear {customer},

At {shippingDate:t} on {shippingDate:D}, the order is on its way to you
It's expected to be delivered at {expectedDelivery:t} on {expectedDelivery:D}, the order is on its way to you
Shipping cost {shippingCost:c}.
                Thanks for shopping with us!";
    Console.WriteLine(str);
}
```

#### Using Raw String

from `c#11`

```c#
private static void UsingRawString()
{
    // Raw string starting from C# 11.0
    string str = """
            <nav class="box">
                <ul>
                    <a href="javascript:void(0)">"Home"</a>
                <li>
                <ul>
                    <a href="javascript:void(0)">About us</a>
                <li>
            </nav>
        """;

    string str2 = """ this is a single line raw string""";
    Console.WriteLine(str);
    Console.WriteLine(str2);
}
```

```xml
<PropertyGroup>
  <LangVersion>preview</LangVersion>
</PropertyGroup>
```

### Unicode and string comparison

```c#
static void Main(string[] args)
{
    // Unicode character -> code point
    // Code point a = "\u0061";
    // graphemes: multiple char object (base, combine) : a  ̈
    // Also we have single chars that represent the graphems ä


    StreamWriter sw = new StreamWriter(@".\output.txt");
    string char1 = "\u0061"; // a
    string char2 = "\u0308"; // ̈

    sw.WriteLine(char1); // a
    sw.WriteLine(char2); // ̈


    string grapheme = "\u0061\u0308";
    sw.WriteLine(grapheme); // ä


    string singleChar = "\u00e4";
    sw.WriteLine(singleChar); // ä

    // representation are equal
    sw.WriteLine("{0} = {1} (Culture-sensitive): {2}", grapheme, singleChar,
                  String.Equals(grapheme, singleChar,
                                StringComparison.CurrentCulture)); // true

    sw.WriteLine("{0} = {1} (Ordinal): {2}", grapheme, singleChar,
                  String.Equals(grapheme, singleChar,
                                StringComparison.Ordinal)); // False

    sw.WriteLine("{0} = {1} (Normalized Ordinal): {2}", grapheme, singleChar,
                  String.Equals(grapheme.Normalize(),
                                singleChar.Normalize(),
                                StringComparison.Ordinal)); // True
    sw.Close();
}
```

```C#

public enum StringComparison
{
  CurrentCulture = 0,
  CurrentCultureIgnoreCase = 1,
  InvariantCulture = 2,
  InvariantCultureIgnoreCase = 3,
  Ordinal = 4,
  OrdinalIgnoreCase = 5
}
```

`Ordinal` using number value

### String Intern Pool

- CLR

  `CLR Common Language Runtime` : Convert `Managed Code` -> `Native code`

  `C# Code` -> `Intermediate Language` ->

  Then `JIT Compiler`

  `Intermediate Language` -> `Binary Code`

- Garbage Collector

  Memory Management
  Allocation and deallocation variables

There is `Stack` and `Heap` but when dealing string there is new concepts `Intern Pool`

![](https://raw.githubusercontent.com/Courses-journey/dotnet/main/Metigator/01_mastering_csharp/assets/044_Strings.png)

#### String Literal Vs Object

```c#
public static void RunStringLiteralVsObject()
{
    string s1 = "metigator"; // string literal
    string s2 = new string ("metigator"); // string object


    Console.WriteLine(s1 == s2);                   // true same content (string override equality value based)
    Console.WriteLine(s1.Equals(s2));              // true same content

    Console.WriteLine((Object)s1 == (Object)s2);   // false two different reference
    Console.WriteLine(ReferenceEquals(s1, s2));    // false two different reference

}
```

![](https://raw.githubusercontent.com/Courses-journey/dotnet/main/Metigator/01_mastering_csharp/assets/044_Strings_02.png)

#### String Literal Key

```c#
public static void RunStringLiteralKey()
{
    string s1 = "metigator"; // string literal
    string s2 = "aspnet"; // string literal
    string s3 = "meti" + "gator"; // string literal



    Console.WriteLine(s1 == s2);                   // false  different content
    Console.WriteLine(ReferenceEquals(s1, s2));    // false two different reference


    Console.WriteLine(s1 == s3);   // true same content
    Console.WriteLine(ReferenceEquals(s1, s3));   // true same reference
}
```

![](https://raw.githubusercontent.com/Courses-journey/dotnet/main/Metigator/01_mastering_csharp/assets/044_Strings_03.png)

#### String Literal With String Object Comparison

```c#
public static void RunStringLiteralWithStringObjectComparison()
{
    string s1 = "metigator"; // string literal
    //string s11 = "metigator";
    string s2 = new string("metigator");                  // string object

    Console.WriteLine(s1 == s2);                   // true, same content

    Console.WriteLine(ReferenceEquals(s1, s2));   // false different reference

}
```

![](https://raw.githubusercontent.com/Courses-journey/dotnet/main/Metigator/01_mastering_csharp/assets/044_Strings_04.png)

#### String Intern

Retrieves the system's reference to the specified System.String.

```c#
public static void RunStringIntern()
{
    string s1 = "metigator";                       // string literal

    string s2 = new string("metigator");   // string object

    string s3 = String.Intern(s2);                  // string literal

    Console.WriteLine(s1 == s2);                   // true, same content
    Console.WriteLine(ReferenceEquals(s1, s2));   // false different reference

    Console.WriteLine(s2 == s3);                   // true, same content
    Console.WriteLine(ReferenceEquals(s2, s3));   // false different reference

    Console.WriteLine(s1 == s3);                   // true, same content
    Console.WriteLine(ReferenceEquals(s1, s3));   // true, same reference


    string str = "xyz";

    Console.WriteLine(str);

}
```

![](https://raw.githubusercontent.com/Courses-journey/dotnet/main/Metigator/01_mastering_csharp/assets/044_Strings_05.png)

### String Methods

#### CopyTo

```c#

static void RunCopyTo()
{
    string s1 = "metigator";
    char[] characters = { 'f', 'u', 'l', 'l', ' ', 's', 't', 'a', 'c', 'k', ' ',
        '?', '?', '?', '?', '?', '?', '?', '?', '?'};

    Console.WriteLine(characters);

    // copies count characters from the sourceIndex position of this instance
    // to the destinationIndex position of destination character array.

    s1.CopyTo(0, characters, 11, s1.Length);

    Console.WriteLine(characters);
}
```

#### Compare

```c#
static void RunCompare()
{
    // ascii sort order (integer, capital, small)
    // a12Bc = 12Bac

    string s1 = "metigator";
    string s2 = "Metigator";

    // Compares two specified String objects and returns an integer
    // that indicates their relative position in the sort order.
    Console.WriteLine(string.Compare(s1, s2, true));  // 0
    Console.WriteLine(string.Compare(s1, s2, false)); // -1
    Console.WriteLine(string.Compare(s2, s1, false)); // 1
}
```

#### StringFound

```c#
static void RunStringFound()
{
    // ascii sort order (integer, capital, small)
    string s1 = "metigator";

    // Returns whether a specified character occurs within this string.
    Console.WriteLine(s1.Contains("gato")); // true

    // starts with the specified character.
    Console.WriteLine(s1.StartsWith("meti")); // true

    // ends with the specified character.
    Console.WriteLine(s1.EndsWith("torx")); // false

    // Reports the zero-based index of the first occurrence
    Console.WriteLine(s1.IndexOf("tig")); //2
}
```

#### StringFormat

```c#
static void RunStringFormat()
{
    var users = new List<dynamic>
    {
        new { Username =  "user1",  Since = new DateTime(2022, 7, 7) , Followers = 15053 },
        new { Username =  "user2",  Since = new DateTime(2021, 5, 9) , Followers = 12046 },
        new { Username =  "user3",  Since = new DateTime(2022, 11, 10) , Followers = 14027 }
    };

    // Converts the value of objects to strings based on the
    // formats specified and inserts them into another string.
    var header = String.Format("{0,-12}{1,8}{2,12}\n",
                      "Username", "Created At", "Followers");

    Console.WriteLine(header);

    foreach (var user in users)
        Console.WriteLine(String.Format("{0,-12}{1,8:yyyy}{2,12:N0}\n",
                      user.Username, user.Since, user.Followers));

}
```

payload

format emails

store formatted files

#### StringIsNullOrEmpty

```c#
static void RunStringIsNullOrEmpty()
{
    string s1 = "metigator";
    string s2 = "";
    string s3 = "   ";
    string s4 = null;
    string s5 = String.Empty;

    // null or empty
    Console.WriteLine(String.IsNullOrEmpty(s1)); // false

    Console.WriteLine(String.IsNullOrEmpty(s2)); // true

    Console.WriteLine(String.IsNullOrEmpty(s3)); // false

    Console.WriteLine(String.IsNullOrEmpty(s4)); // true

    Console.WriteLine(String.IsNullOrEmpty(s5)); // true
}
```

#### StringIsNullOrWhiteSpace

```c#
static void RunStringIsNullOrWhiteSpace()
{
    string s1 = "metigator";
    string s2 = "";
    string s3 = "   ";
    string s4 = null;
    string s5 = String.Empty;

    // null or white spaces
    Console.WriteLine(String.IsNullOrWhiteSpace(s1)); // false

    Console.WriteLine(String.IsNullOrWhiteSpace(s2)); // true

    Console.WriteLine(String.IsNullOrWhiteSpace(s3)); // true

    Console.WriteLine(String.IsNullOrWhiteSpace(s4)); // true

    Console.WriteLine(String.IsNullOrWhiteSpace(s5)); // true
}
```

#### StringModify

```c#
static void RunStringModify()
{
    string s1 = "metior";
    string s2 = "metizanor";
    string s3 = "metixyzgator";

    //Returns a new string in which a specified string is inserted at a
    //specified index position in this instance.
    s1 = s1.Insert(4, "gat");
    Console.WriteLine(s1); // metigator

    // all occurrences the current string are replaced with
    // another specified Unicode character or String.
    s2 = s2.Replace("zan", "gat");
    Console.WriteLine(s2); // metigator

    //Returns a new string in which a specified number of characters
    //from the current string are deleted.
    s3 = s3.Remove(4, 3);
    Console.WriteLine(s3); // metigator
}
```

#### ToCase

```c#
static void RunToCase()
{
    string s1 = "Metigator";

    // Returns a copy of this string converted to uppercase
    // might produce culture specific output,
    // use it when user input string in their own language
    Console.WriteLine(s1.ToUpper());

    // Returns a copy of this string converted to lowercase.
    // might produce culture specific output,
    // use it when user input string in their own language
    Console.WriteLine(s1.ToLower());

    // Returns a copy of this string converted to lowercase.
    // use for non language specific data
    Console.WriteLine(s1.ToLowerInvariant());

    // Returns a copy of this string converted to uppercase.
    // use for non language specific data
    Console.WriteLine(s1.ToUpperInvariant());
}
```

#### Trim

```c#
static void RunTrim()
{
    string s1 = "   Metigator   ";
    string s2 = "...Metigator....";

    //Removes all leading and trailing occurrences
    Console.WriteLine("Trim(), Trim(char)");
    Console.WriteLine(s1.Trim());    // "Metigator"
    Console.WriteLine(s2.Trim('.')); // "Metigator"

    //Removes all leading  occurrences
    Console.WriteLine("TrimStart(), TrimStart(char)");
    Console.WriteLine(s1.TrimStart()); // "Metigator   "
    Console.WriteLine(s2.TrimStart('.'));// "Metigator...."

    //Removes all trailing  occurrences
    Console.WriteLine("TrimEnd(), TrimEnd(char)");
    Console.WriteLine(s1.TrimEnd());//  "   Metigator"
    Console.WriteLine(s2.TrimEnd('.')); // "...Metigator"
}
```

#### ToCharacterArray

```c#
static void RunToCharacterArray()
{
    string s1 = "metigator";
    char[] characters;

    //Copies the characters in this instance to a Unicode character array.
    characters = s1.ToCharArray();

    foreach (char ch in characters)
        Console.Write($" {ch}");
}
```

#### Split

```c#
static void RunSplit()
{
    string s1 = "This is metigator channel";

    // Returns a string array that contains the substrings
    // in this instance that are delimited by elements of
    // a specified string or Unicode character array.
    string[] words = s1.Split(" ");

    foreach (var word in words)
        Console.WriteLine(word);
}
```

#### Join

```c#
static void RunStringJoin()
{
    string[] values = { "Los Angeles", "1st Jan 1940", "15M" };

    //Concatenates the elements of a specified array or the members
    //of a collection, using the specified separator between each
    //element or member.
    string commaSeparated = string.Join(',', values);

    Console.WriteLine(commaSeparated); // Los Angeles,1st Jan 1940,15M
}

```

`,` excel csv files

## 045 String Builder

- Data

  - [Github](https://github.com/metigator/CSharp_Lesson_045/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=46)

- Content

| String                         | String Builder                 |
| ------------------------------ | ------------------------------ |
| System.String                  | System.Text.StringBuilder      |
| Reference Type                 | Reference Type                 |
| Represent string of characters | Represent string of characters |
| Immutable                      | Mutable                        |

![](https://raw.githubusercontent.com/Courses-journey/dotnet/main/Metigator/01_mastering_csharp/assets/045_StringBuilder.jpg)

### using string

```c#
static string GenerateWithString()
{

  // Imagine it's a complicated process to generate 'METIGATOR'
  // using String

  // declare string
  string str = null;

  // append three characters 'E', 'T', and 'I'
  str += String.Concat(new char[] { 'E', 'T', 'I' }); // ETI

  // Append a format string to the end of the string.
  str += String.Format("GAT{0}{1}{2}", '0', 'P', 'S'); // GATOPS

  // Insert 'M' to beginning of a string
  str = "M" + str; // METIGATORS

  // Replace 'P' with 'R'
  str = str.Replace('P', 'R'); //METIGATORS

  // Remove 'S' from the string
  str = str.Remove(str.Length - 1); // METIGATOR

  return str;
}
```

### using StringBuilder

```c#
static string GenerateWithStringBuilder()
{
  // Imagine it's a complicated process to generate 'METIGATOR'
  // using StringBuilder
  // instantiate a StringBuilder
  StringBuilder sb = new StringBuilder();

  // append three characters 'E', 'T', and 'I' to stringBuilder
  sb.Append(new char[] { 'E', 'T', 'I' }); //

  // Append a format string to the end pf the stringBuilder.
  sb.AppendFormat("GAT{0} {1} {23", '0', 'P', 'S'); // ETIGATORS

  // Insert 'M' to beginning of a stringbuilder
  sb.Insert(0, "M"); // METIGATOPS

  // Replace 'P' with 'R'.
  sb.Replace('P', 'R'); //METIGATORS

  // Remove 'S' from the stringbuilder
  sb.Remove(sb.Length - 1, 1); // METIGATOR

  return sb. ToString();
}
```

### StringBuilder How it works

#### Array of characters

```c#
static void RunArray0fCharacterConcept()
{
  char[] characters;
  // Console. WriteLine(characters. Length); // use of unassigned error

  characters = new char[9];

  characters[0] = 'M';
  characters[1] = 'e';
  characters[2] = 't';
  characters[3] = 'i';
  characters[4] = 'g';
  characters[5] = 'a';
  characters[6] = 't';
  characters[7] = 'o';
  characters[8] = 'r';

  // or
  characters = new char[9] { 'M', 'e', 't', 'i', 'g', 'a', 't', 'o', 'r'};

  // or
  characters = new char[] { 'M', 'e', 't', 'i', 'g', 'a', 't', 'o', 'r'};

  characters[0] = 'm'; // mutate

  Console. WriteLine(characters);
}
```

#### StringBuilder Properties

```c#
static void RunStringBuilderProperties()
{

    var sb = new StringBuilder("Metigator");

    Console.WriteLine(sb.ToString());              // Metigator

    //the characters the object currently contains
    Console.WriteLine($"Length: {sb.Length}");     // 9

    //  the number of characters that the object can contain.
    Console.WriteLine($"Capacity: {sb.Capacity}"); // 16 (default)

    // the maximum capacity, if it's reached,  OutOfMemoryException
    Console.WriteLine($"MaxCapacity: {sb.MaxCapacity}"); // 2,147,483,647  (default)

    Console.WriteLine($"First Letter: {sb[0]}");     // M  Index out of range exception

}
```

#### Working mechanism

```c#
static void RunStringBuilderHowItWorks()
{

    var sb = new StringBuilder();
    // sb is a StringBuilder object
    // string value is empty, length 0, capacity 16, maxcapacity is 2,147,483,647

    sb.Append("I Love Metigator"); // add 16 character

    Console.WriteLine($"Length: {sb.Length}");           // 16
    Console.WriteLine($"Capacity: {sb.Capacity}");       // 16  (default)
    Console.WriteLine($"MaxCapacity: {sb.MaxCapacity}"); // 2,147,483,647 (default)

    sb.Append("Youtube Channel"); // add 15 character

    Console.WriteLine($"Length: {sb.Length}");           // 31
    Console.WriteLine($"Capacity: {sb.Capacity}");       // 32 (size doubled)
    Console.WriteLine($"MaxCapacity: {sb.MaxCapacity}"); // 2,147,483,647 (default)
}
```

Parent child Relationship

![](https://raw.githubusercontent.com/Courses-journey/dotnet/main/Metigator/01_mastering_csharp/assets/045_StringBuilder_01.jpg)

### StringBuilder Instantiation

6 overloads constructors

#### 01

```c#
static void RunConstructorOverLoad1()
{
    // StringBuilder ();
    var sb = new StringBuilder();
    // string value in string.Empty
    // capacity is set to the implementation-specific default


    sb.Append("Metigator");

    Console.WriteLine(sb.ToString());
    Console.WriteLine($"Length: {sb.Length}");
    Console.WriteLine($"Capacity: {sb.Capacity}");
    Console.WriteLine($"MaxCapacity: {sb.MaxCapacity}");
}
```

#### 02

```c#
static void RunConstructorOverLoad2()
{
    // StringBuilder (int capacity);
    // capacity is less than zero ArgumentOutOfRangeException
    // capacity is zero =  default will be taken
    // capacity is extended to the default capacity if it fits
    var sb = new StringBuilder(8);

    sb.Append("Metigator");

    Console.WriteLine(sb.ToString());
    Console.WriteLine($"Length: {sb.Length}"); // 9
    Console.WriteLine($"Capacity: {sb.Capacity}"); // 16
    Console.WriteLine($"MaxCapacity: {sb.MaxCapacity}"); //21..
}
```

#### 03

```c#
static void RunConstructorOverLoad3()
{
    // StringBuilder (string? value);
    // If value is null, the new StringBuilder will contain the empty string
    var sb = new StringBuilder("Metigator");

    Console.WriteLine(sb);
    Console.WriteLine($"Length: {sb.Length}");
    Console.WriteLine($"Capacity: {sb.Capacity}");
    Console.WriteLine($"MaxCapacity: {sb.MaxCapacity}");
}
```

#### 04

```c#
static void RunConstructorOverLoad4()
{
    // StringBuilder (string? value, int capacity);
    // if capacity less than zero => ArgumentOutOfRangeException
    // additional allocation if the number of chars stored exceed capacity

    var sb = new StringBuilder("Metigator", 4);

    Console.WriteLine(sb);
    Console.WriteLine($"Length: {sb.Length}"); // 9
    Console.WriteLine($"Capacity: {sb.Capacity}");
    Console.WriteLine($"MaxCapacity: {sb.MaxCapacity}");
}
```

#### 05

```c#
static void RunConstructorOverLoad5()
{
    // StringBuilder (int capacity, int maxCapacity);
    // if capacity less than zero => ArgumentOutOfRangeException
    // if maxcapacity less than one => ArgumentOutOfRangeException
    // if capacity is zero implementation default capacity is used
    // if capacity exeeds max capacity ArgumentOutOfRangeException

    var sb = new StringBuilder(0, 9);
    sb.Append("Metigator");

    Console.WriteLine(sb);
    Console.WriteLine($"Length: {sb.Length}");  // 9
    Console.WriteLine($"Capacity: {sb.Capacity}"); // 9
    Console.WriteLine($"MaxCapacity: {sb.MaxCapacity}"); //9
}
```

#### 06

```c#
static void RunConstructorOverLoad6()
{
    // StringBuilder (string? value, int startIndex, int length, int capacity);
    // If capacity is zero, the implementation-specific default capacity
    // if capacity less than zero => ArgumentOutOfRangeException
    // additional allocation if the number of chars stored exceed capacity
    // startIndex+length is not a position within value.=> ArgumentOutOfRangeException

    //                          01234567
    var sb = new StringBuilder("I Love Metigator", 7, 9, 9);


    Console.WriteLine(sb);
    Console.WriteLine($"Length: {sb.Length}"); // 9
    Console.WriteLine($"Capacity: {sb.Capacity}"); // 9
    Console.WriteLine($"MaxCapacity: {sb.MaxCapacity}"); // 2, 147,0000
}
```

### StringBuilder Methods

#### Append

```c#
private static void RunAppend()
{
    var sb = new StringBuilder();
    // Append Return StringBuilder, useful method chaining
    sb.Append("ƒ(x)").Append("=").Append("Σ").Append("x²").Append("±").Append("α");

    Console.WriteLine(sb.ToString());
}
```

#### AppendJoin

```c#
private static void RunAppendJoin()
{
    string[] words = { "I", "Love", "Metigator" };
    var sb = new StringBuilder();
    sb.AppendJoin('°', words);
    Console.WriteLine(sb.ToString());
}
```

#### AppendFormat

```c#
private static void RunAppendFormat()
{
    string customer = "Issam A";
    DateTime shippingDate = DateTime.Now; // yyyy-MM-dd hh:mm
    DateTime expectedDelivery = shippingDate.AddDays(7); // yyyy-MM-dd hh:mm
    decimal shippingCost = 29.99m;

    var sb = new StringBuilder();

    sb.AppendFormat(
        "\nDear {0}.," +
        "\n\nAt {1:t} on {1:D}, the order is on its way to you" +
        "\nIt's expected to be delivered at {2:t} on {2:D}, the order is on its way to you" +
        "\nShipping cost {3:c}." +
        "\n\t\t\tThanks for shopping with us!",

        customer, shippingDate, expectedDelivery, shippingCost);
    //   0           1              2                3
    Console.WriteLine(sb.ToString());
}
```

#### AppendLine

```c#
private static void RunAppendLine()
{
    var sb = new StringBuilder();

    sb.AppendLine("C# is a modern, object-oriented, type-safe programming language");
    sb.AppendLine("C# enables developers to build secure and robust applications");
    sb.AppendLine("C# has its roots in the C family of languages ");
    Console.WriteLine(sb.ToString());
}
```

#### Insert

```c#
private static void RunInsert()
{
    var sb = new StringBuilder("C# is a modern, object-, type-safe programming language");

    sb.Insert(23, "oriented");

    Console.WriteLine(sb.ToString());
}
```

#### Replace

```c#
private static void RunReplace()
{
    var sb = new StringBuilder();

    // Append Return StringBuilder, useful method chaining
    sb.Append("Fetigator");

    Console.WriteLine("before replace..");
    Console.WriteLine(sb.ToString());

    sb.Replace("Fetigator", "Metigator");

    Console.WriteLine("after replace..");
    Console.WriteLine(sb.ToString());
}
```

#### Remove

```c#
private static void RunRemove()
{
    var sb = new StringBuilder();

    // Append Return StringBuilder, useful method chaining
    sb.Append("Metigator xyx");

    Console.WriteLine("before remove..");
    Console.WriteLine(sb.ToString());

    sb.Remove(9, 4);

    Console.WriteLine("after remove..");
    Console.WriteLine(sb.ToString());
}
```

#### Clear

```c#
private static void RunClear()
{
    var sb = new StringBuilder();

    // Append Return StringBuilder, useful method chaining
    sb.Append("Metigator");

    Console.WriteLine("before clear..");
    Console.WriteLine(sb.ToString());

    sb.Clear();

    Console.WriteLine("after clear..");
    Console.WriteLine(sb.ToString());
}
```

#### GetChuncks

```c#
private static void RunGetChuncks()
{
    var sb = new StringBuilder();

    sb.Append("I Love Metigator");

    sb.Append("Youtube Channel");

    var counter = 1;
    foreach (var chunk in sb.GetChunks())
    {
        Console.WriteLine($"chunck #{counter++}: \"{chunk}\" length: {chunk.Length}");
    }
}
```

#### InsureCapacity

```c#
private static void RunInsureCapacity()
{

    var sb = new StringBuilder(10);

    Console.WriteLine("before sb.EnsureCapacity(12)");
    Console.WriteLine(sb.Capacity); // 10

    Console.WriteLine("after ensuring capacity");

    // If the current capacity is less than the capacity
    // parameter, memory for this instance is reallocated
    // to hold at least capacity number of characters; otherwise,
    // no memory is changed.

    sb.EnsureCapacity(8);

    Console.WriteLine("after sb.EnsureCapacity(12)");
    Console.WriteLine(sb.Capacity); // 12



}
```

#### CopyTo

```c#
private static void RunCopyTo()
{
    var sb = new StringBuilder("Metigator");
    char[] characters = new char[sb.Length];
    sb.CopyTo(0, characters, 0, sb.Length) ;
    Console.WriteLine(characters);

}
```

#### CharAtIndex

```c#
private static void RunCharAtIndex()
{
    var sb = new StringBuilder("Metigator");
    var firstChar = sb[0];
    Console.WriteLine(firstChar);

}
```

Be caution when using it the complicity could be `n^2`

as there is linked list

## 046 Tuple

- Data

  - [Github](https://github.com/metigator/CSharp046/tree/master)
  - [Watch Youtube Video](https://www.youtube.com/watch?v=+&list=PL4n1Qos4Tb6SWPbJNpiznp-Ok4A8J_23l&index=47)

- Content

### To Know

```
-- Collection
    |
    |--- Mutable
    |      |
    |      |--- Strongly Type
    |      |     |
    |      |     |--- array `int[]`
    |      |     |
    |      |     |--- List `List<int>`
    |      |
    |      |--- Weakly Type
    |      |     |
    |      |     |--- array list `ArrayList`
    |
    |--- Immutable
    |      |
    |      |--- Strongly Type
    |      |      |
    |      |      |--- Tuple
```

```c#
// array reference type (list with fixed size)
int[] array = { 50, 10, 23, 1, 7, -4 };

// list represents a dynamically-sized list generally contageous
List<int> list = new List<int> { 50, 10, 23, 1, 7, -4 };

list.AddRange(list); // { 50, 10, 23, 1, 7, -4, 50, 10, 23, 1, 7, -4 };


// collection
ArrayList al = new ArrayList { "50", 10, 23.2m, DateTime. Now };

// In .NET Framework new Data Structure is introduced System. Tuple

Tuple<int, int, int, int, int, int> tuples1 = new Tuple<int, int, int, int, int, int>(50, 10, 23, 1, 7, -4);

Tuple<int, int, int, int, int, int> tuples2 = Tuple.Create(50, 10, 23, 1, 7, -4);

Tuple<string, decimal> distances = Tuple.Create("hospital", 2.5m);
```

### Returning Multiple Values

```c#
public static class FacilityDistanceCalculator
{
    private static Random random = new Random();
    public static Location GetFacilityLocationInfoV1(string facilityName)
    {
        return new Location
        {
            Name = facilityName,
            DistanceInKm = random.NextDouble() * 10.0
        };
    }

    public static void GetFacilityLocationInfoV2(
        string facilityName, out string name, out double distanceInKm)
    {
        name = facilityName;
        distanceInKm = random.NextDouble() * 10.0;
    }
}
```

```c#
public class Location
{
    public string Name { get; set; }
    public double DistanceInKm { get; set; }

    public override string ToString()
    {
        return $"{Name} ....... {DistanceInKm.ToString("F2")} km";
    }
}
```

### Tuple class `Tuple<T1,...>`

`.Net 4`

```c#
public static class FacilityDistanceCalculator
{
    private static Random random = new Random();
    public static Tuple<string, string> CalculateFacilityDistance(string facilityName)
    {
        return Tuple.Create(facilityName, ($"{(random.NextDouble() * 10.0).ToString("F2")} km"));
    }

    public static Tuple<string, string> CalculateFacilityDistanceV2(string facilityName)
    {
        return new Tuple<string, string>(facilityName, ($"{(random.NextDouble() * 10.0).ToString("F2")} km"));
    }

    public static Tuple<string, double> CalculateFacilityDistanceV3(string facilityName)
    {
        return Tuple.Create(facilityName, random.NextDouble() * 10.0);
    }
}
```

- Tuple
  - Applies equality
  - Immutable

### Value Tuple

#### Tuple

- .NET framework 4.0

- Class
- Reference Type
- Heap memory

```c#
Tuple<string, double> t1 = new Tuple<string, double>("Hospital", 2.4);
Console.WriteLine($"t1: {t1}");
```

#### ValueTuple

- .NET framework 4.7.1
- .NET Core 2.0

- Struct
- Value Type
- Stack Type

- Increase readability

```c#
ValueTuple<string, double> t2 = new ValueTuple<string, double>("Hospital", 2.4);
Console.WriteLine($"t2: {t2}");
```

- Implicit Names
- Explicit Names

```c#
public static class FacilityDistanceCalculator
{
    private static Random random = new Random();

    // ValueTuple.Create
    public static ValueTuple<string, string> CalculateFacilityDistance(string facilityName)
    {
        return ValueTuple.Create(facilityName, $"{(random.NextDouble() * 10.0).ToString("F2")} km");
    }

    // Implicit Names
    public static (string, string) CalculateFacilityDistanceV2(string facilityName)
    {
        return ValueTuple.Create(facilityName, $"{(random.NextDouble() * 10.0).ToString("F2")} km");
    }

    // Explicit Names
    public static (string Name, string distanceInKm) CalculateFacilityDistanceV3(string facilityName)
    {
        return ValueTuple.Create(facilityName, $"{(random.NextDouble() * 10.0).ToString("F2")} km");
    }
}
```

```c#
static void Main()
{
    Tuple<string, double> t1 = new Tuple<string, double>("Hospital", 2.4);
    Console.WriteLine($"t1: {t1}");

    ValueTuple<string, double> t2 = new ValueTuple<string, double>("Hospital", 2.4);
    Console.WriteLine($"t2: {t2}");

    var t3 = FacilityDistanceCalculator.CalculateFacilityDistance("Hospital");
    Console.WriteLine($"t3: {t3}");

    var t4 = FacilityDistanceCalculator.CalculateFacilityDistanceV2("Hospital");
    Console.WriteLine($"t4: {t4}");
    Console.WriteLine($"FacilityName: {t4.Item1}");

    var t5 = FacilityDistanceCalculator.CalculateFacilityDistanceV3("Hospital");
    Console.WriteLine($"t5: {t5.Name}");
    Console.WriteLine($"t5: {t5.distanceInKm}");
}
```

### Deconstruction of Tuples

```c#
(string nm, string ds) = t5;

Console.WriteLine($"name: {nm}");
Console.WriteLine($"distance: {ds} km");
```
