# Cargo

## Key Features:

- build system and package manager for rust.
- building your
- downloading and building those libraries, your code depends on.
  (We call the libraries that your code needs dependencies.)`

## creating a project with cargo:

```shell
$ crago new project_name
$ cd porject_name
```

### NOTE:
- cargo also initialize a new git repo along with *.gitignore* file.
- cargo uses git as a default version control system, can use different VCS or no VCS by using _--vcs_ flag with **cargo new**.

### File name: Cargo.toml
```toml
[package]
name = "project_name"
version = "0.1.0"
edition = "2021"

[dependencies]
```

- file is in TOML (Toms's Obvious, Minimal Language) foramt, that's the Cargo's configuration format.
- **package[]**, is a section heading that indicates that the following statements are configuring a package.
- **dependencies[]**, is the start of a section where to list any of your porject's dependencies.
  - in rust, packages of code are reffered to as crates, we won’t need any other crates for this project.
  - But we will in the first project in Chapter 2, so we’ll use this dependencies section then.

