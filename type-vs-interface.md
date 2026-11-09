1. Type Aliases vs Interface in Typescript: Core Differences and When to Use Them

Introduction:
TypeScript provides two powerful ways to define custom types: Type Aliases and Interfaces. Both help developers describe the structure of objects and improve code readability. However, they have some important differences that make them suitable for different situations.

Detailed Explanation:
An Interface is mainly used to define the structure of an objects. It describes which properties and methods an object should contain.

interface User{
name:string;
age:number;
}
const user:User={
name:"Shahriar",
age:28
}

Interface support extension using the extends keyword

interface Employee extends User{
salary:number;
}

On the other hand, a Type Alias uses the type keyword to create a custom name for almost any type, including primitives, unions, intersections, tuples, and object structures.

type ID = string | number;
type Admin = {
name:string;
role:"admin"
}

Type aliases can also combine types using intersections.

type Person = {
name:string;
}
type Developer = Person &{
language:string;
}

Conclusion
Use interfaces when defining object structures, especially when working with extensible APIs or class contracts. Choose type aliases when working with unions, intersections, tuples, or complex type combinations. Both are useful, and choosing between them depends on the requirements of your project.
