# Javascript Assignment 9
# 1. Carefully observe this example.
## a) Is the InnerFunction() a closure?
## b) What is output of this program
```function OuterFunction()
{ var outerVariable = 100;
function InnerFunction() {
alert(outerVariable);
}
return InnerFunction;
}
var innerFunc = OuterFunction();
innerFunc();
```
``` 
a)  yes, it is closure
    InnerFunction() is a closure.
    It remembers the value of  outerVariable i.e., 100 which is in its lexical scope.

b)  output is  -- 100
```

# 2. What is the difference between a closure and a scope ?
Whenever you create a function within another function, then the inner function is closure. This closure is usually returned so you can use the outer function’s variables at a later time.
Whereas
a scope in JavaScript defines what variables you have access to. There are two kinds of scope – global scope and local scope.

OR,
A function along with its lexical scope forms a Closure. Forexample, if we create a function inside another function, the inner function is said to be closure. 

Scope is nothing but what variables you have access to. It refers to the current context of the code, which determines the 
accessibility of variables. There are two types of Scopes: 1.Global Scope and 2. Local Scope.


# 3. What is a lexical scope and how is it related to closure?
 closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function's scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.
 
 # 4. Output of following closure ?
```
for (var i = 0; i < 3; i++) {
setTimeout(function log() {
console.log(i); // What is logged?
}, 1000);
}
```
The above code will log the value 3 three times after 1 second.This happens because of closure. The closure remembers its lexical environment and remembers the reference of variable ‘i’. By the 
time of callback function executes, the for loop completes its iteration upto 3. Therefore, it logs the value which is stored in the variable i. This problem can be avoided by using let keyword instead of var keyword. Because the let keyword is block scoped. So, every time the setTimeout is called the callback function forms a closure with new copy of variable

```
for (var i = 0; i < 3; i++) {
    setTimeout(function log() {
    console.log(i); // What is logged?
    }, 1000);
    }

// output:     3
            // 3
            // 3
            // if you replace var by let then output will be...
            // 0
            // 1
            // 2
```
