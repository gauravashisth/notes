# Exercide 1: building a basic project

## description:
basic camke project is an executable build from a single source code file.
for simple projects like this, a **CMakeLists.txt** file with three commands is required.
  - cmake_minimum_required()
    - CMakeLists.txt must start by specifying a minimum CMake version.
    - establishes policy settings, and ensures that following CMake functions are run w/ compatible version of CMake.
  - project()
