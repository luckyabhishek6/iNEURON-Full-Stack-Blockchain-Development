# Javascript Assignment 7

## Question 1
Input a String S, and check its length and if the length is greater than 4, truncate the input String and output the result.

```
let str = "icecreame";
let len = str.length;

if (len < 4) {
    console.log(str);
} else {
    console.log(str.slice(0, 4) + "...");
}
```

## Question 2
Input a String S with multiple words, and remove whitespaces and output the result.

```
let input2 = "Hii Boy how are you??????";
let output2 = input2.split(" ").join("");
console.log(output2);
```

## Question 3
Input a String S with two words, and replace the first word with the second word and display the result.

```
let input3 = "Hii Boy";
let output3 = input3.split(" ").reverse().join(" ");
console.log(output3);
```

## Question 4
Input a String S with a word, and replace character “a” with “x” and display the result.

```
let input4 = "apple";
let output4 = input4.replace("a", "x");
console.log(output4);
```

## Question 5
What string method can be used to convert a string into an array?

```
let input5 = "string";
let output5 = input5.split("");
console.log(output5);
```

## Question 6
What string method can be used to check the occurrence of a specified text in a string?

```javascript
let input6 = "management";
let number = input6.split("m").length - 1;
let number1 = input6.match(/a/g).length; // g is a flag for global scope
console.log(number);
console.log(number1);

//----------------OR---------------------------
let str= "apple is the best fruit in the entire world";
let arr = str.includes('best');
console.log(arr);
//includes() - string method is used to check the occurrences. It returns true.
//indexOf(‘best’) - string method gives index of the word in the string.
```

## Question 7
How can you break a string to a newline in Javascript?

```
let str2 = "lellop\nooooo";   // \n is an escape sequence for a new line
console.log(str2);
```

## Question 8
Write a Javascript function to test whether the first character of a string is lowercase.

```
let s = "Apple";

function isLowerCase(str, index) {
    return str.charAt(index).toLowerCase() === str.charAt(index);
}

console.log(isLowerCase(s, 0));
```

## Question 9 
Give a correct verdict to users input if he enters "yes", "YES", "Yes", etc (any combination) using string methods.
```
function checkUserInput(input) {
  // Convert the input to lowercase
  const lowercaseInput = input.toLowerCase();

  // Check if the lowercase input is "yes"
  if (lowercaseInput === "yes") {
    return "User input is affirmative.";
  } else {
    return "User input is not affirmative.";
  }
}


const userInput1 = "Yes";
const userInput2 = "yEs";
const userInput3 = "YES";

console.log(checkUserInput(userInput1)); // Output: "User input is affirmative."
console.log(checkUserInput(userInput2)); // Output: "User input is affirmative."
console.log(checkUserInput(userInput3)); // Output: "User input is affirmative."

```
## Question 10
Given a String S, achieve the following tasks:

a) Convert the String into upper case.

b) Convert only the first character to uppercase.

c) Convert the String into lower case.

d) Break the string into two halves and swap them.

e) Count the repeating characters.

f) Reverse the string.

```
let str10 = "Abhishek";

//a) Convert the String into upper case.

console.log("Entered string in uppercase:", str10.toUpperCase());

//b) Convert only the first character to uppercase.

console.log("Only the first character to uppercase:", str10.charAt(0).toUpperCase() + str10.substring(1));

//c) Convert the String into lower case.

console.log("Entered string in lower case:", str10.toLowerCase());

//d) Break the string into two halves and swap them.

let half1 = str10.slice(0, str10.length / 2);
let half2 = str10.slice(str10.length / 2);
console.log(half2 + half1);

//e) Count the repeating characters.

let num = str10.split("a").length - 1;
console.log(num);

//f) Reverse the string.

console.log(str10.split('').reverse().join(''));
```
