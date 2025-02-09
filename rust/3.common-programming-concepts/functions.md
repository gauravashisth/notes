# Function:

## Key Points:
- **fn** is the keyword for function declaration.
- rust uses snake case as a convention for fn and variable names.
```rust
fn another_fn() {
  println!("another function");
}
fn main() {
  println!("hello");
  another_fn();
}
```
- here another_fn is defined before main fn in source code; but rust doesnt care where fn a function is defined, only that they're defined somewhere in a scope that can be seen by the caller.
