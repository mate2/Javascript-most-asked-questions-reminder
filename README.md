# Javascript-most-asked-questions-reminder

#### [Closure] What is a closure ? ####
It's a function that have access to parent (another function) scope even after it closed. So you can define private variables.

```
	var myFunction = ( () => {	
  		var privateVariable = 0;
  		return () => {
  			privateVariable += 1; 
  			return privateVariable
  		}
	})();

	myFunction();	// Output 1
	myFunction();	// Output 2
	privateVariable	// undefined
```

[https://www.w3schools.com/js/js_function_closures.asp](https://www.w3schools.com/js/js_function_closures.asp)

---

#### [For...in / For...of] What is the difference between for..in and for...of loops ? ####
- `for...in` : iterates over `keys`
- `for...of` : iterates over `values`

```
	for(key in myArray) {
		console.log(key);
		console.log(myArray[key]);
	}

	for(value of myArray) {
		console.log(value);
	}
```
[https://alligator.io/js/for-of-for-in-loops/](https://alligator.io/js/for-of-for-in-loops/)

---

#### [Functional Programming] What is functional programing ? ####
Functional programing is building a software  with only pure functions, avoiding sharing state, mutable data and side effects. It is declarative rather than imperative. It is easier to unit test because of pure functions.

[https://medium.com/javascript-scene/master-the-javascript-interview-what-is-functional-programming-7f218c68b3a0](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-functional-programming-7f218c68b3a0)

---

#### [Var / Let / Const] What are the difference between var, let and const ? ####
- var : variable is scoped to the function where it is declared and value can be overwritten
- let : variable is scoped to the block where it is defined and value can be overwritten.
- const : variable is scoped to the block where it is defined and value cannot be overwritten.

[https://www.freecodecamp.org/news/var-let-and-const-whats-the-difference/](https://www.freecodecamp.org/news/var-let-and-const-whats-the-difference/)

---

#### [Object Oriented Programming] What is oop in javascript ? ####
It is prototype based, not relying on Class.

[https://www.freecodecamp.org/news/how-javascript-implements-oop/](https://www.freecodecamp.org/news/how-javascript-implements-oop/)
[https://medium.com/javascript-scene/master-the-javascript-interview-what-s-the-difference-between-class-prototypal-inheritance-e4cd0a7562e9](https://medium.com/javascript-scene/master-the-javascript-interview-what-s-the-difference-between-class-prototypal-inheritance-e4cd0a7562e9)

---

#### [* Generators] What is *() function ? ####
It is a generator function. You can call `.next()` to get the next yield value.

```
	const generator = function* (i) {
		yield i;
		yield i + 1;
		yield i + 2;
	}

	const gen = generator(1); 
	gen.next().value;  // output 1
	gen.next().value;  // output 2
	gen.next().value;  // output 3
```

[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*)

---

#### [Event Bubbling] What is event bubbling ? ####
Event bubling is propagation of an event from the element that triggered the event up to its ancestors (going up the DOM tree).

By default events bubble.

In opposition of event capturing which is propagation of an event from the element that triggered the event starting with outer ancestors (going dow the DOM tree from further ancestor to the element that triggered the event).

[https://flaviocopes.com/javascript-event-bubbling-capturing/](https://flaviocopes.com/javascript-event-bubbling-capturing/)

---

#### [Hooks] What are React Hooks ? ####
They are functions that let you "hook into" React state and life cycle from function component.
[https://reactjs.org/docs/hooks-overview.html#:~:text=Hooks%20are%20functions%20that%20let,lifecycle%20features%20from%20function%20components.&text=React%20provides%20a%20few%20built,stateful%20behavior%20between%20different%20components.](https://reactjs.org/docs/hooks-overview.html#:~:text=Hooks%20are%20functions%20that%20let,lifecycle%20features%20from%20function%20components.&text=React%20provides%20a%20few%20built,stateful%20behavior%20between%20different%20components.)

---

#### [Stateless component] What is a stateless component ? ####
It is a component that has no state, and returns same markups with same props.
[https://medium.com/groww-engineering/stateless-component-vs-pure-component-d2af88a1200b](https://medium.com/groww-engineering/stateless-component-vs-pure-component-d2af88a1200b)

---

#### [IE9] What the difference with event propagation in Internet Explorer 9 ? ####
You cannot stop event propagation with `event.stopPropagation()` in Internet explorer and lesser versions. You have to use `event.cancelBubble = true;`

[https://en.wikipedia.org/wiki/Event_bubbling#How_to_stop_bubbling](https://en.wikipedia.org/wiki/Event_bubbling#How_to_stop_bubbling)

---

#### [Map] What is Map class ? ####
Map is an optimized object that iterates on key-value pair in order they have been inserted.

Main differences with standard objects :
- Map does not have default key
- Map key can be any value (even functions, objects or primitives)
- Map key-value pairs are ordered (insertion ordered) 
- You can get number of items in a Map with its `size` property
- You can iterate directly on Map items
- Better performance for insertion and removal of key-value pairs

[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)

---
## Other non Javascript questions ##
---

#### [CI / CD] What is the difference between Continuous integration and continuous delivery ? ####
- Continuous integration is the fact to push your code on the repository as soon as it's done.
- Continous delivery is extension of continuous integration to push latest changes on release branch as soon as code has been merged in it.

[https://www.atlassian.com/continuous-delivery/principles/continuous-integration-vs-delivery-vs-deployment](https://www.atlassian.com/continuous-delivery/principles/continuous-integration-vs-delivery-vs-deployment)

---

#### [Object Oriented Programming] What is oop ? ####
It is a programming paradigm based on the concept of "objects" (instance of a class), which contain properties (variables) and methods (functions).
The four principles of object oriented programming are :
	- encapsulation
	- inheritance
	- polymorphisme
	- abstraction

[https://www.freecodecamp.org/news/object-oriented-programming-concepts-21bb035f7260/](https://www.freecodecamp.org/news/object-oriented-programming-concepts-21bb035f7260/)
[https://en.wikipedia.org/wiki/Object-oriented_programming](https://en.wikipedia.org/wiki/Object-oriented_programming)