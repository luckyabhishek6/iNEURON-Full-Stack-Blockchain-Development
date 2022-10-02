#  Javascript Assignment 2

## 1. Write a Javascript function to check whether a triangle is equilateral,isosceles or scalene.
```
//------------------solution -1----------------- //
function triangleType(x,y,z){
        if (x == y && y == z)                   // Checks for equilateral triangle
        console.log("Equilateral Triangle");
        
        else if (x == y || y == z || z == x)    // Checks for isosceles triangle
        console.log("Isosceles Triangle");
        
        else                                     // Otherwise scalene triangle
        console.log("Scalene Triangle");    
}

triangleType(3,4,5)
triangleType(3,3,5)
triangleType(3,3,3)
```


## 2. Write a function using switch case to find the grade of a student based on marks obtained.
- a. “S grade” if the marks are between 90 and 100.
- b. “A grade” if the marks are between 80 and 90.
- c. “B grade” if the marks are between 70 and 80.
- d. “C grade” if the marks are between 60 and 70.
- e. “D grade” if the marks are between 50 and 60.
- f. “E grade” if the marks are between 40 and 50.
- g. “Student has failed” if the marks are between 0 and 40.
- h. Else output “Invalid marks”.

```
//------------------solution -2----------------- //
     function grading(marks)
        {
            let x= Math.floor(marks/10)
            console.log(x)
        switch(x)
        {
            case 10 :
                    console.log("excellent")
            case 9 :
                //Marks between 90-100
                console.log(" Your Grade is:S");
                break;
            case 8 :
                    // Marks between 80-89
                console.log(" Your Grade is: A" );
                break;
            case 7 :
                // Marks between 70-79
                console.log(" Your Grade is: B" );
                break;
            case 6 :
                // Marks between 60-69
                console.log(" Your Grade is: C" );
                break;
            case 5 :
                    // Marks between 50-59
                console.log(" Your Grade is: D" );
                break;
            case 4 :
                    // Marks between 40-49
                console.log(" Your Grade is: E" );
                break;
            case 3 :
                    // Marks between 30-39
                console.log(" “Student has failed”" );
                break;
            case 2 :
                    // Marks between 20-29
                console.log(" “Student has failed”" );
                break;
            case 1 :
                    // Marks between 10-19
                console.log(" “Student has failed”" );
                break;
            case 0 :
                    // Marks between 0-9
                console.log(" “Student has failed”" );
                break;
            default :
                    console.log(" “Invalid marks");
        }
        return 0;
        }

        grading(59);
```

## 3. Write a JavaScript program to find the sum of the multiples of 3 and 5 under 1000.

```
//---------solution 3--------------
        function sumOfMultiplesOf3and5 (number) {
            let sum = 0;
            for(let i=1; i<number; i++) {
                if(i % 3 === 0 || i % 5 === 0){
                    sum += i;
                }
            }
            console.log('sum of multiple of 3 and 5 under',number +" is: "+sum)
        }
        sumOfMultiplesOf3and5(1000);
```
## 4. Write a program to find the factorial of all prime numbers between a given range . Range will be passed as 2 values in the function parameters. eg- if it is needed to find the values for numbers 1-100, then function declaration can look like - function prime(1,100).

```

//---------solution 4--------------
function primecheckerAndFactorial(start, end)
{
        let primeNumber=[]
    for(let i=start; i<=end;i++ )
    {
     let count =0
     for (let j=1;j<=end;j++){
        if(i%j==0){
                count++;
         }
     }
     if (count==2){
        primeNumber.push(i)
     }
     }
      //facrorial part
     for(let num of primeNumber){
        let fact=1
        for(let i=1;i<=num;i++){
                fact=fact*i;
        }
        console.log(`factorial of ${num} is ${fact}.`);
     }
     return `list of prime Numbers between ${start} and ${end} are ${primeNumber}`
    }

let result= primecheckerAndFactorial(1,10)
console.log(result);
```
