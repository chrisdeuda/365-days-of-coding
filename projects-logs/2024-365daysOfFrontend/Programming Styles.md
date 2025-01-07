

![[CleanShot 2025-01-07 at 14.24.30.png]]

## Imperative Programming:


- Characteristics:
    - Uses statements that change a program's state
    - Focuses on describing how a program operates
    - Uses loops, conditionals, and variable assignments
- Example (JavaScript):


```js
function findEvenNumbers(numbers) {
    let evenNumbers = [];
    for (let i = 0; i < numbers.length; i++) {
        if (numbers[i] % 2 === 0) {
            evenNumbers.push(numbers[i]);
        }
    }
    return evenNumbers;
}
console.log(findEvenNumbers([1, 2, 3, 4, 5, 6]));

```


## Declarative Programming:

- Characteristics:
    - Expresses the logic of computation without describing its control flow
    - Often uses higher-order functions and expressions instead of statements
    - SQL is a classic example of declarative programming
- Example (JavaScript):
```js
function findEvenNumbers(numbers) {
    return numbers.filter(num => num % 2 === 0);
}
console.log(findEvenNumbers([1, 2, 3, 4, 5, 6]));

```


## Functional Programming:

- Characteristics:
    - Treats computation as the evaluation of mathematical functions
    - Avoids changing state and mutable data
    - Emphasizes the application of functions to inputs to produce outputs
- Example (JavaScript):
```js
const compose = (f, g) => x => f(g(x));
const addOne = x => x + 1;
const double = x => x * 2;
const doubleAndAddOne = compose(addOne, double);

console.log(doubleAndAddOne(3)); // Output: 7

```


## Object-Oriented Programming (OOP):

- Characteristics:
    - Based on the concept of "objects" containing data and code
    - Emphasizes concepts like inheritance, polymorphism, and encapsulation
    - Organizes software design around data, or objects, rather than functions and logic
- Example (JavaScript):



```js
class Animal {
    constructor(name) {
        this.name = name;
    }
    speak() {
        console.log(`${this.name} makes a sound.`);
    }
}

class Dog extends Animal {
    speak() {
        console.log(`${this.name} barks.`);
    }
}

let dog = new Dog('Rex');
dog.speak(); // Output: Rex barks.
```
```
```

### 

Reactive Programming:

- Characteristics:
    - Focuses on data flows and the propagation of change
    - Built on the observer pattern
    - Particularly useful for handling asynchronous data streams
- Example (JavaScript with RxJS):

```js
import { fromEvent } from 'rxjs';
import { map, debounceTime, distinctUntilChanged } from 'rxjs/operators';

const input = document.getElementById('search-input');
const typeahead = fromEvent(input, 'input').pipe(
    map(e => e.target.value),
    debounceTime(300),
    distinctUntilChanged()
);

typeahead.subscribe(value => {
    console.log('Search term:', value);
});

```


## Logic Programming:


- Characteristics:
    - Based on formal logic
    - Program statements express facts and rules about problems
    - Computation is done by inferencing on these facts and rules
- Example (Prolog):

```prolog
parent(john, mary).
parent(john, tom).
parent(mary, ann).

grandparent(X, Z) :- parent(X, Y), parent(Y, Z).

% Query: grandparent(john, ann).
% Output: true

```



- React uses a declarative style for describing UI, but often employs functional programming concepts in hooks and state management.
- Python supports both OOP and functional programming styles.
- Scala integrates both object-oriented and functional programming paradigms.



# How AI was genereating code

1. AI-generated code tendencies:
    
    - Often optimizes for brevity and "clever" solutions
    - May use advanced language features or functional programming concepts
    - Can combine multiple operations into a single line (chain of methods)
2. Readability vs. Conciseness:
    
    - Shorter code isn't always more readable, especially for developers with different backgrounds
    - What's concise for one developer might be cryptic for another
3. Programming paradigm differences:
    
    - Coming from PHP, which often uses more imperative styles, functional or declarative JavaScript can look unfamiliar
    - Modern JavaScript (and frameworks like React) often lean towards functional and declarative styles
4. Language feature utilization:
    
    - AI might use newer JavaScript features that you're not yet familiar with
    - Examples: arrow functions, destructuring, spread operators, array methods like map/reduce/filter