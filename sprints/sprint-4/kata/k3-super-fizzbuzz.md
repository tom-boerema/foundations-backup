[Sprint 4 Home](../README.md) | [Kata Page](../t6-js-kata.md)|
---|---|

# FizzBuzz (Super Edition)

## Learning Competencies
- Use strings, integers, arrays, functions
- Use if/else or switch statements, string methods, for loops

Activity | Time|
------------|----------|
Kata | 4 hours
Reflect | 10 minutes

## Summary:
FizzBuzz is a classic programming exercise (and fairly common interview question).

The usual example asks the developer to write a program which prints out each number from 1 to 100.  But for multiples of 3 print 'Fizz' instead of the number and for multiples of 5 print 'Buzz'.  For numbers which are multiples of both 3 and 5 print 'FizzBuzz'.

This exercise has a little twist.  Write a method called `super_fizzbuzz` which takes as its input an `Array` of integers.

It should loop over that array and then return a "fizzbuzzed" `Array`, i.e., the array is identical to the original, but with the following changes:

1. Multiples of `3` should be replaced with the string `"Fizz"`
2. Multiples of `5` should be replaced with the string `"Buzz"`
3. Multiples of `15` should be replaced with the string `"FizzBuzz"`
```
For example:

super_fizzbuzz([1,2,3])     // will return [1, 2, "Fizz"]
super_fizzbuzz([1,2,5])     // will return [1, 2, "Buzz"]
super_fizzbuzz([1,2,15])    // will return [1, 2, "FizzBuzz"]

super_fizzbuzz([30, 9, 20, 1])      // will return ["FizzBuzz", "Fizz", "Buzz", 1]
```

## [Repl.it](https://repl.it/@devacademy)
Making sure you are logged into your account, navigate to the [Super FizzBuzz](https://repl.it/@devacademy/Super-FizzBuzz) challenge. Starting the challenge will then fork it to your own account.

---

## Get Coding!
For this challenge, we're going to start by practicing our pseudocode. Before we can code complex functions, we first need to think through the steps we need them to do. This can take some time and brainpower to think through now, but saves you time when it comes to writing your code.

#### Plan your code
To start, think through what you need the function to do and write pseudocode comments for the steps your function will take. These comments will not be written in code but plain English, as if you were talking a friend through the steps.

#### Write your initial solution
Write code to match your pseudocode steps. You may find you have to do things in a different order than you originally wrote in your pseudocode, or add more steps in, and that's alright! The pseudocode is a first go, you don't have to match it exactly.

Once written, run the tests. If your initial solution passes all tests, move on to the next part.

## Reflection
Navigate to your `my-reflections-sprint-4` file and answer the questions under the heading `FizzBuzz (Super Edition)`.
