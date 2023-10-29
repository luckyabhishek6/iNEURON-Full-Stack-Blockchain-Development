# JavaScript Assignment 10
# 1. Are Higher Order functions and Call back functions the same? If not,briefly explain about both functions.
NO. Both are different.
Higher Order functions are the functions which takes other 
functions as an argument and return the functions to its callers.

Whereas Callback function is a function that is passed to another 
function with the expectation that another function will call it.

# 2. Is filter a Higher Order function in Javascript ? If yes, why ?

YES. Map, filter and reduce are the built-in higher order functions in Javascript.
Because filter will return each element that meets the condition set within the anonymous function it receives.
filter is a higher order function which provides a higher level of abstraction for functions.
# 3. Give an example of a Higher Order function and a call back function used in the same program.

```function doArithmetic(arr, instruction) { 
const output =[];
for(let i=0; i<arr.length; i++){
output.push(instruction(arr[i])); 
}
return output;
}
function multiplyByTwo(input) {
return input*2;
}
let arr = [1,2,3,4];
let result = doArithmetic(arr, multiplyByTwo);
console.log(result);

//doArithmetic is a higher order function because it takes in a function called instruction.

//Here, Instruction is a callback function which does some work and gives output.
```
# 4. Carefully check the example below:
- a) What will be the output of this program ?
- b) Which function is a Higher Order function here ?
```const names= ['John', 'Tina','Kale','Max']
function useFunction(arr,fn){
for(let i=0; i<arr.length; i++){
fn(arr[I]);
}
}
function argFn (name){
console.log("Hello " + name );
}
useFunction(names,argFn);
```
a) Output is :-

Hello John

Hello Tina

Hello Kale

Hello Max

b) The outer function i.e, useFunction is a Higher Order Function.And argFn is a callback function
