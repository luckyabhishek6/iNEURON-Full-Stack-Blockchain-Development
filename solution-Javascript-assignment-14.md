# JavaScript Assignment 14
# 1. Write a JavaScript program to:
- a) filter employees according to department = IT
- b) filter employees who earn a salary < 65000
```
let employees = [
{
"id": 1,
"name":"Abhinav",
"department":"IT",
"Salary":75000
},
{
"id": 2,
"name":"Gaurav",
"department":"Sales",
"Salary":52000
},
{
"id": 3,
"name":"Raj",
"department":"IT",
"Salary":64000
}]

// a) filter employees according to department = IT
let itEmployees = employees.filter(employee => employee.department == "IT");
console.log(itEmployees);

// b) filter employees who earn a salary < 65000
let lessSalaryEmployees = employees.filter(employee => employee.Salary < 
65000);
console.log(lessSalaryEmployees);
```
# 2. Write a JavaScript program to filter the hospitals according to:
- a) Number of Beds > 200
- b) Availability of Beds = Yes
- c) Location = Pune
```let hospitals = [
{
"id": 1,
"name":"Hospital A",
"location":"Delhi",
"noOfBeds":450,
"availability":"Yes"
},
{
"id": 2,
"name":"Hospital B",
"location":"Pune",
"noOfBeds":150,
"availability":"No"
},
{
"id": 3,
"name":"Hospital C",
"location":"Pune",
"noOfBeds":350,
"availability":"Yes"
}]

// a) Number of Beds > 200
console.log(
hospitals.filter(hospital => hospital.noOfBeds > 200)
);

// b) Availability of Beds = Yes
console.log(
hospitals.filter(hospital => hospital.availability == "Yes")
);

// c) Location = Pune
console.log(
hospitals.filter(hospital => hospital.location == "Pune")
);
```
