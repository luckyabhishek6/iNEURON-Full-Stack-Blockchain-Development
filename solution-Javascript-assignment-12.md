# JavaScript Assignment 12
# 1. Write a JavaScript program to map Employee Records according to Employee IDs.
Employee: { id, name, salary }
a) Print an array of all employee ids
b) Print count of employees
c) Print the name of the employee according to their id { key: value }
d) Store the salaries of all employees in an array
e) Calculate the average salary the company is paying to its employees.
```
Sample Input:
"id": [ 67, 48, 29 ]
"name": [ "Hitanshu", “Ninad”, “Amandeep” ]
"salary": [ 75000, 82000, 98000 ]
Output:
[ 67, 48, 29 ]
3
67: Hitanshu
48: Ninad
29: Amandeep
[ 75000, 82000, 98000 ]
85000
```
```
let obj ={
"id": [ 67, 48, 29 ],
"name": [ "Hitanshu", "Ninad", "Amandeep" ],
"salary": [ 75000, 82000, 98000 ]
}

// a) Print an array of all employee ids
console.log(`Employee IDs: [${obj.id}]`);

// b) Print count of employees
console.log(`Count of Employees: ${obj.id.length}`);

// c) Print the name of the employee according to their id { key: value }
const employees = new Map();
for(let i =0; i<obj.id.length; i++){
employees[obj.id[i]] = obj.name[i];
}
console.log(employees);

// d) Store the salaries of all employees in an array
console.log(`Salaries of all Employees: [${obj.salary}]`);

// e) Calculate the average salary the company is paying to its employees
let sumOfSalaries = 0;
for(let i =0; i<obj.id.length; i++) {
sumOfSalaries += obj.salary[i];
}
console.log(`Average salary company paying is : 
${sumOfSalaries/obj.id.length}`)
```
# 2. Write a program in JavaScript to map the student ids, names and scores.
- a) Add data for 3 students (use map functions)
- b) Get Student Names using map functions
- c) Delete Student Scores using map functions
- d) Display 1 parameter (only value), 2 parameters (value + key), and 3 parameters (value + key + map) for the student

```
Sample Input:
"id": [ 1, 2, 3 ]
"name": [ 'Hitanshu', 'Ninad', 'Amandeep' ]
"scores": [ 90, 88, 92 ]
Output:
[ 'Hitanshu', 'Ninad', 'Amandeep' ]
-----one parameter-----
[ 1, 2, 3 ]
[ 'Hitanshu', 'Ninad', 'Amandeep' ]
[ 90, 88, 92 ]
-----two parameter-----
id 1, 2, 3
name Hitanshu,Ninad,Amandeep
scores 90,88,92
-----three parameter-----
id 1, 2, 3
Map(3) {
'id' => [ 67, 48, 29 ],
'name' => [ 'Hitanshu', 'Ninad', 'Amandeep' ],
'scores' => [ 90, 88, 92 ]
}
name Hitanshu,Ninad,Amandeep
Map(3) {
'id' => [ 1, 2, 3 ],
'name' => [ 'Hitanshu', 'Ninad', 'Amandeep' ],
'scores' => [ 90, 88, 92 ]
}
scores 90,88,92
Map(3) {
'id' => [ 1, 2, 3 ],
'name' => [ 'Hitanshu', 'Ninad', 'Amandeep' ],
'scores' => [ 90, 88, 92 ]
}

```
```

// a) Add data for 3 students (use map functions)
let students = new Map();
students.set("id",[1,2,3]);
students.set("name",[ 'Hitanshu', 'Ninad', 'Amandeep' ]);
students.set("scores",[ 90, 88, 92 ]);

// b) Get Student Names using map functions
let names= students.get("name");
console.log(names);

// d) Display 1 parameter (only value)
for(let [key,value] of students){
console.log(`${value}`)
}

// Display 2 parameters (value + key)
for(let [key,value] of students){
console.log(`${key} : ${value}`)
}

// Display 3 parameters (value + key + map)
console.log(students)

// c) Delete Student Scores using map functions
students.delete("scores");
console.log(students);
```
# 3. Write a JavaScript program to iterate over an array inputted by the user using mapping. Perform the square of all elements in the original array, store the squares in a new array and make a mapping for the squares and display it.
```
Sample Input:
[ 1, 2, 3, 4, 5 ]
Explanation:
Original Array = [ 1, 2, 3, 4, 5 ]
New Array = [ 1, 4, 9, 16, 25 ]
Mapping = squares => [ 1, 4, 9, 16, 25 ]
Output:
[ 1, 4, 9, 16, 25 ]
```
```
//To take input from Browser
let elements = prompt("Enter values of Array");
elements = elements.split(',');
elements = elements.map(i => parseInt(i));

//document.write(elements)
console.log(elements)
// let elements = [ 1, 2, 3, 4, 5 ];

//Squares of Input Elements
let squares = elements.map(num => num*num)
console.log(squares);

//Mapping of Elements with Squares
let mappedValues = new Map();
for(let element of elements){
mappedValues.set(element,squares[elements.indexOf(element)]);
}
console.log(mappedValues)

```
