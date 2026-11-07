# P and NP
P and NP are two classes of computational problems, though you could describe P as a subset of problems in NP. These classes describe how efficiently a computer can solve or verify problem. P stands for polynomial time, a problem is in P if an algorithm exists that can solve said problem in ploynomial time, meaning that it grows at a polynomial rate relative to the size of input. 

NP stands for Nondeterministic Polynomial Time, a problem is in NP if it can be verified in polynomial time. This doesn't mean that finding the solution is an easy undertaking, but that once a proposed solution is reached that solution can be verified efficiently. 


The reason we say that P is a subset in NP is because if a computer can solve a problem effectively then it certainly can verify its solution, though whether every problem in NP is in P is not known.


## Halting problem
```
Theorem. (Turing, 1937) The halting problem is unsolvable.

Proof sketch: Suppose, for the sake of proving a contradiction, that a function halts(f,x) exists as described previously. Our first step is to create a new function strange() that takes as input a single function f (encoded as a string), and calls halts(), as follows:


public static boolean strange(String f)
{
   if (halts(f, f))
      while (true) /* infinite loop */ ;
}

It may seem strange to call halts(f,f) to check whether a program halts when given itself as input; we do so solely as a device in the proof. But it is actually not that strange: for example, imagine that the designer of a compiler wishes to check that it does not go into an infinite loop when compiling itself.

What does strange() actually do? Recall that halts(f, x) returns true if f(x) halts and false if f(x) does not halt, where we use the term “halt” to mean “does not enter into an infinite loop.” Therefore, examining the code:

• If f(f) halts, then strange(f) does not halt.

• If f(f) does not halt, then strange(f) halts.

Now, we perform the crucial step: What happens when we call strange() with itself (encoded as a string) as input? That is, we replace f by strange in the above two statements, leaving the following two (strange) statements:

• If strange(strange) halts, then strange(strange) does not halt.

• If strange(strange) does not halt, then strange(strange) halts.

Both statements are contradictions, an absurdity, leaving us with the conclusion that our hypothetical function halts(f, x) does not exist. That is, the halting problem is unsolvable!

```
—Textbook: Computer Science
(Robert Sedgewick; Kevin Wayne)


Essentially the halting problem is: given an arbitrary compuer program and an input, can you write a general algorithm that decides if the program will eventually stop running/finish or if it will loop forever. 

