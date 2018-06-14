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
