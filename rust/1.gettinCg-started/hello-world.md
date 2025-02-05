# Writing a hello world porgram in rust:

## rust program
```rust
fn main() {
  println!("hello world");
}
```

## compiling and running the executable
- rustc main.rs
- ./main
- hello world

## understanding the rust program
- the **main** function is special, it's the first code that runs in every executable rust program.
- rust style is to indent with 4 spaces, not tab.
- **println!** calls a rust macro. when calling a function, it would be entered as **println** (w/o !).
  this point will be discussed in ch 19, and remember that using **!** means you're calling a macro instead of normal function.
