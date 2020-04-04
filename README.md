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
