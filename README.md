![Image description](https://i1.faceprep.in/ProGrad/face-logo-resized.png)

# ProGrad Lab | Higher Order Function

In the previous lesson, we have learnt some useful Higher Order Functions to manipulate arrays & objects. Now, let's put them to use in this lab.

## What should you do
```
Fork this repo
Clone this repo
Practice JavaScript - Higher order functions
```

## How To Submit
```
Upon completion, run the following commands:

git add .
git commit -m "ProGrad ID"
git push origin master

And finally, create a pull request so your ProGrad Mentor (PM) can review your work.
```

## Tests

Open the `SpecRunner.html` file on your browser and start coding to pass the test. Remember to focus on one test at a time and read carefully the instructions to understand what should be done.

### Function #1: Array Slice

Take an example array. We will be using the below array for reference.
```
const foods = [pizza, burger, fingerChips, donuts, springRoll];

solution:
const food=["pizza", "burger", "fingerShips", "donuts", "springRoll"];
undefined
food.splice(2,0,"noodles","icecream")
[]
console.log(food)
VM248:1 (7) ["pizza", "burger", "noodles", "icecream", "fingerShips", "donuts", "springRoll"]

```
Create a new array named as `modifiedFood` and also create a `slice()` method.The `slice()` method should return the selected elements in an array, as a new array object. This method starts slicing the array from the given start argument and ends the slicing operation one element before the given second argument.

```
co

Expected output: [burger, fingerShips, donuts]
```
solution:
const food=["pizza", "burger", "fingerShips", "donuts", "springRoll"];
var modifiedfood=food.slice(1, 4);
console.log(modifiedfood)
[burger, fingerShips, donuts]

### Function #2: Array Splice

The splice() method adds/removes items to/from an array, and returns the removed item(s).

Take an example array. Create a new array named as `modifiedFood` and use `splice()` to get the below expected output. Elements are added to the original array.

```
const foods = [pizza, burger, fingerShips, donuts, springRoll];

Expected output: [pizza, burger, noodles, icecream, fingerShips, donuts, springRoll];
```
solution:
const food=["pizza", "burger", "fingerShips", "donuts", "springRoll"];
undefined
food.splice(2,0,"noodles","icecream")
[]
console.log(food)
VM248:1 (7) ["pizza", "burger", "noodles", "icecream", "fingerShips", "donuts", "springRoll"]
 2)
const food=["pizza", "burger", "fingerShips", "donuts", "springRoll"];
var modified11=food.splice(2)
undefined
console.log(modified11)
VM785:1 (5) ["noodles", "icecream", "fingerShips", "donuts", "springRoll"]
undefined

### Function #3: Filter

Filter is an array method. It accepts a test function as an argument and returns a new array with only the elements for which the test function returns true.

Now, create a function `isEven()` which takes `numberArray` as argument and _returns all even numbers from the given array_.

```
Take numberArray as

const numberArray = [12,324,213,4,2,3,45,4234];
var evennumbers = numberArray.filter(function(num){ return num&2; });
undefined
console.log(evennumbers)
VM1252:1 (3) [2, 3, 4234]

```

Next, let's build on top of this. Create another functon called `isPrime()` with takes same `numberArray` as argument and _returns all prime numbers from the above given array_.


### Function #4: Reject

We can now reuse the `isPrime()` function in conjunction with reject to get all the non-prime numbers in the array. The reject function does the opposite of the filter function. It returns an array with all the elements that do not satisfy the condition.

Create a function `nonPrime()` which takes `numberArray` as argument and _return all non-prime numbers from the above given array in Function #3_.
var numArray = [12,324,213,4,2,3,45,4234]

numArray = numArray.filter((number) => {
  for (var i = 2; i <= Math.sqrt(number); i++) {
    if (number % i === 0) return false;
  }
  return true;
});
(2) [2, 3]

### Function #5: Lambda

When defining short functions, it's convenient to use an alternative syntax called lambda function that allows us to define anonymous functions in a more compact way: _( /*arguments*/ ) => { /*code*/ }_. If our function is only a return statement, we can even strip the curly brackets and avoid writing return: _( /*arguments*/ ) => /*value to return*/_.

Now, rewrite the function `isEven()` by using the concept of Lambda Function.

const numberArray = [12,324,213,4,2,3,45,4234];
var evennumbers = numberarray.reduce(function(num){ return num&2; });
undefined
console.log(evennumbers)
VM1252:1 (3) [2, 3, 4234]
### Function #6: Map

Another very useful higher order function is map. It takes a function and applies it to all the elements of an array.
The syntax is identical to `filter`.

Now, create a function `findSquareOfNumbers()` which takes the following array called `myArray` as argument and _returns square value of all elements in the given array_.

```
const myArray = [11, 34, 20, 5, 53, 16];
```
const numberArray4 = [11, 34, 20, 5, 53, 16];
var squareroot = numberArray4.map(function(num){ return num*num });
undefined
console.log(squareroot)
VM302:1 (6) [121, 1156, 400, 25, 2809, 256]
### Function #7: Reduce

Reduce is the last higher order function we are going to discuss and it's also the most powerful one. In fact, you can implement any list transformation operation with reduce.

Reduce takes a callback function and a starting value. The callback function takes as arguments an accumulator and the value of the current element of the array and returns the accumulator to be used in the next cycle. The values returned from the last call of the callback function is the value returned by `reduce`.

Create a function `multiply()` which takes an argument of `myArray` which holds the values as `[2, 3, 5, 10]` and _returns multiplication value of all numbers in the given array_.

Let's expand our knowledge by `implementing map with reduce`.

const numberArray8 = [2, 3, 5, 10];
var mulitiply = numberArray8.reduce(function(num){ return num*num });
undefined
console.log(mulitiply)
256

Take the function explained in the above task of `map` and try is by implementing the same by using `reduce`.

Happy Coding ProGrad ❤️
