# Recursion 

>During this exercise, I delved deep into the concept of recursion—a technique where a function calls itself in order to solve problems.

## The Challenge
For the sprint, I was tasked with reimplementing certain parts of the browser that involve recursion. The trick? Not using any built-in shortcuts or functionalities that would make the problem trivial. This exercise reminded me of "polyfills"—a term used to describe reimplementing new browser functionalities in older browsers.


## What I Learned
One of the core takeaways was understanding how smaller parts of a problem can reflect the larger problem as a whole when using recursion. This became evident when I dissected the function eat:

```
var eat = function(meal){
  console.log('meal before bite:', meal);
  console.log('now eating', meal.pop());
  if(meal.length){
    eat(meal);
  } else {
    console.log('done with the meal!');
  }
}
```

The output for `eat(['soup', 'potatoes', 'fish'])` illustrated the step-by-step recursive processing of the array until it was empty.

## Fixing Broken Tests
An additional layer of complexity was the broken test suite. My objective was not only to understand and fix the tests but also to make them pass by implementing the missing functionalities. This required me to become familiar with two key testing tools: Mocha and Chai.

Mocha: A test framework that I used to structure the test files. It ran the tests and reported the results.
Chai: This was an assertion library that enriched the expressiveness of my tests and made the error messages more insightful.
It was crucial for me not to reference the previous test suite. Instead, I relied heavily on the Mocha and Chai documentation to navigate through the exercise.


## Bare Minimum Requirements
1. Replacing stringifyJSON with my own function in src/stringifyJSON.js and ensuring the specs passed.</br>
2. Implementing getElementsByClassName in src/getElementsByClassName.js and, again, ensuring the specs passed. I made use of document.body, element.childNodes, and element.classList to accomplish this.
To test everything, I ran npm start from the sprint's root directory and subsequently opened the SpecRunner.html file in my browser.

## Conclusion
This exercise was not only about understanding recursion but also about familiarizing myself with testing tools and problem-solving. It was a challenging yet rewarding experience that honed my skills and deepened my appreciation for recursion and browser functionalities.
