# Arrays
A array, also called a one-dimensional array is a data structure that holds a sequence of values all of the same type. Each component in an array is called an element, each element is indexed from left to right, starting with index 0 all that way to n-1 so each element can be specified without ambiguity . 

Array initialization looks like:

```
int n = 5;
//Where n is the size of our array,
double[] numbers = new double[n];
//This creates an empty array with a length of 5 

//To fill this array:
for (int i = 0; i < numbers.length; i++){
    numbers[i] = i + 1;
}
//this would give us an array of {1.0, 2.0, 3.0, 4.0, 5.0}
//This is great if the contents may be varying values 
```
Something like:
```
int[] originalArray = {1, 2, 3}; //This is great if you want the array to be more static 

```

This doesn't mean that you can't use either one for the same or different reasons, but just remember that Arrays cannot dynamically change size, in order to "change" the size of your array you would need to copy the contents to a new larger array. 


It's important to be **cautious** with the index of your arrays as if you try to refer or assign a value outside of an arrays bounds of 0 to n-1, you will recieve an IndexOutOfBoundsException

## Array of Arrays
Array of arrays, otherwise known as two-dimensional arrays, are arrays that contain other arrays. A normal one-dimensional array is indexed with a single integer, but a 2d array is indexed by two integers, a row and then column.


```
int[][] score = {
    {105, 90, 20},
    {55, 21, 33},
    {0, 7 , 2}
} // this is like a 3x3 grid or a matrix
//an array of arrays can also be created like: 

int[][] scores = new int[3][3]; // but this one is empty right now
//you can add to it like:
scores[0][1] = 99;
scores[0][0] = 100;
```

### Ragged Arrays 
There is no requirement that all rows in a two-dimensional array must be the same length, such arrays with nonuniform length are called ragged arrays.

This a a way of iterating through and printing a ragged array.
```
for (int i = 0; i < a.length; i++)
{
   for (int j = 0; j < a[i].length; j++)
      System.out.print(a[i][j] + " ");
   System.out.println();
}
```


## Shuffling and Exchanging 
Swapping the position of two elemenents in an array uses a procedure that looks something like: 
```
int temp = numbers[i]; //Temporarily store value of numbers at i
numbers[i] = digits[j]; //Swap value of numbers at i with value of digits at j 
digits[j] = temp; //Then assign digits at j to what we stored in temp

```

Shuffling uses this same idea:
```
public static void shuffle(int[] array){
        for(int i = array.length - 1; i > 0; i--){
            int j = (int) (Math.random() * (i + 1));

            int temp = array[i];
            array[i] = array[j];
            array[j] = temp;
        }
}
```
This is called the Fisher-Yates shuffle or Fisher-Yates algorithm.

# Input and Output
Input and output is the communication from outside world <-> computer, but sometimes input and output can also go from system to system without necessarily having a immediate direct output, like with piping commands in the cmdline. 

- Redirection: Changes where a stream of input/output comes from or goes to. (e.g. saving output to a text file instead of printing to the terminal)
- Piping ( | ): Feeding standard output of one program directly to anothers standard input of a program in the command line. 
## Inputs 

### Java Standard Library: Scanner
- Purpose: built in tool to read text from the terminal and parse it. 
- Methods: next(), nextInt(), nextDouble(), and nextLine()

### [Princeton's StdIn Library](https://introcs.cs.princeton.edu/java/stdlib/javadoc/StdIn.html#readDouble())
Customer library with a variety of methods to simplify standard input without the need to instantiate a Scanner.


## Output 

Outputs can come in many forms, but by default it usually outputs into the terminal. Writing to files is another common standard output, as well as standard error, an exclusive output channel for errors. 

Java has operations like ``System.out.print()``, ``System.out.println()``, and ``System.out.printf()``.


### [Princeton's StdOut Library](https://introcs.cs.princeton.edu/java/stdlib/javadoc/StdOut.html)

This library has a variety of methods for printing strings and numbers to standard output. 

They also have librarys for audio and drawing outputs. 


