# Variables and Constants:

## Key points(variables):
- by default variables in rust are immutable, though any variable can be made mutable by using **mut** keyword.

## Key points(constants):
- are valid for the entire time a program runs, within the scope in which they were declared.

(the above property makes constants useful for values in your application domain that mutiple parts of program might need to know about,
such as the maximum number of points any player of a game is allowed to earn, or the speed of light.)

## Difference between Variables and Constants:
- use of mut keyword
  - use of mut is allowed w/ variables
  - use of mut isn't allowed w/ constants, as they're always immutable
- having different keywords
  - let is used for definingvariables
  - const is used for defining constants
- the scope
  - asdf
  - constants can be declared in any scope, including global scope 
  (which means them useful for values that many parts of code needs to know about)
- asdf
  - asdf
  - constants may be set only to a constant expression, not the result of a value that could only be computed at runtime.
- naming convention
  - for variables have no such conventions
  - for constants it's using all uppercase w/ underscore b/w words
- example
  - variables: let THREE_HOURS_IN_SECONDS: u32 = 60 * 60 * 3;
  - constants: const THREE_HOURS_IN_SECONDS: u32 = 60 * 60 * 3;


## Shadowing:
- when declared a new variable w/ same name as previous variable, here the first variable is shadowed by seocnd one
- means its the second variable what compiler sees, when name of the variable is used.
- second variable overshadows the first, until either it itself is shadowed or the scope ends.

```rust
fn main() {
    let x = 5;
    let x = x + 1;
    {
        let x = x * 2;
        println!("The value of x in the inner scope is: {x}");  //12
    }
    println!("The value of x is: {x}");  //6
}
```
### NOTE:
- shadowing is different from marking a variable as **mut**, 'cause gets compiler error if we accidently 
try to reassign to this variable w/o using the let keyword.
- By using let, we can perform a few transformations on a value but have the variable be immutable 
after those transformations have been completed.
- other difference b/w mut and shadowing is that, 'cause we’re effectively creating a new variable when we use the let keyword again, 
we can change the type of the value but reuse the same name.
