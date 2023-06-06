# 14.6DestructingExercise

**What does the following object destructuring code return/print?**
ANSWER:  8, 1846

let facts = {numPlanets: 8, yearNeptuneDiscovered: 1846};
let {numPlanets, yearNeptuneDiscovered} = facts;

console.log(numPlanets); // 8
console.log(yearNeptuneDiscovered); // 1846

**What does the following object destructuring code return/print?**
ANSWER:  { yearNeptuneDiscovered: 1846, yearMarsDiscovered: 1659 }

let planetFacts = {
  numPlanets: 8,
  yearNeptuneDiscovered: 1846,
  yearMarsDiscovered: 1659
};

let {numPlanets, ...discoveryYears} = planetFacts;

console.log(discoveryYears); // { yearNeptuneDiscovered: 1846, yearMarsDiscovered: 1659 }

**What does the following object destructuring code return/print?**
ANSWER:
"Your name is Alejandro and you like purple"
"Your name is Melissa and you like green"
"Your name is undefined and you like green"
function getUserData({firstName, favoriteColor="green"}){
  return `Your name is ${firstName} and you like ${favoriteColor}`;
}

getUserData({firstName: "Alejandro", favoriteColor: "purple"}) // "Your name is Alejandro and you like purple"
getUserData({firstName: "Melissa"}) // "Your name is Melissa and you like green"
getUserData({}) // "Your name is undefined and you like green"

**What does the following array destructuring code return/print?**
ANSWER:  "Maya" "Marisa" "Chi"

let [first, second, third] = ["Maya", "Marisa", "Chi"];

console.log(first); // Maya
console.log(second); // Marisa
console.log(third); // Chi

**What does the following array destructuring code return/print?**
ANSWER:
Raindrops on roses 
whiskers on kittens
["Bright copper kettles", "warm woolen mittens", "Brown paper packages tied up with strings"]

let [raindrops, whiskers, ...aFewOfMyFavoriteThings] = [
  "Raindrops on roses",
  "whiskers on kittens",
  "Bright copper kettles",
  "warm woolen mittens",
  "Brown paper packages tied up with strings"
]

console.log(raindrops); // Raindrops on roses 
console.log(whiskers); // whiskers on kittens
console.log(aFewOfMyFavoriteThings); /*
(3) ['Bright copper kettles', 'warm woolen mittens', 'Brown paper packages tied up with strings']
0: "Bright copper kettles"
1: "warm woolen mittens"
2: "Brown paper packages tied up with strings"
length: 3
[[Prototype]]:  Array(0)

**What does the following array destructuring code return/print?**
ANSWER:  [10, 30, 20]

let numbers = [10, 20, 30];
[numbers[1], numbers[2]] = [numbers[2], numbers[1]]

console.log(numbers) /*  
(3) [10, 30, 20]
0: 10
1: 30
2: 20
length: 3
[[Prototype]]: Array(0)
*/

**Write an ES2015 version of the code shown below.**

var obj = {
  numbers: {
    a: 1,
    b: 2
  }
};

var a = obj.numbers.a;
var b = obj.numbers.b;

ES2015 (ES6) version:
const obj = {
  numbers: {
    a: 1,
    b: 2
  }
};

const { a, b } = obj.numbers;

**Write an ES2015 one-line array swap with destructuring version of the code shown below.**
var arr = [1, 2];
var temp = arr[0];
arr[0] = arr[1];
arr[1] = temp;

ANSWER:
let arr = [1, 2];
[arr[0], arr[1]] = [arr[1], arr[0]];

**Write a one line function called raceResults which accepts a single array argument and uses the following to produce the result:
•  an arrow function
•  destructuring 
•  ‘Enhanced’ object assignment (same key/value shortcut) 
By using the code shown below, the solution should return an object with the keys first, second, third, and rest.**

ANSWER:
const raceResults = (arr) => ({ first, second, third, ...rest } = arr);





