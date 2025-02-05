# Variables and constants:

## key info(variables):
- by default variables in rust are immutable, though any variable can be made mutable by using **mut** keyword.

## key info(constants):
- are valid for the entire time a program runs, within the scope in which they were declared.

(the above property makes constants useful for values in your application domain that mutiple parts of program might need to know about,
such as the maximum number of points any player of a game is allowed to earn, or the speed of light.)

### difference between variables and constants:
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
- 
  - 
  - constants may be set only to a constant expression, not the result of a value that could only be computed at runtime.
- naming convention
  - for variables have no such conventions
  - for constants it's using all uppercase w/ underscore b/w words
- example
  - variables: let THREE_HOURS_IN_SECONDS: u32 = 60 * 60 * 3;
  - constants: const THREE_HOURS_IN_SECONDS: u32 = 60 * 60 * 3;


## shadowing:
```rust
fn main() {
    let x = 5;

    let x = x + 1;

    {
        let x = x * 2;
        println!("The value of x in the inner scope is: {x}");
    }

    println!("The value of x is: {x}");
}
```
