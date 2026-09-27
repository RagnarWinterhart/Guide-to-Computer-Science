# Built-in Types of Data

## Primitive Types
These are the most often used primitive types:

| Type | Set of Values | Common operators | Literal Values |
| ---- | ------------- | ---------------- | -------------- |
| int  | integers      | +  -  *  /  %    | 99 12 21321312 |
| double | floating point numbers | + - * / | 3.14 2.0     |
| boolean | boolean values | && || !        | true false   | 
| char | characters    |                  | 'A' '1' '%' '\n' |
| String | sequences of characters | + | "AB" "hello" "15.1" |


### Terminology 
A line of code such as: 
```
int a, b, c;
```
Is a declaration statement, declaring the ``names`` of three variables with the ``type`` int. 
Statements such as: 
```
a = 42;
b = 2
c = a - b;
```
Are assignment statements. However something such as: 
```
int a = 10; // this is another way to declare a variable and assign value at the same time
int b = "hello world" // however this is incorrect
```

# Conditionals and Loops

## Conditionals 

### If Statements
One of the most foundation decision makers in computer science if statements decide based off given criteria ``If`` something happens at all, they also are often followed by an ``else`` which gives a block of funtion that happens if the conditions for ``If`` are not met.
```
if (a == b) {System.out.println("a is equal to b");}
else{System.out.println("a is not equal to b")}
```
If statements can be complex using multiple boolean resulting conditions at the same time (`` && ``) and in "either/or" scenarios (``||``)
### Switches
Useful for long conditon "ladder" situations where more than two conditions or variables must be compared or checked. 

```
int dayNmbr = 2;
String dayName;

switch (dayNmbr){
    case 1: dayName = "Sunday"' break;
    case 2: dayName = "Monday"' break;
    case 3: dayName = "Tuesday"' break;
    .
    .
    .
    default: dayName = "Invalid; break; //happens if the day number doesn't match
}
```
Switches are nice for single variable checks that need to be strictly equal to one other value. 

## Loops

### While Loops
While loops, loop until a set condition becomes false.

```
int count = 0;

while(count < 10){
    count++;
    System.out.println(count);
}

```
These loops are nice if there is a clear condition that will eventually become false and not risk looping infinitely. Can be nice for reading a file for example. 



### For Loops
For loops iterate until a set number of iterations have occurred. 
```
String[] fruits = {"apple", "banana", "orange"}

for (int i = 0; i < fruits.length; i++){
    System.out.println("At index " i + ": " + fuits[i]);
}

//Alternatively a for-each loop
for(String fruit : fruits){
    System.out.println(fruit); // can be simpler and more readable depending on situation
}
```