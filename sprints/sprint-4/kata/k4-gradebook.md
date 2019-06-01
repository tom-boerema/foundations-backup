[Sprint 4 Home](../README.md) | [Kata Page](../t6-js-kata.md)|
---|---|

# A Gradebook from Names and Scores

## Learning Competencies
- Define local variables in JavaScript
- Define functions in JavaScript
- Create, add properties to, delete properties from, and access values in object literals

Activity | Time|
------------|----------|
Kata | 8 hours
Reflect | 10 minutes

## Summary
In this challenge you will be taking your knowledge of JavaScript to the next level! Assume there is a teacher with a list of students and a list of their respective test scores.  The teacher is providing you with this data which looks like ...

```javascript
var students = ["Joseph", "Susan", "Wiremu", "Elizabeth"]

var scores = [ [80, 70, 70, 100],
               [85, 80, 90, 90],
               [75, 70, 80, 75],
               [100, 90, 95, 85] ]
```

You will take this data and transform it into a gradebook.  The gradebook will be a JavaScript object.

## [Repl.it](https://repl.it/@devacademy)
Making sure you are logged into your account, navigate to the [JS Gradebook](https://repl.it/@devacademy/JS-Gradebook) challenge. Starting the challenge will then fork it to your own account.

## Get Coding!

Follow the steps below to make the tests pass and complete the challenge.  The order of the steps
corresponds to the order of the tests. After completing each step, run the code to check it has passed the test.

In the past, you had the option of using dot notation or bracket notation. In this challenge some properties need the bracket notation to be referenced correctly. Find out why in this [medium article](https://medium.com/@prufrock123/js-dot-notation-vs-bracket-notation-797c4e34f01d) on dot vs. bracket notation.

----

#### Create your `gradebook`
Create a variable `gradebook` and assign it the value of an empty object.

#### Add a property to `gradebook`
Make each student name in `students` a property of `gradebook` and assign each the value of a new object.

#### `testScores`
Give each `student` property of `gradebook` its own `testScores` property and assign it the value of the respective students scores from scores.

#### `addScore`
Create an `addScore` function that accepts `gradebook`, `name` and `score` arguments.

Have `addScore` push the score to the value of the `testScore` property that matches the value of the `name` argument in the given `gradebook`.

For example,
```javascript
    addScore(gradebook, "Susan", 80) // would push the score 80 into the value of gradebook.Susan.testScores
```

#### Create the function `average`
Have `average` accept an array of integers and return the average of those integers.

#### `getAverage`
Create a `getAverage` function so that it accepts a `name` as a String (e.g., "Joseph") and returns that student's average score. Use the average function you created in the last step as part of this function.

## Reflection
Navigate to your `my-reflections-sprint-4` file and answer the question under the heading `JavaScript Gradebook`.

Commit and push your changes to GitHub.
