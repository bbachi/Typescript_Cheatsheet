# Typescript_Cheatsheet

## Template Strings

  *Template Strings can span multiple lines and embedded expressions.These strings are surrounded by the backtick/backquote (`)   character, and embedded expressions are of the form ${ expr }.*
  
  ```
   let fullName: string = `Bob Bobbington`;
   let age: number = 37;
   let sentence: string = `Hello, my name is ${ fullName }.
   
   I'll be ${ age + 1 } years old next month.`;
  ```
