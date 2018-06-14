# Typescript_Cheatsheet

## Template Strings

  *Template Strings can span multiple lines and embedded expressions.These strings are surrounded by the backtick/backquote (`)   character, and embedded expressions are of the form ${ expr }.*
  
  ```
   let fullName: string = `Bob Bobbington`;
   let age: number = 37;
   let sentence: string = `Hello, my name is ${ fullName }.
   
   I'll be ${ age + 1 } years old next month.`;
  ```
  
  ## Type assertions
  
  *Sometimes you’ll end up in a situation where you’ll know more about a value than TypeScript does. Usually this will happen   when you know the type of some entity could be more specific than its current type.*
 
 *Type assertions are a way to tell the compiler “trust me, I know what I’m doing.” A type assertion is like a type cast in  other languages, but performs no special checking or restructuring of data. It has no runtime impact, and is used purely by the compiler. TypeScript assumes that you, the programmer, have performed any special checks that you need.*
 
 ### Two kinds
 
 ```
  let someValue: any = "this is a string";
  let strLength: number = (<string>someValue).length;
 ```
 
 ```
  let someValue: any = "this is a string";
  let strLength: number = (someValue as string).length;
 ```

## Destructuring

 **Array destructuring**
 
  The simplest form of destructuring
  
 ```
  let input = [1, 2];
  let [first, second] = input;
  console.log(first); // outputs 1
  console.log(second); // outputs 2
 ```
 
  Destructuring works with already-declared variables as well:
  
  ```
   // swap variables
   [first, second] = [second, first];
  ```
  
  And with parameters to a function:
  
  ```
  function f([first, second]: [number, number]) {
    console.log(first);
    console.log(second);
  }
  f([1, 2]);
  ```
  
  You can create a variable for the remaining items in a list using the syntax ...:
  
  ```
   let [first, ...rest] = [1, 2, 3, 4];
   console.log(first); // outputs 1
   console.log(rest); // outputs [ 2, 3, 4 ]
  ```
  
  Of course, since this is JavaScript, you can just ignore trailing elements you don’t care about:
  
  ```
   let [first] = [1, 2, 3, 4];
   console.log(first); // outputs 1
  ```
  
  Or other elements:
  
  ```
  let [, second, , fourth] = [1, 2, 3, 4];

  ```
