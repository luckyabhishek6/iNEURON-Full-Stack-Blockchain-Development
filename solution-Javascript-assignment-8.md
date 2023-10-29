# Javascript Assignment 8
# 1. Can we put duplicate values in the set object ? 
```
//No, we cannot. A Set is a collection that cannot contain duplicate elements.
console.log("solution question -->1") 
const setName = new Set();
setName.add(1)
setName.add(1)
setName.add(2)
setName.add(3)
setName.add(4)
console.log(setName)    //Set(4) { 1, 2, 3, 4 }
console.log("No We cannot")
console.log("A Set is a Collection that cannot contain duplicate elements.")
```

# 2. Write the syntax for
- a) Creating new set object
- b) Adding new element to set object
- c) Deleting element from set object
```
console.log("solution question -->2")    
const setName = new Set();      // creating set object.
setName.add(1);
setName.add(12);    // adds element in the set
setName.add(13);
console.log(setName)
setName.delete(13)  //delete elements from set
console.log(setName)
```

# 3. Create a set object with four random numbers from 0 to 10. Check if this newly created set object has 8 in it. Use set object methods.
```
console.log("solution question -->3")    
const set = new Set();
while(set.size !=4){
set.add( Math.round((Math.random()*10)) );
}
console.log(set);
const ishas = set.has(8)  // retuens true if present otherwise false.
console.log(ishas);
```
