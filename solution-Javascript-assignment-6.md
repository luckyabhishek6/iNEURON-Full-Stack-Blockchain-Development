# Javascript Assignment 6
## 1) Perform the following operations to provide the implementation for a Rectangle class. The operations are:
- 1. Add an area() method to the Rectangle class.
- 2. Create a Square class that satisfies the following conditions:
- ○ It is a subclass of Rectangle.
- ○ It contains a constructor and no other methods.
- ○ It can use the Rectangle class' area method to print the area of a Square object.
```
//--------------------------------------solution of question no. 1--------------------------
console.log("solotion of question 1")
class Rectangle{
    constructor(length, breadth){
        this.length= length;
        this.breadth= breadth;
        }

        area()
        {
            return `area :  ${this.length * this.breadth}`
        }
}
 class Square extends Rectangle{
    constructor(length){
        super(length,length)
        }
 }

 const rect= new Rectangle(4,5)
 console.log(rect.area());
 const sq= new Square(4);
 console.log(sq.area())
 ```
## 2) Write a javascript function find_largest to return the nth largest number in an arrayeg- given an array of integers- [3,45,6,7,23,5,7,8] find_largest(3) will return third largest number from the above array - which is 8.*/
```
//------------------"solotion of question 2"--------------
class Nth_largest{
    constructor(arr){
    this.arr = arr;
}

    Find_largest(n){
        let sorted=this.arr.sort((a,b) => b-a);        
       
    let sortedArr=[...new Set(sorted)]
    console.log(`Array is Sorted in Decending Order [${sortedArr}]`)
    return sortedArr[n-1]
}
}

const obj = new Nth_largest([3,45,6,7,23,5,7,8,]);
console.log(obj.Find_largest(3))
```

## 3) Write a JavaScript program which accept a number as input in the function parameter and insert dashes (-) between each two evennumbers.For example if you accept 025468 as the output should be 0-254-6-8. computeDash(025468) -> 0-254-6-8

```
//--------------"solotion of question 3"-----------

        function insertDash(num){
            let Arr=num.toString();
            let output=[Arr[0]];

            for (let i=1; i<Arr.length; i++){
                if ((Arr[i-1]%2===0) && ( Arr[i]%2===0))
                {
                    output.push('-',Arr[i]);
                }else{
                    output.push(Arr[i])
                } 
            }
            return (output.join(''))
        }
    
        const newNum =  insertDash(025468);
        console.log(newNum)
```
