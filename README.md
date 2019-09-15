# JSEpisodeThree-Demo

[Slides](https://docs.google.com/presentation/d/1Jf6Dj5KhhUJZ-2sbSBAeLZb4ZeI5SxmfaBnvyNpqw2k/)

---

All demos should be done in `script.js` file of an [`HTML` repl](https://repl.it/languages/html)

### Code Blocks (Functional Programming)

BLOCK 01 (ASSIGNING TO VARIABLE)

```javascript
let hello = function() {
  console.log("Hello!");
};

hello();
```

BLOCK 02 (PASSING FUNCTION AS ARGUMENT)

```javascript
// Simple
function runMe(fn) {
  fn();
}

runMe(hello);

// Complete
hello = function(name) {
  console.log(`Hello ${name}`);
};

const formal = function(name) {
  console.log(`Greetings ${name}`);
};

const informal = function(name) {
  console.log(`Yo ${name}`);
};

function greeting(greetFn, name) {
  greetFn(name);
}

greeting(hello, "Asis");
greeting(formal, "Mishmish");
greeting(informal, "Hamsa");

// Anonymous Function
greeting(function(name) {
  console.log(`こんにちは ${name}`);
}, "Lailz");
```

BLOCK 03 (RETURNING A FUNCTION)

```javascript
function makeGreeter() {
  return function(name) {
    console.log(`Hello ${name}`);
  };
}

makeGreeter()("Asis");
```

BLOCK 04 (ARROW NOTATION)

```javascript
const increment = n => {
  return n + 1;
};

console.log(incremenet(5));

// Implicit Return
const increment = n => n + 1;
```

BLOCK 05 (ARROW NOTATION MULTIPLE/NO PARAMETERS)

```javascript
const multiply = (a, b) => a * b;

multiply(3, 4); // returns 7

const noParameters = () => "No Parameters Here.";
```

BLOCK 06 (PUTTING IT ALL TOGETHER)

```javascript
function makeGreeter(greeting) {
  return name => console.log(`${greeting} ${name}`);
}

const helloGreeter = makeGreeter("Hello");
helloGreeter("Asis");
helloGreeter("Hamsa");

const arabicGreeter = makeGreeter("هلا");
arabicGreeter("عزيز");
arabicGreeter("حمزة");

const japaneseGreeter = makeGreeter("こんにちは");
japaneseGreeter("ライラ");
```

---

### Code Blocks (Array Iterators)

BLOCK 01 (.FOREACH)

```javascript
let cities = ["Kuwait", "London", "New York", "Perth", "West Lafayette"];

console.log("I've lived in: ");
for (let i = 0; i < cities.length; i++) {
  console.log(cities[i]);
}

// You can rewrite the loop using the .forEach method:
cities.forEach(city => console.log(city));
```

BLOCK 02 (.MAP)

```javascript
let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let squares = [];

for (let i = 0; i < numbers.length; i++) {
  squares.push(numbers[i] * numbers[i]);
}

// You can rewrite the loop using the .map method:
squares = numbers.map(number => number * number);
```

BLOCK 03 (.FILTER)

```javascript
let emails = [
  "asis@joincoded.com",
  "fawas@joincoded.com",
  "mishmish@gmail.com",
  "hamsa@hotmail.com"
];

let approvedEmails = [];

for (let i = 0; i < emails.length; i++) {
  if (!emails[i].endsWith("@hotmail.com")) {
    approvedEmail.push(emails[i]);
  }
}

// You can rewrite the loop using the .filter method:
approvedEmails = emails.filter(email => !email.endsWith("@hotmail.com"));
```
