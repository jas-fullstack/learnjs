
### Array functions
#### includes

```
** includes -> it will check if value is available inside array or string. **
const arr = [1,2,3,5,6,3];
console.log(arr.includes(1));
//output true
```
#### indexOf
```
indexOf() -> return the first index from element.
const arr = [1,2,3,5,6,3];
console.log(arr.indexOf(3));
//output 2
```

#### find
```
find() -> return the element based on the condition...
const arr = [1,2,3,5,5,6,3];
console.log(arr.find((val)=>  val > 3 ));
//output 5
```


#### split 
```
it will convert string to array..
  
const str = 'sanjeev kumar';
console.log(str.split(" "));
//output  ["sanjeev", "kumar"]
```


#### splice 
```
we can push item into array at any place with delete or not.
  
let data = ["jan","march","apprail"];

//data.splice(index to add,index to remvoe,"value);

data.splice(data.length,0,"feb");
console.log(data);

```



### Qustions : let and var and const
-The let keyword was introduced in ES6 (2015).
-Variables defined with let cannot be Redeclared.
-main diffrance is that let is blocked scoped and var is not blocked scoped. {...}.
we can declare variable multiple times with var but not with let or const

###  Qustions : Hoisting    
Hoisting mean java script moves the variables on the top when execute any file. but you can do it with var only with let you will get an error. 
###  Qustions : what is user strict mode
 This mode disable the forgivness of java script. means we can intilize variable without using var keyword javascript automatically pic it. by using strict mode it disable this behaviour. 
 ###  Qustions : arrow function
 arrow function is new syntex to write function. we write function without using function keyword. its have short syntex. 
 - return value withour return keyword.
 - syntex can much shorter.
  
 const arrowFn = () => {  }
 ###  Qustions : call back function
 When we pass function as a parameter is called callback function. we can make api calls and can get waited response with callback functions. 
 
```
syntex
//declare function
function testcallbackfunc(cb){
 cb('name will print there')
}

//calling funtion
testcallbackfunc(cb = (name) => {
 console.log(name)
})
  ```
  ```
Another example with settimeout
setTimeout(function(){ console.log('name will print there') }, 3000);
console.log("after call back2222")

function testcallbackfunc(cb){
setTimeout(function(){ cb('name will print there') }, 3000);
		
}
testcallbackfunc(cb = (name) => {
	
 console.log(name)
 console.log("after call back")
})
```

 ###  Qustions : adding and removing elements from array push , unshift , pop ,shift
  
  ```
- PUSH INTO Array
//push method will always push item last into array.we can push multiple or single value into an array
const hobbies = ['sports','Cooking']
hobbies.push('Reading','music');
console.log("hobbiles--->",hobbies)

- unshift ...with this we can add item begning of the array
const hobbies_unshift = ['sports','Cooking']
hobbies_unshift.unshift('coading');
console.log("hobbies_unshift--->",hobbies_unshift)


- pop this will remove item from last from the array
const hobbies_pop = ['sports','Cooking']
hobbies_pop.pop();
console.log("pop--->",hobbies_pop)

- shift this will remove item from last from the array
const hobbies_shift = ['sports','Cooking']
hobbies_shift.shift();
console.log("shift--->",hobbies_shift)
```

###  Qustions : this keyword

This keyword refer to the current object. suppose if we define function inside any object we can access outer objects with this.

const person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};

### Scope in java script
- Global scope 
- function scope
- block scope

### lexical scope
lexcal score mean we can access variable which is declared outside the function. but we cant access variable out side the function which is declared inside the function.

### Qustions : map , reduce and filter
- map :
it's used to loop through array and return us modified result of array. we can chain the method with map like reduce or filter.
###### ` [1, 2, 3, 4, 5].map((x)=> x * x)`
- reduce : 
Reduce will take array and return the final modified result. it should have two params one is accumulator and other is currentValue. But I can have index as well. 
###### `[1, 2, 3, 4, 5].reduce(function (acc, current) {return acc + current}, 0) //zero means start from where e.g 0`
- Filter : 
Filter will return the filtred items of array.

### pure funcions 
Pure functions are the functions which does return same result every time e.g a function doing sum of values will always return same result.

### event loop
Event loop plays important role in nodejs processing. when we execure any program in node js it goes into the call stack after the execution it goes into call back que. now the job of event loop is to make sync between call back que and call stack. 
if call stack is empty then event loop move program from call back que to call stack. 

### undefined vs undeclared vs null
undefined : is when variable is declared but not assigned any value.
undeclared : when we try to assign any value without declaration. 
null: when we assing null value to variable

### modules in javascript.
export to export function or variable.import to include file.
 
### generator functions
Normal function return value single time but in the generator function we can return values multiples time accorting to the requirement using **yield** 
syntex :
 
```
function* generateSequence() {
  yield 1
  yield 2
  return 3
}

let generator = generateSequence();
let one = generator.next();
let two = generator.next();
alert(JSON.stringify(one)); // {value: 1, done: false}
alert(JSON.stringify(two)); // {value: 1, done: false}
```
- Generators are iterable : we can make loop of generator functions. but it will not print value of return.
```
function* generateSequence() {
  yield 1;
  yield 2;
  return 3;
}

let generator = generateSequence();

for(let value of generator) {
  alert(value); // 1, then 2
}
```

### does typescript run on browser
No compiler complie ts code to run on any browser.




# Angular

### life cycle hooks 
```
- ngOnChange()
- ngOnInit()
- ngViewOnInit()
- ngAfterContentInit()
- ngAfterContentCHecked()
- ngAfterViewInit()
- ngAfterViewChecked()
- ngDoCheck()
- ngOnDestroy()
```



