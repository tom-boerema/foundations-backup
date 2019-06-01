[Sprint 4 Home](README.md)|
---|

# Testing

## Summary

Testing is a hugely important and also rather large concept in coding. It is part of every coding language and has been around since coding began. As such, this means we can only briefly touch on some key concepts of testing this sprint.

## Timebox

Activity | Time|
------------|----------|
Learn | 30 minutes
Reflect | 10 minutes

## Description

Testing is how we know that code works. It's what tells us our code is reliable, that it isn't going to break and is actually doing what we want it to. We will often say that code that isn't tested, isn't complete yet.

During Foundations most of the testing you will be doing will be manual testing, running the code and seeing what results or using `console.log` to check what is happening. But not all testing is manual testing. We can instead write tests in our code that say, _when I tell this piece of code to run, this is what I expect to happen_. 

__For example:__ If we wanted to write a function that would greet someone when given their name, the test we would write might look something like:
```
function testGreeting(){
    var expected = "Kia ora Cam!"
    var actual = greeting("Cam")

    if (actual != expected) {
        console.log("It's broken..")
    } else {
        console.log("It works!")
    }
}
```

The function that passes this test would then be:
```
function greeting(name){
    return "Kia ora " + name + "!"
}
```
Two aspects of testing that we will see a lot of are Unit Testing and Test Driven Development. These help us write tests to ensure our code is reliable, but for now it is enough to get familiar with the concepts as we won't be asking you to write your own tests yet.

#### Unit Testing

Unit testing is a part of `functional programming` (the type of programming we are doing). As our code is divided into small individual functions that make up a larger programme, we need to test these small `units` of code to make sure each part is doing what we expect. 

Unit testing doesn't care if our whole project works as expected, but instead makes sure each of the functions within it does what we need them to. As we can rely on the small pieces of code, we can build our larger pieces on top of them knowing they are working correctly.

This method of unit testing means that, if we change something in our code, not only do we not have to manually test our large project to find out if it is broken, but the tests will also tell us where in our code this has happened if so.

#### Test Driven Development (TDD)

`TDD` is a particular way of doing code development as a whole. It involves starting with the big picture and writing your tests _before_ you write your code. 

This way of coding means you have to work out what you intend for the code to do and what smaller things need to happen to achieve this before jumping into writing it. Tests are then written that match this intent for your project.

Once the tests are written, you can then write the code that makes these tests pass. Because of this, TDD forgoes writing "nice" code, so long as it works to achieve the needs of the test. This also means we can try a number of different methods to achieve the same goal as it doesn't matter how we get there, just that we do. Once the code works we then go back and `refactor` it to make it more concise and readable.

## Reflect

In your `my-reflections-sprint-4` file, answer the questions under the `Testing` heading.

Commit and push the changes to GitHub.

#### Some interesting links:

[A crash course on testing](https://hackernoon.com/a-crash-course-on-testing-with-node-js-6c7428d3da02)\
[What is TDD and why should we care about it?](https://medium.freecodecamp.org/isnt-tdd-test-driven-development-twice-the-work-why-should-you-care-4ddcabeb3df9)\
[How to write a good Unit Test](https://medium.com/javascript-scene/what-every-unit-test-needs-f6cd34d9836d)
