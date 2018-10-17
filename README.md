# JSEpisodeThree-Demo

[Slides]()

---

### Code Blocks (Functional Programming)

BLOCK 01 (ASSIGNING TO VARIABLE)

```javascript
let sayHello = function() {
  console.log("Hello");
};
```

BLOCK 02 (PASSING FUNCTION AS ARGUMENT)

```javascript
function runMe(fn) {
  fn();
}

let sayHello = function() {
  console.log("Hello");
};

runMe(sayHello);

// Anonymous function
runMe(function() {
  console.log("This is amazing!!");
});
```

BLOCK 03 (RETURNING A FUNCTION)

```javascript
function sayHello() {
  return function() {
    console.log("Hello!");
  };
}

sayHello()(); // logs "Hello!" - notice the double parentheses
```

BLOCK 04 (ARROW NOTATION)

```javascript
const incrementWibble = wibble => {
  return wibble + 1;
};

const incrementWibble = wibble => {
  return wibble + 1;
};

const incrementWibble = wibble => wibble + 1;
```

BLOCK 05 (ARROW NOTATION MULTIPLE/NO PARAMETERS)

```javascript
const multipleParameters = (parameterOne, parameterTwo) => {
  return parameterOne + parameterTwo;
};

multipleParameters(3, 4); // returns 7

const noParameters = () => {
  return "No Parameters Here.";
};
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
