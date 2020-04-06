# JSLearningJournal.com
JS Learning Journal For Beginners

VARIABLES:

// Rule 1. You can't define a variable more than once
// Rule 2. Variables must start with letters, only the dollar sign and underscore can be used as special symbols
// Rule 3. Names cannot be reserved keywords

BOOLEAN:

// ==== is the equality operator
// !== not equal operator
//< or > less than or greater than
// >== less than or equal to
// <== more than or equal to

BOOLEAN ExErCiSe 1:

// Program an amusement park discount for children younger than 7 and seniors over 65.

let age = 55;
let isChild = age <= 7;
let isSenior = age >= 65;
let discount = isChild || isSenior;
console.log(discount);

IF STATEMENT EcErCiSe 1:

// Program an automatic response that lets the client know if they receive a child or senior discount.

if (age <= 7) {
console.log('You get the child\'s discount! Yay!');
};
if (age >= 65) {
console.log('You get the senior\'s discount! Yay!');
};

IF ELSE STATEMENT ExErCiSe 1:

// Program a message that says whether the temperature is too hot, freezing, or just right.

let temp = 45;
let weather = 10;
if (weather === temp) {
console.log('Go for it. It is pretty nice.');
} else if (weather > temp) {
console.log('It is hot outside');
} else {
console.log('It is freezing outside!');
};

LOGICAL AND OR OPERATORS ExErCiSe 1:

// Program a message that tells the server what kind of meal to offer clients who might be vegan

let isGuestOneVegan = true;
let isGuestTwoVegan = false;
if (isGuestOneVegan === isGuestTwoVegan) {
console.log('Only offer up vegan dishes.')
} else if (isGuestOneVegan || isGuestTwoVegan) {
console.log('Make sure to offer some vegan options.')
} else {
console.log('Offer up anything on the menu.')
};

ARGUMENTS ExErCiSe 1:

//Program a tip calculator with a default tip of .20

let tipAmount = function (totalBill, tipDefault = .20) {
return totalBill * tipDefault;
};
let results = tipAmount(1000);
console.log(results);

WHILE LoOpS:
// In a small town the population is p0 = 1000 at the beginning of a year. The population regularly increases by 2 percent per year and moreover 50 new inhabitants per year come to live in the town. How many years does the town need to see its population greater or equal to p = 1200 inhabitants?

At the end of the first year there will be: 
1000 + 1000 * 0.02 + 50 => 1070 inhabitants

At the end of the 2nd year there will be: 
1070 + 1070 * 0.02 + 50 => 1141 inhabitants (number of inhabitants is an integer)

At the end of the 3rd year there will be:
1141 + 1141 * 0.02 + 50 => 1213

It will need 3 entire years.
More generally given parameters:

p0, percent, aug (inhabitants coming or leaving each year), p (population to surpass)

the function nb_year should return n number of entire years needed to get a population greater or equal to p.

aug is an integer, percent a positive or null number, p0 and p are positive integers (> 0)

Examples:
nb_year(1500, 5, 100, 5000) -> 15
nb_year(1500000, 2.5, 10000, 2000000) -> 10
Note: Don't forget to convert the percent parameter as a percentage in the body of your function: if the parameter percent is 2 you have to convert it to 0.02.

function nbYear(p0, percent, aug, p) {
    const per = percent / 100
    let n = 0
    while (p0 < p) {
    p0 + ((p0 * per) + aug);
    n++
}  return n
}

ARRAYS MATH. :
// Create a function that returns the sum of the two lowest positive numbers given an array of minimum 4 positive integers. No floats or non-positive integers will be passed.

For example, when an array is passed like [19, 5, 42, 2, 77], the output should be 7.

[10, 343445353, 3453445, 3453545353453] should return 3453455.

function sumTwoSmallestNumbers(numbers) {  
 const a = Math.min(...numbers)
 const index = numbers.indexOf(a)
 const newArray = numbers.splice(index, 1)
 const b = Math.min(...numbers)
 return a + b
}

// OR

function sumTwoSmallestNumbers(numbers) {  
  numbers.sort((a,b) => a - b);
  return numbers[0] + numbers[1];
};

ARRAYS:

// I have the par value for each hole on a golf course and my stroke score on each hole. I have them stored as strings, because I wrote them down on a sheet of paper. Right now, I'm using those strings to calculate my golf score by hand: take the difference between my actual score and the par of the hole, and add up the results for all 18 holes.

For example:

If I took 7 shots on a hole where the par was 5, my score would be: 7 - 5 = 2
If I got a hole-in-one where the par was 4, my score would be: 1 - 4 = -3.
Doing all this math by hand is really hard! Can you help make my life easier?

Task Overview
Complete the function which accepts two strings and calculates the golf score of a game. Both strings will be of length 18, and each character in the string will be a number between 1 and 9 inclusive.

function golfScoreCalculator(parList, scoreList){
    result = 0;
    for (let i = 0; i < parList.length; ++i) {
        result += scoreList[i] - parList[i];
    }
    return result;
}

FIZZBUZZ:

for (var i=1; i <= 20; i++)
{
    if (i % 15 == 0)
        console.log("FizzBuzz");
    else if (i % 3 == 0)
        console.log("Fizz");
    else if (i % 5 == 0)
        console.log("Buzz");
    else
        console.log(i);
}

MATH.SQRT:
A square of squares
You like building blocks. You especially like building blocks that are squares. And what you even like more, is to arrange them into a square of square building blocks!

However, sometimes, you can't arrange them into a square. Instead, you end up with an ordinary rectangle! Those blasted things! If you just had a way to know, whether you're currently working in vain… Wait! That's it! You just have to check if your number of building blocks is a perfect square.

Task
Given an integral number, determine if it's a square number:

In mathematics, a square number or perfect square is an integer that is the square of an integer; in other words, it is the product of some integer with itself.

The tests will always use some integral number, so don't worry about that in dynamic typed languages.

var isSquare = function(n){
  if ((n % Math.sqrt(n)) === 0 || (n === 0)) {
  return true
}  else if ((n % Math.sqrt(n)) < 0) {
  return 'Negative numbers cannot be squares'
}  else {
  return false
}}
