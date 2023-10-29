# JavaScript Assignment 11
# 1. Write a JavaScript program to take an array as input from the user and calculatethe sum of numbers in odd places and the sum of numbers at even places.
- a) Print the difference between the two sums
- b) Print the number of elements in odd places
- c) Print the number of elements in even places
- d) Print the average of all elements in the arrayEven Places
 
Sample Input: [ 1, 2, 3, 4, 5 ]

Explanation:

Sum of Numbers at Odd Places = 1 + 3 + 5 = 9

Sum of Numbers at Even Places = 2 + 4 = 6

Difference = 9 - 6 = 3

Sample Output:

Difference = 3

Odd Elements = 3

Even Elements = 2

Average = 3

GCD = 3

```
//To take input from browser

let userInput = prompt('Enter comma separated numbers');
let arr= userInput.split(',');
arr = arr.map(i => parseInt(i));

//let arr = [1,2,3,4,5];
let oddEle = arr.filter(num => num%2 !=0);
console.log(oddEle);
let evenEle = arr.filter(num => num%2 ==0);
console.log(evenEle);

//Print the difference between the two sums

let sumInOdd = oddEle.reduce((sum,ele) => sum+ele);
console.log(sumInOdd)
let sumInEven = evenEle.reduce((sum,ele) => sum+ele);
console.log(sumInEven);
let difference = Math.abs(sumInEven-sumInOdd);
console.log(`Difference = ${difference}`);

//Print the number of elements in odd places

console.log(`Odd Elements = ${oddEle.length}`);

//Print the number of elements in even places

console.log(`Even Elements = ${evenEle.length}`);

//Print the average of all elements in the array

let avg = (sumInOdd+sumInEven)/arr.length;
console.log(`Average = ${avg}`);

//Print GCD of Sum of Numbers at Odd Places and Sum of Numbers at Even Places

let GCD = gcd(sumInEven,sumInOdd);
function gcd(a,b) {
if(b==0) return a;
else return gcd(b,a%b);
}
console.log(`GCD = ${GCD}`);
```
# 2. Write a JavaScript program to take 2 arrays from the user and check if the number 4 exists in any of the arrays, or both of the arrays.

```
Sample Input 1:
[ 1, 2, 3, 4, 5 ]
[ 4, 6, 1, 8, 2 ]
Output:
4 in both arrays
Sample Input 2:
[ 1, 2, 3, 6, 5 ]
[ 4, 6, 1, 8, 2 ]
Output:
4 in array 2
Sample Input 3:
[ 1, 2, 3, 4, 5 ]
[ 5, 6, 1, 8, 2 ]
Output:
4 in array 1
```
```
let arr1 = prompt("Enter array 1");
let arr2 = prompt("Enter array 2");
arr1= arr1.split(',');
arr1 = arr1.map(i => parseInt(i));
arr2= arr2.split(',');
arr2 = arr2.map(i => parseInt(i));
// let arr1= [1,2,3,4,5];
// let arr2= [6,1,8];
let ans = [0,0];
for(let i =0; i<arr1.length; i++){
if (arr1[i]==4){
ans[0]= 1;
}
}
for(let i =0; i<arr2.length; i++){
if (arr2[i]==4){
ans[1]= 1;
}
}
console.log(ans);
if (ans[0] !=0 && ans[1] !=0){
console.log("4 is present in Both arrays");
}else if(ans[0] !=0 && ans[1]==0){
console.log("4 is in array 1");
}else{
console.log("4 is in array 2")
}
```
# 3. Write a JavaScript program to flatten the array, ie, turns a deep array into a plain array.
- Note: Do not use array.flat();
```
Sample Input:
[ 1, 2, [ 3, 4, [ 5 ] ] ]
Output:
[ 1, 2, 3, 4, 5 ]
```
```
//Program to flatten the array
const flattenArray = function(arr, result = []) {
for (let i = 0; i < arr.length; i++) {
const value = arr[i];
if (Array.isArray(value)) {
flattenArray(value, result);
} else {
result.push(value);
}
}
return result;
};
//driver code
let arr= [ 1, 2, [ 3, 4, [ 5 ] ] ];
let result = flattenArray(arr);
console.log(result);
```
# 4. Write a JavaScript program to take an array as input from the user and:
- a) Store all duplicate elements in a separate array
- b) Remove the duplicate elements from the original array
```Sample Input:
[ 1, 2, 3, 2, 3, 4, 5 ]
Output:
Duplicate Elements = [ 2, 3 ]
Array without duplicate elements = [ 1, 2, 3, 4, 5 ]
```

```//To take input from browser
let arr = prompt("Enter the array elements");
arr = arr.split(',');
arr = arr.map(i => parseInt(i));
// let arr = [1,2,3,2,3,4,5];
// Program to Store all duplicate elements in a separate array
let duplicates = arr.filter( (num,index) =>{
if(arr.indexOf(num) != index) return num;
})
console.log(duplicates);
//Program to Remove the duplicate elements from the original array
arr = [...new Set(arr)];
console.log(arr);
```
# 5. Debug the given JavaScript program and execute the correct code.
```
function thirdLargest(arr, arr_size)
{
/* There should be
at least three elements */
if (arr_size < 3)
{
document.write(" Invalid Input "); return;
}
let first = arr[0];
for (let i = 1;i < arr_size ; i++)
if (arr[i] > first)
arr[i] = first;
let second = Number.MIN_VALUE; for (let i = 0;
i < arr_size ; i++)
if (arr[i] > first &&
arr[i] < second)
arr[i] = second;
let third = Number.MIN_VALUE; for (let i = 0;
i < arr_size ; i++)
if (arr[i] < third &&
arr[i] > second)
third = arr[i];
document.write("The third Largest " + "element is ", third); }
let arr = [12, 13, 1, 10, 34, 16]; let n = arr.length;
thirdLargest(arr, n);
```
```
//Correct Code
function thirdLargest(arr, arr_size) {
/* There should be at least three elements */
if (arr_size < 3){
document.write(" Invalid Input "); return;
}
let first = arr[0];
for (let i = 1; i < arr_size ; i++)
if (arr[i] > first)
first = arr[i];
let second = Number.MIN_VALUE;
for (let i = 0; i < arr_size ; i++)
if (arr[i]>second && arr[i]<first)
second = arr[i];
let third = Number.MIN_VALUE;
for (let i = 0; i < arr_size ; i++)
if (arr[i] > third && arr[i] < second)
third = arr[i];
document.write("The third Largest " + "element is ", third);
}
//driver code
let arr = [12, 13, 1, 10, 34, 16];;
let n = arr.length;
thirdLargest(arr, n)
```
