# Contents

- Python
- Rust
- Svelte

# Python

## 1. Lint

You are expected to run `pylint` on your code using this [pylintrc](./Codestyles/.pylintrc).

The recommendations that `pylint` makes aren't the word of God; you may ignore any that offends your common sense.

## 2. Typechecking

Use `mypy` to type-check your code.

## 3. Globals

Avoid global variables unless they are module-level constants. If they exist, they must be extremely visible and adequately documentedo

## 4. Scoping

Make use of lexical scoping.

## 5. Style

### 5.1 Semicolons

Do not use semicolons to terminate your lines, even to put two statements on the same line.

### 5.2 Line length

All lines should wrap to, at most, 80 characters. Exceptions to this rule include:

* Long URLs, addresses of any variety -- anything that may need to be copied.
* Import statements

### 5.3 Blank lines

Use blank lines to group chunks of code that make logical sense. Use your judgement, here. Top-level definitions should be separated by 2 lines.

### 5.4 Naming Conventiono

[PEP 8 Naming Conventions](https://www.python.org/dev/peps/pep-0008/#naming-conventions) must be used.

### 5.4 Comments & Documentation

Ideally, one's documentation should read like Arthur Conan Doyle; we can, however, settle for a lack of typographical or grammatical errors. Learn the use and abuse of docstrings.

# Rust

Recommendations on this front are rather limited as Rust's tooling already handles common pitfalls without any effort from the user.

## 1. Rust Analyzer

One is expected to run `rustfmt` on one's code using this [configuration](Codestyles/Rust/.rustfmt.toml).

## 2. Lint

Make use of `clippy`.

# Javascript

## 1. Code Formatting

Make use of `prettier` to format code with this [configuration](Codestyles/Svelte/.prettierrc).

## 2. Dependencies

Make note of your dependencies and do a cursory examination of the nature, state and future of those dependencies. If one of those seem uncertain, avoid the use of said dependency.

## 3. Style

### 3.1 Naming Convention

Opt for descriptive variable names. Shun abbreviations unless universally acknowledged. Restrict yourself to ASCII. Package names are `lowerCamelCase`, classes are `UpperCamelCase`, methods are `lowerCamelCase`, constants are `CONSTANT_CASE`, variables are `lowerCamelCase`.

Keep in mind that a `const` in JS isn't necessarily a constant in the mathematical and vernacular sense. Ascertain whether a variable is truly and deeply immutable before giving it `CONSTANT_CASE`.

# Svelte 

## 1. Code Formatting

Make use of `prettier` to format code with this [configuration](Codestyles/Svelte/.prettierrc).

## 2. Dependencies

Make note of your dependencies and do a cursory examination of the nature, state and future of those dependencies. If one of those seem uncertain, avoid the use of said dependency.

## 3. Style

Style considerations applicable to Javascript apply here as well.
