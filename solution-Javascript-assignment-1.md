# Javascript Assignment 1
## 1. Write a program to find whether a given year is a leap year or not.

```
//----------solution 1------------------//
const year = 2004;
if ((year % 4 == 0) && (year % 100 != 0) || (year % 400 == 0)) {
    console.log(year + ' is a leap year');
} else {
    console.log(year + ' is not a leap year');
}
```

## 2. Write a JavaScript program to convert temperatures to and from Celsius,Fahrenheit.
[ Formula : c/5 = (f-32)/9 [ where c = temperature in Celsius and f = temperature in Fahrenheit ]
Expected Output :
60°C is 140 °F
45°F is 7.222222222222222°C 
``` 
/*-----------solution 2--------------*/
function toFahrenheit(celsius)
 {
  let  temp=celsius;
  let fdegree = temp * 9 / 5 + 32;
  let  message = temp+'\xB0C is equivalent to ' + fdegree + ' \xB0F.';  // xBOC is for printing  °C
     console.log(message);
 }
 function toCelsius(fahrenheit) 
 {
   var temp = fahrenheit;
   var cdegree = (temp - 32) * 5 / 9;
   var message = temp+'\xB0F is equivalent to ' + cdegree + '\xB0C.'; 
     console.log(message);
 } 
 toFahrenheit(60);
 toCelsius(45);
```

## 3. Write a program to find the factorial of a number
```
//*---------------------solution 3-------------*//

function factorial(num) {
    if (num<0){
        return `factorial of ${num} is not possible`;
    }
    else if(num==0){
        return `factorial of ${num} is 1`;
    }
    else{
    let fact = 1;
    for (let i = 1; i <= num; i++)
    {
        fact = fact * i
    }
    return `factorial of ${num} is ${fact}`;
}
}
let Fact = factorial(-1);
let Fact1 = factorial(0);
let Fact2 = factorial(5);
console.log(Fact)
console.log(Fact1)
console.log(Fact2)
```
