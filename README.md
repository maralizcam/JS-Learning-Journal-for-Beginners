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

