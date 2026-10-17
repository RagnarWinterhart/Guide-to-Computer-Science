# Object Oriented Programming
_"whenever you can clearly separate data and associated tasks within a computation, you should do so."_ 
—Textbook: Computer Science
(Robert Sedgewick; Kevin Wayne)

Object-oriented programming organizes code around objects and data rather than pure functions and logic. Involving 4 pillars of OOP encapsulation, abstraction, inheritance, and polymorphism.  
## Using Data Types
A data type defines:

- The possible data or values an object can have/store.
- The operations that can be done to that data.

Objects are created from classes using constructors, usage like: CustomDate first = new CustomDate(10, 17, 2026);

Methods can then be called on the object:
first.getDayOfWeek();

Primitive types such as int and boolean are built into Java, while classes allow custom types to be defined.

## Creating Data Types
A class usually contains:
- Instance variables store the state of an object. Each instance of a class maintains its own value.
- Constructors initialize new objects.
- Methods define operations the object can perform.
```
public class CustomDate {
    private int month, day, year;

    public CustomDate(int month, int day, int year){
        this.month = month;
        this.day = day;
        this.year = year;
    }
}
```
Each CustomDate object gets its own copy of month, day, and year.
The keyword `this` refers to the current object:
this.month = month;

this.month is the object's field while month is the constructor parameter.

## Designing Data Types
A good data type groups together related state and behavior while hiding unnecessary implementation details.
Fields are commonly made private so outside code cannot directly modify an object's internal state:
`private int balance;`

Public methods provide the interface for interacting with the object, and can be called outside their class. For example a GUI class could call:
- `machine.insertCoin();`
- `machine.buy(25);`
- `machine.getChange();`
as effects for UI buttons.

Things to ask when designing a data type:
- What minimum amount of information is necessary for an object to store?
- What operations naturally belong to that object?
- What details or operations should be private, or what shouldn't be accessed from outside?
- Can calculated information be derived each time or should it instead be stored?

Helper methods are another way to break operations into smaller more resuseable pieces. They usually are made private so they can only be used internally. 


