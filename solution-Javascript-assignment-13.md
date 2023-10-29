# JavaScript Assignment 13
# 1. Write a JavaScript program to get an array from the user and return the:
- a) Sum of all elements in the array using reduce()
- b) Average of all elements in the array using reduce()
```
Sample Input:
[ 1, 2, 3, 4, 5 ]
Output:
15
3
```
```
//To take input from user in Browser
let arr = prompt("Enter array values");
arr = arr.split(",");
arr = arr.map(i => parseInt(i));
//let arr = [ 1, 2, 3, 4, 5 ];
//a) Sum of all elements in the array using reduce()
let sum = arr.reduce((sum, ele) => sum+ele);
console.log(sum);
//b) Average of all elements in the array using reduce()
let avg = arr.reduce((sum,ele,index,ar) => (sum+ele/ar.length),0);
console.log(avg);
```
# 2. Write a JavaScript program to
```
a) Calculate grades on basis of marks
>90 = A
>80 = B
>70 = C
>60 = D
>50 = E
else = F
b) Map the grades of each student
c) Group students according to the grades they have received and display.
Sample Input:
let students = [
{ name: "John", marks: “92” },
{ name: "Oliver", marks: “85” },
{ name: "Michael", marks: “79” },
{ name: "Dwight", marks: “95”},
{ name: "Oscar", marks: “64” },
{ name: "Kevin", marks: “48” },
];
Output:
{
'A': [ { name: "John", grade: “A” },
{ name: "Dwight", grade: “A” } ],
'B': [ { name: "Oliver", grade: “B” } ],
'C': [ { name: "Michael", grade: “C” } ],
'D': [ { name: "Oscar", grade: “D” } ],
'E': [ ],
'F': [ { name: "Kevin", grade: “F” } ],
}
```
```

// a) Calculate grades on basis of marks
let students = [
{ name: "John", marks: "92" },
{ name: "Oliver", marks: "85" },
{ name: "Michael", marks: "79" },
{ name: "Dwight", marks: "95"},
{ name: "Oscar", marks: "64" },
{ name: "Kevin", marks: "48" }
];

// b) Map the grades of each student
students.map(item => {
if(item.marks >= 90 ){
item["Grade"] = "A";
}else if(item.marks >= 80 ){
item["Grade"] = "B";
}else if(item.marks >= 70 ){
item["Grade"] = "C";
}else if(item.marks >= 60 ){
item["Grade"] = "D";
}else if(item.marks >= 50 ){
item["Grade"] = "E";
}else {
item["Grade"] = "F";
}
})
console.log(students);

// c) Group students according to the grades they have received and display
let group= students.reduce((acc, obj) => {
const prop = obj["Grade"];
acc[prop] = acc[prop] || [];
acc[prop].push(obj);
return acc;
},{})
console.log(group)
```
