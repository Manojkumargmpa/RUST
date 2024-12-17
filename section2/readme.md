# Section2 (Variables and Mutability)

## Snake Case Formatting
1. All letters in lowercase and words separated by underscores.

## Interpolation with Curly Braces
1. To format a string, use `{}`.
2. Example: 
    ```rust
    println!("hello {}", name); // where name is the variable
    ```

## Positional Arguments to `println!`
1. 
    ```rust
    println!("hey {} and {}", var1, var2) // equivalent to println!("hey {0} and {1}", var1, var2)
    ```
2. The right-hand side of the equation is better because we can reuse `var1` in the string multiple times by simply keeping `{0}`.

## Underscore with Variables
1. To avoid warnings of unused variables.
2. Fix it by starting the variable with an underscore.

## Immutable and Mutable Variables
1. `let` variables are immutable by default in Rust.
2. The value assigned to the variable cannot be changed over the course of program execution.
3. To declare a mutable variable:
    ```rust
    let mut var = 34;
    ```
4. With the above kind of declaration, we may change the value of the variable but we cannot change the type of the variable.
5. Example: In C++, we can do `int x = 34.444`.
6. In Rust, once we use `let mut x = 3;`, `x` will forever be considered an integer and we can't later assign a float to `x` (i.e., `x = 3.3`) even though `x` is mutable.

## Rust Error Codes Index
1. This subsection is about finding more information other than what the compiler provides us about a specific error in Rust.
2. You don't have to remember the command. Whenever you compile an error code, the compiler suggests: 
    ```bash
    For more information about this error, try `rustc --explain E0425`
    ```
3. Just copy that command into the command line and execute it. This info is also available in the Rust error code index online.
4. So whenever you face an error, either in the terminal or by typing that error code on the website mentioned in 3, it will explain the error more clearly.

## Variable Shadowing
1. Shadowing refers to re-declaring a variable.
2. 
    ```rust
    let grams = "100.34";
    let grams = 100.34;
    let grams = 3;
    ```
3. The code in 2 won't produce any error. Unlike C++, we can re-declare the same variable with `let` again in the same scope.
4. A specific use case of where the re-declaration is helpful is explained in lecture 34.

## Scopes in Rust
1. To create a new block in Rust, simply use `{}`.
2. Example:
    ```rust
    let mut coffee_price = 34;
    {
         println!("{coffee_price}");
    }
    coffee_price = 3333;
    ```
3. Everything else is the same as in C++.

## Constants
1. We cannot use `mut` keywords with constants.
2. The difference between a constant and an immutable variable in Rust:
3. Immutable `let` variables are limited to a function's scope, but constants can be declared at any scope.
4. You cannot declare global variables using `let`; it has to be either `const` or `static`.
5. The value of a constant has to be known at compile time, unlike a variable.
6. To declare a constant, the convention is to keep all letters capitalized.
7. When declaring constants, we have to manually provide the type.
8. Example:
    ```rust
    const VARIABLE: u32 = 343;
    ```

## Type Aliases
1. A type alias is an alternate name that we can assign to an existing type.
2. Example:
    ```rust
    type Meters = i32;
    fn main() {
         let mile_race_length: Meters = 1600;
    }
    ```
3. It is just to enhance readability.

## Compiler Directives
1. A compiler directive is an annotation that tells the compiler how to parse the source code.
2. The word directive means an instruction or command.
3. We write the directive above the entity that we want the directive to be applied to.
4. For example, if we want to avoid the unused variables warning, we can either put an underscore or use the directive.
5. Example:
    ```rust
    #[allow(unused_variables)] // this applies to the next line, not to the entire block below it.
    let unused_var = 34;
    ```
6. To apply it to the entire block, use the directive above the function. So, on the whole, this directive can be applied to functions or variables.
7. To apply the directive to the file, put it at the top of the file and also use `!` after `#`.
8. Example:
    ```rust
    #![allow(unused_variables)] // applies the directive to the entire file
    ```



    
<!-- 1.snake case formatting- all letters in lowercase and words seperated by underscore.
2.Rust first evaluates the expression on the right hand side of the equation and then assigns it to the corresponding variables(like most langauges)

# Interpolation with curly braces
1. Inorder to format string use {}
2. Ex: println!("hello {}",name); where name is the variable.

# Positional arguments to println
1. println!("hey {} and {}",var1,var2)=== println!("hey {0} and {1} ",var1,var2)
2. the right hand side of lthe equation is better because we can resue var1 in the string multiple times by simply keeping {0}

# Underscore with variables
1. To avoid the warnings of unused variables.
2. Fix it by starting the variable with underscore.

# Immutable and mutable variables.
1. LET Variables are immutable by default in rust.
2. i.e the value assigned to the variable cannot be changed over the course of program execution.
3. Inorder to declare a mutable variable,let mut var=34;
4. with the above kind of declaration,we may change the value of variable but we cannot change the type of the variable.
5. Ex: in c++,we can do "int x=34.444"
6. In rust ,once we use "let mut x=3;" then x will forever be considered as integer and we can't later assign a float to x i.e x=3.3 even though x is mutable.

# Rust Error Codes Index
1. This sub section is about finding more information other than what the compiler provides us about a specific error in rust.
2. You don't have to remember the command,whenever you compile an error code,then the compiler along with showing the error suggests you like "For more information about this error, try `rustc --explain E0425`"
3. Just copy that command into the command line and execute it.This info is also available in rust eerror code index online.
4. So whenever you face the error,either in terminal or by typing that error code in the website mentioned in 3 will explain you the error more clearly.

# Variable shadowing
1. shadowing refers to re declaring a variable.
2. ` let grams="100.34";
    let grams=100.34;
    let grams=3;`
3. the code in 2 won't produce any error.Unlike c++,we can redeclare the same variable with let again in the same scope.
4. A specific use case of where the redeclaration is helpful is explained in lecture 34.

# Scopes in rust

1. to create a new block in rust ,simple use {} ..
2. Ex: ` let mut coffeprice=34;
        {
            println!("{coffeprice}")
        }
        coffeprice=3333;
        `

3. Remaining eveything else is same like c++.

# Constants

1. we cannot use mut keywords with constant.
2. then whats the difference between a constant and immutable variable in rust.
3. Immutable let Variables are limited to a function's scope but constants can be declared at any scope .(this point ..even i didnt get it)
4. Now i understand the 3 stmt,you cannot declare global variables using "let",it has to be either const or static.
5. The value of constant has to be known at compile time unlike variable.
6. Inorder to declare a constant,convention of const variables is to keep all lettes as capital.
7. When declaring constants we have to manually provide the type.
8. const VARIABLE: u32 = 343;


# Type Aliases
1. A type alias is an alternate name that we can assign to an existing type.
2. `type Meters = i32;
fn main(){

let mile_race_length : Meters=1600;

}`
3. It is just to enhance readibility.

# Compiler Directives

1. A compiler directive is an annotation that tells the compiler how to parse the source  code.
2. The word directive means an instruction or command.
3. We write the directive above the entity that we want the directive to be applied to .
4. for example,if we want to avoid the unused variables warning we can either put an underscore or use the directive.
5. Example:
6.   ` #[allow(unused_variables)] //this applies to the next line not to the entire block below it.
7.     let unused_var=34;
8.   `
9.   In order to apply it to entire block,use the directive above the function.So,on a whole,this directive can be applied to functions or variables.
10.  Inorder to apply the directive to the file ,put it at the top of the file and also use ! after #
11.  #![] will apply the directive to the entire file.
12.  

 -->
