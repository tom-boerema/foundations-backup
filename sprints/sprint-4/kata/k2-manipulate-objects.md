[Sprint 4 Home](../README.md) | [Kata Page](../t6-js-kata.md)|
---|---|

# Manipulating JavaScript Objects

## Learning Competencies
- Define local variables in JavaScript
- Create, add properties to, delete properties from, and access values from JavaScript Object literals
- Use pre-written tests to drive development

Activity | Time|
------------|----------|
Kata | 4 hours
Reflect | 10 minutes

## Summary
In this challenge you will work with the following JavaScript object that has been assigned to the variable `terah`. You will have to complete each task without modifying the object itself. That means everything must be done outside of the curly braces.

```javascript
var terah = {
  name: "Terah",
  age: 32,
  height: 66,
  weight: 130,
  hairColor: "brown",
  eyeColor: "brown"
}
```

## [Repl.it](https://repl.it/@devacademy)
Making sure you are logged in to your account, navigate to the [Manipulating JS Objects](https://repl.it/@devacademy/Manipulating-JS-Objects) challenge. Starting the challenge will then fork it to your own account.

## Run the tests 
Run the code on your forked repl.it challenge. All tests will log `true` in the console when they pass -- `false`, otherwise.

## Pass the Tests
The steps below match the order of the tests you will need to complete. After completing each step, run your code to be certain that the next test has passed. Note that each step should build on __but not modify__ any of the code before it.

1. Define a variable `adam` and use object literal notation to assign this variable the value of an object with no properties.

2. Give `adam` a name property with the value "Adam".

3. Add a spouse property to `terah` and assign it the value of `adam`.

4. Change the value of the `terah` weight property to 125.

5. Remove the eyeColor property from `terah`.

6. Add a spouse property to `adam` and assign it the value of `terah`.

7. Add a children property to `terah` and and use object literal notation to assign
 this variable to an empty object.

8. Add a `carson` property to the value of the `terah` children property. `carson` should be an object with a property `name` with the value "Carson".

9. Add a `carter` property to the value of the `terah` children property. `carter` should be an object with a property `name` with the value "Carter".

10. Add a `colton` property to the value of the `terah` children property. `colton` should be an object with a property `name` with the value "Colton".

11. Add a children property to `adam` and assign it the value of `terah.children`.


When all of the tests have passed, your final `terah` object will be logged to the console.

## Reflection
Navigate to your `my-reflections-sprint-4` file and answer the questions under `Manipulating JavaScript Objects`.
