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
  
  
