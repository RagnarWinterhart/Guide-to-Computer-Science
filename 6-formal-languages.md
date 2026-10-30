# Formal Languages

## Definitions 
It is best to think of a symbol as a digit or character. 


``alphabet`` is a finite set of symbols


``string`` is a finite set of alphabet symbols


``formal language`` is a set of strings that is possibly infitite, all over the same alphabet

## Specification and Recognition Problem

### Specification Problem
How do we completely and precisly define formal languages? 

Sometimes this is more easily addressed with certain classes of formal languages.

### Recognition Problem
Once there is a way to specify the language there arrives another problem: given a language L and a string x, is x in L, or not?

## Regular Expressions
Sequences of characters that make a specific search pattern, that can be used to find, match, extract, or replace text within strings, docs, and code. 

Characters:

``.`` matches any single character except a newline

``\d`` matches any single digit

``\w`` matches any word character

``\s`` matches any whitespace character

``[abc]`` matches any single character listed inside brackets

``|`` find match for any one of the patterns separated by | 

Quatifiers: 

``*`` matches zero or more times

``+`` matches one or more times 

``?`` matches zero or one time

``{n,m}`` matches between n and m times

## DFA (Deterministic Finite Automaton)
A DFA is a state machine where for any given state and an input symbol there is exactly one next state it can move to.

The machine reads input one character at a time, from its current state it looks at the character and move to the designated next state based off said character. 
It makes no choices, there's no guess work and no transitions that are empty. If the machine finishes reading the sting and is in its accepted state then the string is valid.



## NFA (Nondeterministic Finite Automaton)
An NFA is a state machine where for any given state and input symbol there are either multiple or no next states it can go to.

When there are multiple choices the NFA chooses all paths simultaneously, and if any of those paths are successful in reaching an accepting state, the string is valid. This allows for more guessing and branching. 

NFA's also allow for something called epsilon transition which is a state change that happens without any input symbol in the string.