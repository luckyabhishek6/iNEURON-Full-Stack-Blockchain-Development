# Javascript Assignment 5
## 1) Write a JavaScript program to get the volume of a Cylinder, Sphere andCone with four decimal places using objects and classes.
- Create classes for volumes for each geometric shape which returns the output using the getVolume() method.
- eg- to get volume of cylinder-let obj= new Cylinder(radius,height);
- obj.getVolume();
- Formulas for volumes of the shapes
- 1) Cylinder- Volume = πr2h  -->here r is the radius and h is the height of the cylinder.
- 2) Sphere- Volume= 4/3π𝑟3  -->where r is the radius
- 3) Cone- Volume= πr2h/3  -->where r is the radius and h is the height of the cone.
```
            class Cylinder{
                constructor(radius,height){
                    this.raidus=radius;
                    this.height=height
                }

                getVolume(){
                    return Math.PI*this.raidus*this.raidus*this.height;
                }
            }


            class Sphere{
                constructor(radius,height){
                    this.raidus=radius;
                    this.height=height
                }

                getVolume(){
                    return (Math.PI*this.raidus*this.raidus)*4/3;
                }
            }
            class Cone{
                constructor(radius,height){
                    this.raidus=radius;
                    this.height=height
                }

                getVolume(){
                    return (Math.PI*this.raidus*this.raidus*this.height)/3;
                }
            }

            const obj1 =  new Cylinder(2,3);
            console.log((obj1.getVolume()).toFixed(4));
            const obj2 =  new Sphere(2);
            console.log((obj2.getVolume()).toFixed(4));
            const obj3 =  new Cone(2,3);
            console.log((obj3.getVolume()).toFixed(4));
   ```
