### Qustions : let and var and const
-main diffrance is that let is blocked scoped and var is not blocked scoped. {...}.
we can declare variable multiple times with var but not with let or const
      note : we can access parent block level inside child block level
###  Qustions : Hoisting    
Hoisting mean java script moves the variables on the top when execute any file. but you can do it with var only with let you will get an error. 
###  Qustions : what is user strict mode
 This mode disable the forgivness of java script. means we can intilize variable without using var keyword javascript automatically pic it. by using strict mode it disable this behaviour. 
 ###  Qustions : arrow function
 arrow function is new syntex to write function. we write function without using function keyword. its have short syntex.
 
 const arrowFn = () => {  }
 ###  Qustions : call back function
 When we pass function as a parameter is called callback function. 
 
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

 ###  Qustions : adding and removing elements from array.. push , unshift , pop ,shift
  
  ```
  //PUSH INTO Array
//push method will always push item last into array.we can push multiple or single value into an array
const hobbies = ['sports','Cooking']
hobbies.push('Reading','music');
console.log("hobbiles--->",hobbies)

//unshift ...with this we can add item begning of the array
const hobbies_unshift = ['sports','Cooking']
hobbies_unshift.unshift('coading');
console.log("hobbies_unshift--->",hobbies_unshift)


//pop this will remove item from last from the array
const hobbies_pop = ['sports','Cooking']
hobbies_pop.pop();
console.log("pop--->",hobbies_pop)

//shift this will remove item from last from the array
const hobbies_shift = ['sports','Cooking']
hobbies_shift.shift();
console.log("shift--->",hobbies_shift)
```

###  Qustions : this keyword

if in a method this keyword refer to the current object. 

const person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};

### Scope in java script
Global scope , function scope, block scope

### lexical scope
lexcal score mean we can access variable which is declared outside the function. but we cant access variable out side the function which is declared inside the function.

### Qustions : map , reduce and filter
#### map :
it's used to loop through array and return us modified result of array. we can chain the method with map like reduce or filter.
###### ` [1, 2, 3, 4, 5].map((x)=> x * x)`
#### reduce : 
Reduce will take array and return the final modified result. it should have two params one is accumulator and other is currentValue. But I can have index as well. 
###### `[1, 2, 3, 4, 5].reduce(function (acc, current) {return acc + current}, 0) //zero means start from where e.g 0`
#### Filter : 
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



