# 1. Introduction to TypeScript

TypeScript is a strongly typed programming language developed by Microsoft that builds on top of JavaScript.

It adds:

- Static typing
- Interfaces
- Classes
- Modern JavaScript features
- Better development tools

TypeScript code is compiled into JavaScript because browsers understand JavaScript, not TypeScript directly.

---

# What is TypeScript?

TypeScript is:

- Open-source
- Object-oriented
- A superset of JavaScript
- Designed for scalable applications

Every valid JavaScript code is also valid TypeScript code.

---

# Why TypeScript?

JavaScript applications become difficult to manage when projects grow larger.

TypeScript solves many development problems such as:

- Runtime errors
- Poor scalability
- Difficult debugging
- Weak type safety
- Hard maintenance

---

# JavaScript vs TypeScript

| JavaScript | TypeScript |
|---|---|
| Dynamically typed | Statically typed |
| Runtime error checking | Compile-time error checking |
| Harder for large apps | Better for large apps |
| Less tooling support | Excellent tooling support |
| Difficult maintenance | Easier maintenance |

---

# Key Features of TypeScript

## Static Typing

```ts
let username: string = "Ali";
```

TypeScript ensures `username` always remains a string.

---

## Early Error Detection

```ts
let age: number = "Twenty";
```

TypeScript immediately shows an error because `"Twenty"` is not a number.

---

## Better IntelliSense

TypeScript provides:

- Auto-completion
- Smart suggestions
- Better navigation
- Refactoring support

---

## Object-Oriented Programming

TypeScript supports:

- Classes
- Interfaces
- Inheritance
- Encapsulation
- Abstraction

---

# How TypeScript Works

## Step 1 — Write TypeScript Code

```ts
let message: string = "Hello TypeScript";
```

---

## Step 2 — Compile TypeScript

```bash
tsc app.ts
```

---

## Step 3 — JavaScript Generated

```js
var message = "Hello TypeScript";
```

---

## Step 4 — Run JavaScript

```bash
node app.js
```

---

# Advantages of TypeScript

- Cleaner code
- Better scalability
- Easier debugging
- Strong type safety
- Better collaboration
- Professional development structure

---

# Where TypeScript is Used

TypeScript is commonly used in:

- React applications
- Angular applications
- Node.js backend
- Full-stack development
- Enterprise software
- APIs and microservices

---

# Popular Companies Using TypeScript

- Microsoft
- Google
- Slack
- Airbnb
- Discord
- Asana

---

# Example Program

```ts
function greet(name: string): string {
  return `Hello ${name}`;
}

console.log(greet("Ali"));
```

---

# Output

```bash
Hello Ali
```

---

# Conclusion

TypeScript improves JavaScript development by adding strong typing, better tooling, and scalable architecture.

It helps developers build professional, maintainable, and production-ready applications efficiently.


# 2. Installing TypeScript

This section explains how to install and configure TypeScript for development.

---

# Prerequisites

Before installing TypeScript, make sure the following tools are installed:

- Node.js
- npm (Node Package Manager)
- VS Code (Recommended)

---

# Install Node.js

Download Node.js from the official website:

```bash
https://nodejs.org
```

After installation, verify Node.js and npm versions.

---

# Check Node.js Version

```bash
node -v
```

## Example Output

```bash
v22.0.0
```

---

# Check npm Version

```bash
npm -v
```

## Example Output

```bash
10.5.0
```

---

# Install TypeScript Globally

Global installation allows TypeScript to be used anywhere in the system.

```bash
npm install -g typescript
```

---

# Verify TypeScript Installation

```bash
tsc -v
```

## Example Output

```bash
Version 5.8.2
```

---

# Install TypeScript Locally

Local installation is recommended for professional projects.

```bash
npm install --save-dev typescript
```

---

# Difference Between Global & Local Installation

| Global Installation | Local Installation |
|---|---|
| Available system-wide | Available only inside project |
| Good for learning | Recommended for production |
| Shared version | Project-specific version |

---

# Create a TypeScript Project

## Step 1 — Create Folder

```bash
mkdir typescript-project
```

---

## Step 2 — Move Into Folder

```bash
cd typescript-project
```

---

## Step 3 — Initialize Node.js

```bash
npm init -y
```

This creates:

```bash
package.json
```

---

# Install TypeScript in Project

```bash
npm install --save-dev typescript
```

---

# Initialize TypeScript Configuration

```bash
npx tsc --init
```

This command creates:

```bash
tsconfig.json
```

---

# What is tsconfig.json?

`tsconfig.json` is the main configuration file for TypeScript projects.

It controls:

- Compiler settings
- File structure
- Output directory
- Strict type checking
- Module system

---

# Basic tsconfig.json Example

```json
{
  "compilerOptions": {
    "target": "ES6",
    "module": "commonjs",
    "strict": true
  }
}
```

---

# Install VS Code Extensions

Recommended extensions:

- TypeScript Importer
- ESLint
- Prettier
- Error Lens

---

# Create First TypeScript File

Create a file:

```bash
app.ts
```

---

# Write TypeScript Code

```ts
let message: string = "Hello TypeScript";

console.log(message);
```

---

# Compile TypeScript File

```bash
tsc app.ts
```

After compilation:

```bash
app.js
```

will be generated automatically.

---

# Run JavaScript File

```bash
node app.js
```

---

# Output

```bash
Hello TypeScript
```

---

# Watch Mode

Watch mode automatically recompiles files after changes.

```bash
tsc --watch
```

---

# Compile Entire Project

```bash
tsc
```

This compiles all TypeScript files in the project.

---

# Recommended Project Structure

```bash
project/
│
├── src/
│   └── app.ts
│
├── dist/
│
├── package.json
├── tsconfig.json
└── README.md
```

---

# Important Installation Commands

| Command | Purpose |
|---|---|
| npm install -g typescript | Install globally |
| npm install --save-dev typescript | Install locally |
| tsc -v | Check TypeScript version |
| tsc --init | Create tsconfig.json |
| tsc app.ts | Compile file |
| tsc --watch | Enable watch mode |

---

# Common Installation Errors

## Command Not Found

```bash
tsc: command not found
```

### Solution

Install TypeScript globally:

```bash
npm install -g typescript
```

---

## Permission Errors

### Solution

Run terminal as administrator or use:

```bash
sudo npm install -g typescript
```

---

# Best Practices

- Prefer local installation in projects
- Use strict mode
- Keep TypeScript updated
- Organize files properly
- Use VS Code for best experience

---

# Conclusion

TypeScript installation is simple and professional project setup becomes easier with Node.js and tsconfig.json.

After installation, developers can start building scalable and strongly typed applications efficiently.

# 3. TypeScript Project Setup

This section explains how to properly create and configure a professional TypeScript project from scratch.

---

# Why Project Setup is Important

A proper project structure helps developers:

- Organize files efficiently
- Maintain clean architecture
- Improve scalability
- Simplify debugging
- Collaborate professionally

---

# Step 1 — Create Project Folder

Create a new folder for the project.

```bash
mkdir typescript-project
```

---

# Step 2 — Open Project Folder

```bash
cd typescript-project
```

---

# Step 3 — Initialize Node.js Project

```bash
npm init -y
```

This command creates:

```bash
package.json
```

---

# What is package.json?

`package.json` stores:

- Project information
- Dependencies
- Scripts
- Project version
- Package settings

---

# Example package.json

```json
{
  "name": "typescript-project",
  "version": "1.0.0",
  "description": "TypeScript learning project",
  "main": "index.js",
  "scripts": {
    "start": "node dist/index.js"
  }
}
```

---

# Step 4 — Install TypeScript

## Local Installation

```bash
npm install --save-dev typescript
```

---

# Step 5 — Initialize TypeScript

```bash
npx tsc --init
```

This creates:

```bash
tsconfig.json
```

---

# What is tsconfig.json?

`tsconfig.json` is the main TypeScript configuration file.

It controls:

- Compiler behavior
- Output settings
- File structure
- Strict type checking
- Module system

---

# Basic tsconfig.json

```json
{
  "compilerOptions": {
    "target": "ES6",
    "module": "commonjs",
    "strict": true
  }
}
```

---

# Recommended Professional tsconfig.json

```json
{
  "compilerOptions": {
    "target": "ES6",
    "module": "commonjs",
    "rootDir": "./src",
    "outDir": "./dist",
    "strict": true,
    "esModuleInterop": true,
    "skipLibCheck": true
  }
}
```

---

# Understanding Important Compiler Options

| Option | Purpose |
|---|---|
| target | JavaScript version output |
| module | Module system |
| rootDir | Source folder |
| outDir | Compiled output folder |
| strict | Enable strict type checking |
| esModuleInterop | Better module compatibility |
| skipLibCheck | Faster compilation |

---

# Step 6 — Create Project Structure

Recommended folder structure:

```bash
typescript-project/
│
├── src/
│   ├── index.ts
│   ├── app.ts
│
├── dist/
│
├── node_modules/
│
├── package.json
├── package-lock.json
├── tsconfig.json
└── README.md
```

---

# Folder Explanation

| Folder/File | Purpose |
|---|---|
| src | TypeScript source code |
| dist | Compiled JavaScript output |
| node_modules | Installed packages |
| package.json | Project information |
| tsconfig.json | TypeScript configuration |
| README.md | Project documentation |

---

# Step 7 — Create Source File

Inside `src/` create:

```bash
index.ts
```

---

# Example TypeScript Code

```ts
function greet(name: string): string {
  return `Hello ${name}`;
}

console.log(greet("Ali"));
```

---

# Step 8 — Compile TypeScript

```bash
npx tsc
```

Compiled JavaScript files will appear inside:

```bash
dist/
```

---

# Generated Output Structure

```bash
dist/
│
└── index.js
```

---

# Step 9 — Run JavaScript File

```bash
node dist/index.js
```

---

# Output

```bash
Hello Ali
```

---

# Enable Watch Mode

Watch mode automatically recompiles files whenever changes occur.

```bash
npx tsc --watch
```

---

# Add Useful npm Scripts

Inside `package.json`:

```json
{
  "scripts": {
    "build": "tsc",
    "start": "node dist/index.js",
    "dev": "tsc --watch"
  }
}
```

---

# Run Build Script

```bash
npm run build
```

---

# Run Project

```bash
npm start
```

---

# Run Watch Mode

```bash
npm run dev
```

---

# Install Node Type Definitions

For Node.js projects:

```bash
npm install --save-dev @types/node
```

---

# Install Development Tools

Recommended tools:

```bash
npm install --save-dev eslint prettier
```

---

# VS Code Recommended Extensions

- ESLint
- Prettier
- Error Lens
- TypeScript Importer

---

# Best Practices for Project Setup

- Keep source code inside `src`
- Keep compiled files inside `dist`
- Enable strict mode
- Use local TypeScript installation
- Use meaningful folder names
- Organize modules properly

---

# Common Beginner Mistakes

| Mistake | Problem |
|---|---|
| Writing code outside src | Poor structure |
| Not using strict mode | Weak type safety |
| Mixing JS and TS randomly | Confusing architecture |
| No folder organization | Hard maintenance |

---

# Professional Workflow

## Development Flow

```bash
Write TypeScript → Compile → Generate JavaScript → Run Application
```

---

# Example Full Workflow

## Create File

```bash
src/index.ts
```

---

## Write Code

```ts
const course: string = "TypeScript";

console.log(course);
```

---

## Compile

```bash
npx tsc
```

---

## Run

```bash
node dist/index.js
```

---

# Output

```bash
TypeScript
```

---

# Conclusion

A professional TypeScript setup creates a scalable and maintainable development environment.

Good project structure improves:

- Readability
- Collaboration
- Debugging
- Scalability
- Professional development workflow

# 3. Basic Syntax

This section explains the basic syntax of TypeScript and how TypeScript code is written.

---

# What is Syntax?

Syntax is the set of rules used to write code correctly in a programming language.

TypeScript syntax is very similar to JavaScript syntax but includes type annotations.

---

# First TypeScript Program

```ts
console.log("Hello TypeScript");
```

---

# Output

```bash
Hello TypeScript
```

---

# Variables in TypeScript

Variables are used to store data.

---

# Declaring Variables

## Using let

```ts
let username: string = "Ali";
```

---

## Using const

```ts
const age: number = 22;
```

---

## Using var

```ts
var city: string = "Lahore";
```

---

# Difference Between let, const, and var

| Keyword | Scope | Reassignable | Recommended |
|---|---|---|---|
| var | Function | Yes | No |
| let | Block | Yes | Yes |
| const | Block | No | Yes |

---

# Type Annotations

Type annotations define the data type of a variable.

---

# String Type

```ts
let firstName: string = "Ahmed";
```

---

# Number Type

```ts
let price: number = 100;
```

---

# Boolean Type

```ts
let isLoggedIn: boolean = true;
```

---

# Type Inference

TypeScript can automatically detect types.

```ts
let country = "Pakistan";
```

TypeScript automatically understands this is a string.

---

# Comments in TypeScript

Comments are used to explain code.

---

# Single Line Comment

```ts
// This is a single line comment
```

---

# Multi-line Comment

```ts
/*
This is a
multi-line comment
*/
```

---

# Console Output

Use `console.log()` to display output.

```ts
console.log("Welcome");
```

---

# String Concatenation

```ts
let firstName: string = "Ali";
let lastName: string = "Khan";

console.log(firstName + " " + lastName);
```

---

# Template Literals

Template literals use backticks.

```ts
let name: string = "Ali";

console.log(`Welcome ${name}`);
```

---

# Output

```bash
Welcome Ali
```

---

# Case Sensitivity

TypeScript is case-sensitive.

```ts
let userName = "Ali";
let username = "Ahmed";
```

Both variables are different.

---

# Naming Rules

## Valid Variable Names

```ts
let age = 22;
let firstName = "Ali";
let user_id = 100;
```

---

## Invalid Variable Names

```ts
let 1name = "Ali";
let user-name = "Ahmed";
```

---

# Reserved Keywords

Reserved keywords cannot be used as variable names.

Examples:

```ts
let class = "Web";
let function = "Test";
```

These produce errors.

---

# Semicolons

Semicolons are optional but recommended.

```ts
let language: string = "TypeScript";
```

---

# Code Blocks

Code blocks are written using curly braces `{}`.

```ts
if (true) {
  console.log("Inside block");
}
```

---

# Basic Operators

## Addition

```ts
let sum = 10 + 5;
```

---

## Subtraction

```ts
let result = 20 - 10;
```

---

## Multiplication

```ts
let total = 5 * 2;
```

---

## Division

```ts
let value = 10 / 2;
```

---

# Comparison Operators

```ts
let a = 10;
let b = 20;

console.log(a < b);
```

---

# Logical Operators

## AND Operator

```ts
console.log(true && true);
```

---

## OR Operator

```ts
console.log(true || false);
```

---

## NOT Operator

```ts
console.log(!true);
```

---

# Conditional Statements

## if Statement

```ts
let age: number = 18;

if (age >= 18) {
  console.log("Adult");
}
```

---

## if...else Statement

```ts
let marks: number = 40;

if (marks >= 50) {
  console.log("Pass");
} else {
  console.log("Fail");
}
```

---

# Loops

## for Loop

```ts
for (let i = 1; i <= 5; i++) {
  console.log(i);
}
```

---

## while Loop

```ts
let count = 1;

while (count <= 3) {
  console.log(count);
  count++;
}
```

---

# Functions

```ts
function greet(): void {
  console.log("Hello");
}

greet();
```

---

# Simple User Input Example

```ts
let username: string = "Ali";

console.log(`Welcome ${username}`);
```

---

# Output

```bash
Welcome Ali
```

---

# Basic TypeScript File Example

```ts
// Variables
let course: string = "TypeScript";
let duration: number = 30;
let isFree: boolean = true;

// Output
console.log(course);
console.log(duration);
console.log(isFree);
```

---

# Output

```bash
TypeScript
30
true
```

---

# Common Beginner Mistakes

| Mistake | Problem |
|---|---|
| Using wrong data type | Type errors |
| Forgetting type annotations | Poor readability |
| Using var everywhere | Scope issues |
| Invalid variable names | Syntax errors |

---

# Best Practices

- Use `const` whenever possible
- Use meaningful variable names
- Prefer template literals
- Avoid using `var`
- Write clean comments
- Keep code readable

---

# Conclusion

Basic syntax is the foundation of TypeScript development.

Understanding variables, operators, conditions, loops, comments, and basic structure helps developers write clean and professional TypeScript code.

# 4. Data Types in TypeScript

Data types define the kind of data a variable can store.

TypeScript uses static typing, which helps developers catch errors during development instead of runtime.

---

# Why Data Types are Important

Data types help:

- Prevent programming errors
- Improve code readability
- Make applications scalable
- Improve auto-completion
- Increase code safety

---

# Basic Data Types in TypeScript

TypeScript provides multiple built-in data types.

---

# 1. String Type

The `string` type stores textual data.

---

## Example

```ts
let firstName: string = "Ali";
```

---

## Multiple String Examples

```ts
let country: string = "Pakistan";
let course: string = "TypeScript";
```

---

## String Concatenation

```ts
let firstName: string = "Ali";
let lastName: string = "Khan";

console.log(firstName + " " + lastName);
```

---

## Template Literals

```ts
let name: string = "Ahmed";

console.log(`Welcome ${name}`);
```

---

# Output

```bash
Welcome Ahmed
```

---

# 2. Number Type

The `number` type stores numeric values.

---

## Example

```ts
let age: number = 22;
```

---

## Decimal Numbers

```ts
let price: number = 99.99;
```

---

## Negative Numbers

```ts
let temperature: number = -5;
```

---

## Arithmetic Operations

```ts
let a: number = 10;
let b: number = 5;

console.log(a + b);
console.log(a - b);
console.log(a * b);
console.log(a / b);
```

---

# Output

```bash
15
5
50
2
```

---

# 3. Boolean Type

The `boolean` type stores `true` or `false`.

---

## Example

```ts
let isLoggedIn: boolean = true;
```

---

## More Examples

```ts
let isAdmin: boolean = false;
let isActive: boolean = true;
```

---

# Boolean with Conditions

```ts
let age: number = 20;

console.log(age >= 18);
```

---

# Output

```bash
true
```

---

# 4. Any Type

The `any` type can store any type of value.

---

## Example

```ts
let data: any = "Hello";

data = 100;
data = true;
```

---

# Why Avoid any?

Using `any` removes TypeScript safety features.

---

## Bad Practice Example

```ts
let value: any = "Hello";

value = 500;
value = false;
```

---

# Best Practice

Avoid using `any` unless absolutely necessary.

---

# 5. Unknown Type

`unknown` is safer than `any`.

---

## Example

```ts
let value: unknown;

value = "Hello";
value = 100;
```

---

# Type Checking Before Use

```ts
let value: unknown = "TypeScript";

if (typeof value === "string") {
  console.log(value.toUpperCase());
}
```

---

# Output

```bash
TYPESCRIPT
```

---

# 6. Void Type

The `void` type is mainly used for functions that return nothing.

---

## Example

```ts
function showMessage(): void {
  console.log("Welcome");
}
```

---

# 7. Null Type

`null` represents an empty value.

---

## Example

```ts
let emptyValue: null = null;
```

---

# 8. Undefined Type

`undefined` means a variable has not been assigned a value.

---

## Example

```ts
let user: undefined = undefined;
```

---

# Difference Between null and undefined

| null | undefined |
|---|---|
| Intentionally empty | Value not assigned |
| Assigned manually | Assigned automatically |

---

# 9. Never Type

The `never` type represents values that never occur.

---

## Example

```ts
function throwError(message: string): never {
  throw new Error(message);
}
```

---

# 10. Array Type

Arrays store multiple values.

---

## Number Array

```ts
let numbers: number[] = [1, 2, 3];
```

---

## String Array

```ts
let users: string[] = ["Ali", "Ahmed"];
```

---

# Array Operations

```ts
let fruits: string[] = ["Apple", "Banana"];

fruits.push("Orange");

console.log(fruits);
```

---

# Output

```bash
["Apple", "Banana", "Orange"]
```

---

# 11. Tuple Type

Tuples store fixed-length arrays with predefined types.

---

## Example

```ts
let student: [string, number];

student = ["Ali", 22];
```

---

# Invalid Tuple Example

```ts
student = [22, "Ali"];
```

This produces an error.

---

# 12. Enum Type

Enums store named constants.

---

## Example

```ts
enum Role {
  Admin,
  User,
  Guest
}

let currentRole: Role = Role.Admin;
```

---

# 13. Object Type

Objects store related data.

---

## Example

```ts
let person: {
  name: string;
  age: number;
};

person = {
  name: "Ali",
  age: 22
};
```

---

# Type Inference

TypeScript can automatically detect types.

---

## Example

```ts
let language = "TypeScript";
```

TypeScript automatically infers this as a string.

---

# Explicit Typing vs Type Inference

| Explicit Typing | Type Inference |
|---|---|
| Type written manually | Type detected automatically |
| More readable | Less code |
| Better for teams | Faster coding |

---

# Type Aliases

Type aliases create reusable custom types.

---

## Example

```ts
type UserID = string | number;

let id: UserID = 100;
```

---

# Union Types

Union types allow multiple possible types.

---

## Example

```ts
let code: string | number;

code = "TS100";
code = 500;
```

---

# Literal Types

Literal types restrict exact values.

---

## Example

```ts
let direction: "left" | "right";

direction = "left";
```

---

# Readonly Type

Readonly prevents value modification.

---

## Example

```ts
const colors: readonly string[] = ["Red", "Blue"];
```

---

# Common Beginner Mistakes

| Mistake | Problem |
|---|---|
| Overusing any | Removes type safety |
| Wrong type assignment | Type errors |
| Ignoring strict mode | Unsafe code |
| Mixing incompatible types | Compilation errors |

---

# Best Practices

- Use strict typing
- Avoid using `any`
- Use type inference wisely
- Create reusable types
- Use meaningful variable names
- Keep data structures clean

---

# Complete Example

```ts
// String
let name: string = "Ali";

// Number
let age: number = 22;

// Boolean
let isStudent: boolean = true;

// Array
let skills: string[] = ["HTML", "CSS", "TypeScript"];

// Object
let user: { name: string; age: number } = {
  name: "Ali",
  age: 22
};

console.log(user);
```

---

# Output

```bash
{
  name: 'Ali',
  age: 22
}
```

---

# Conclusion

Data types are one of the most important parts of TypeScript.

Strong typing improves:

- Code quality
- Scalability
- Debugging
- Readability
- Application safety

Understanding data types is essential for becoming a professional TypeScript developer.

# 5. Functions in TypeScript

Functions are reusable blocks of code used to perform specific tasks.

TypeScript functions provide:

- Type safety
- Better readability
- Reusability
- Better error checking
- Cleaner architecture

---

# Why Functions are Important

Functions help developers:

- Avoid repeating code
- Organize logic
- Improve maintainability
- Create scalable applications

---

# Basic Function Syntax

```ts
function functionName() {
  // code
}
```

---

# Simple Function Example

```ts
function greet() {
  console.log("Hello TypeScript");
}

greet();
```

---

# Output

```bash
Hello TypeScript
```

---

# Function with Parameters

Parameters allow functions to receive values.

---

## Example

```ts
function greet(name: string) {
  console.log(`Hello ${name}`);
}

greet("Ali");
```

---

# Output

```bash
Hello Ali
```

---

# Multiple Parameters

```ts
function add(a: number, b: number) {
  console.log(a + b);
}

add(10, 5);
```

---

# Output

```bash
15
```

---

# Function Return Type

TypeScript allows defining return types.

---

## Example

```ts
function multiply(a: number, b: number): number {
  return a * b;
}
```

---

# Calling Function

```ts
console.log(multiply(5, 2));
```

---

# Output

```bash
10
```

---

# Void Return Type

`void` means the function returns nothing.

---

## Example

```ts
function showMessage(): void {
  console.log("Welcome");
}
```

---

# Optional Parameters

Optional parameters use `?`.

---

## Example

```ts
function greetUser(name?: string) {
  console.log(name);
}

greetUser();
greetUser("Ahmed");
```

---

# Output

```bash
undefined
Ahmed
```

---

# Default Parameters

Default values are used if no argument is provided.

---

## Example

```ts
function welcome(user: string = "Guest") {
  console.log(`Welcome ${user}`);
}

welcome();
welcome("Ali");
```

---

# Output

```bash
Welcome Guest
Welcome Ali
```

---

# Rest Parameters

Rest parameters accept multiple values.

---

## Example

```ts
function total(...numbers: number[]) {
  let sum = 0;

  for (let number of numbers) {
    sum += number;
  }

  return sum;
}

console.log(total(1, 2, 3, 4));
```

---

# Output

```bash
10
```

---

# Anonymous Functions

Functions without names are called anonymous functions.

---

## Example

```ts
let greeting = function () {
  console.log("Hello");
};

greeting();
```

---

# Arrow Functions

Arrow functions provide shorter syntax.

---

## Basic Arrow Function

```ts
const greet = () => {
  console.log("Hello");
};
```

---

# Arrow Function with Parameters

```ts
const add = (a: number, b: number): number => {
  return a + b;
};
```

---

# Short Arrow Function

```ts
const square = (num: number): number => num * num;
```

---

# Output

```bash
console.log(square(5));
```

```bash
25
```

---

# Function Type Aliases

Functions can use custom types.

---

## Example

```ts
type MathOperation = (a: number, b: number) => number;

const subtract: MathOperation = (a, b) => a - b;
```

---

# Function with Object Parameter

```ts
function displayUser(user: { name: string; age: number }) {
  console.log(user.name);
}
```

---

# Example Usage

```ts
displayUser({
  name: "Ali",
  age: 22
});
```

---

# Function with Interface

```ts
interface User {
  name: string;
  age: number;
}

function showUser(user: User) {
  console.log(user.name);
}
```

---

# Higher-Order Functions

Functions that receive another function as a parameter.

---

## Example

```ts
function process(
  callback: () => void
) {
  callback();
}

process(() => {
  console.log("Running callback");
});
```

---

# Output

```bash
Running callback
```

---

# Callback Functions

A callback function is passed into another function.

---

## Example

```ts
function greetUser(name: string, callback: () => void) {
  console.log(`Hello ${name}`);
  callback();
}

greetUser("Ali", () => {
  console.log("Callback executed");
});
```

---

# Output

```bash
Hello Ali
Callback executed
```

---

# Recursive Functions

Recursive functions call themselves.

---

## Example

```ts
function countdown(num: number): void {
  if (num <= 0) {
    return;
  }

  console.log(num);

  countdown(num - 1);
}

countdown(5);
```

---

# Output

```bash
5
4
3
2
1
```

---

# Function Overloading

Function overloading allows multiple function signatures.

---

## Example

```ts
function combine(a: string, b: string): string;
function combine(a: number, b: number): number;

function combine(a: any, b: any): any {
  return a + b;
}
```

---

# Usage

```ts
console.log(combine(10, 20));
console.log(combine("Hello ", "TypeScript"));
```

---

# Output

```bash
30
Hello TypeScript
```

---

# Generic Functions

Generic functions work with multiple data types.

---

## Example

```ts
function identity<T>(value: T): T {
  return value;
}

console.log(identity<string>("Hello"));
console.log(identity<number>(100));
```

---

# Output

```bash
Hello
100
```

---

# Async Functions

Async functions handle asynchronous operations.

---

## Example

```ts
async function fetchData(): Promise<string> {
  return "Data Loaded";
}
```

---

# Calling Async Function

```ts
fetchData().then((data) => {
  console.log(data);
});
```

---

# Output

```bash
Data Loaded
```

---

# Common Beginner Mistakes

| Mistake | Problem |
|---|---|
| Missing return type | Poor readability |
| Wrong parameter types | Type errors |
| Overusing any | Unsafe code |
| Long functions | Hard maintenance |

---

# Best Practices

- Use proper return types
- Keep functions small
- Use meaningful names
- Prefer arrow functions for callbacks
- Avoid unnecessary global functions
- Use interfaces for complex parameters

---

# Complete Example

```ts
interface Product {
  name: string;
  price: number;
}

function showProduct(product: Product): void {
  console.log(product.name);
  console.log(product.price);
}

showProduct({
  name: "Laptop",
  price: 1000
});
```

---

# Output

```bash
Laptop
1000
```

---

# Conclusion

Functions are one of the most important building blocks in TypeScript.

Understanding functions helps developers create:

- Reusable code
- Scalable applications
- Professional architecture
- Clean and maintainable systems

# 6. Arrays & Tuples in TypeScript

Arrays and tuples are used to store multiple values in a single variable.

TypeScript provides strong typing support for arrays and tuples which improves:

- Data safety
- Readability
- Scalability
- Error prevention

---

# What is an Array?

An array stores multiple values of the same type.

---

# Array Syntax

```ts
let arrayName: type[] = [];
```

---

# String Array

```ts
let users: string[] = ["Ali", "Ahmed", "Usman"];
```

---

# Number Array

```ts
let numbers: number[] = [10, 20, 30];
```

---

# Boolean Array

```ts
let status: boolean[] = [true, false, true];
```

---

# Array Type Inference

TypeScript can automatically detect array types.

---

## Example

```ts
let fruits = ["Apple", "Banana", "Orange"];
```

TypeScript automatically understands this is a string array.

---

# Generic Array Syntax

Arrays can also be written using generic syntax.

---

## Example

```ts
let skills: Array<string> = ["HTML", "CSS", "TypeScript"];
```

---

# Accessing Array Elements

Array indexing starts from `0`.

---

## Example

```ts
let colors: string[] = ["Red", "Blue", "Green"];

console.log(colors[0]);
console.log(colors[1]);
```

---

# Output

```bash
Red
Blue
```

---

# Modifying Array Elements

```ts
let users: string[] = ["Ali", "Ahmed"];

users[1] = "Usman";

console.log(users);
```

---

# Output

```bash
["Ali", "Usman"]
```

---

# Adding Elements to Array

## push()

```ts
let fruits: string[] = ["Apple"];

fruits.push("Banana");

console.log(fruits);
```

---

# Output

```bash
["Apple", "Banana"]
```

---

# Removing Last Element

## pop()

```ts
let numbers: number[] = [1, 2, 3];

numbers.pop();

console.log(numbers);
```

---

# Output

```bash
[1, 2]
```

---

# Add Element at Beginning

## unshift()

```ts
let users: string[] = ["Ahmed"];

users.unshift("Ali");

console.log(users);
```

---

# Output

```bash
["Ali", "Ahmed"]
```

---

# Remove First Element

## shift()

```ts
let users: string[] = ["Ali", "Ahmed"];

users.shift();

console.log(users);
```

---

# Output

```bash
["Ahmed"]
```

---

# Array Length

```ts
let fruits: string[] = ["Apple", "Banana", "Orange"];

console.log(fruits.length);
```

---

# Output

```bash
3
```

---

# Loop Through Arrays

## for Loop

```ts
let numbers: number[] = [10, 20, 30];

for (let i = 0; i < numbers.length; i++) {
  console.log(numbers[i]);
}
```

---

# Output

```bash
10
20
30
```

---

# for...of Loop

```ts
let skills: string[] = ["HTML", "CSS", "TS"];

for (let skill of skills) {
  console.log(skill);
}
```

---

# Output

```bash
HTML
CSS
TS
```

---

# Array Methods

---

# map()

`map()` creates a new array.

---

## Example

```ts
let numbers: number[] = [1, 2, 3];

let doubled = numbers.map(num => num * 2);

console.log(doubled);
```

---

# Output

```bash
[2, 4, 6]
```

---

# filter()

`filter()` returns matching elements.

---

## Example

```ts
let ages: number[] = [10, 18, 25, 15];

let adults = ages.filter(age => age >= 18);

console.log(adults);
```

---

# Output

```bash
[18, 25]
```

---

# find()

`find()` returns the first matching value.

---

## Example

```ts
let users: string[] = ["Ali", "Ahmed", "Usman"];

let result = users.find(user => user === "Ahmed");

console.log(result);
```

---

# Output

```bash
Ahmed
```

---

# includes()

Checks whether a value exists.

---

## Example

```ts
let skills: string[] = ["HTML", "CSS"];

console.log(skills.includes("CSS"));
```

---

# Output

```bash
true
```

---

# Multi-dimensional Arrays

Arrays can contain other arrays.

---

## Example

```ts
let matrix: number[][] = [
  [1, 2],
  [3, 4]
];

console.log(matrix[0][1]);
```

---

# Output

```bash
2
```

---

# Readonly Arrays

Readonly arrays cannot be modified.

---

## Example

```ts
const colors: readonly string[] = ["Red", "Blue"];
```

---

# Invalid Operation

```ts
colors.push("Green");
```

This produces an error.

---

# What is a Tuple?

A tuple stores fixed-length data with predefined types.

---

# Tuple Syntax

```ts
let tupleName: [type1, type2];
```

---

# Basic Tuple Example

```ts
let student: [string, number];

student = ["Ali", 22];
```

---

# Access Tuple Values

```ts
console.log(student[0]);
console.log(student[1]);
```

---

# Output

```bash
Ali
22
```

---

# Invalid Tuple Example

```ts
student = [22, "Ali"];
```

This produces a type error.

---

# Tuple with Multiple Types

```ts
let employee: [number, string, boolean];

employee = [1, "Ahmed", true];
```

---

# Optional Tuple Elements

```ts
let user: [string, number?];

user = ["Ali"];
```

---

# Readonly Tuples

```ts
const point: readonly [number, number] = [10, 20];
```

---

# Array of Objects

```ts
let users: { name: string; age: number }[] = [
  {
    name: "Ali",
    age: 22
  },
  {
    name: "Ahmed",
    age: 25
  }
];
```

---

# Access Object Inside Array

```ts
console.log(users[0].name);
```

---

# Output

```bash
Ali
```

---

# Array Destructuring

```ts
let colors: string[] = ["Red", "Blue", "Green"];

let [first, second] = colors;

console.log(first);
console.log(second);
```

---

# Output

```bash
Red
Blue
```

---

# Tuple Destructuring

```ts
let user: [string, number] = ["Ali", 22];

let [name, age] = user;

console.log(name);
console.log(age);
```

---

# Output

```bash
Ali
22
```

---

# Common Beginner Mistakes

| Mistake | Problem |
|---|---|
| Mixing types in arrays | Type errors |
| Wrong tuple order | Invalid tuples |
| Using any[] everywhere | Unsafe code |
| Modifying readonly arrays | Compilation errors |

---

# Best Practices

- Use typed arrays
- Prefer readonly arrays when needed
- Use tuples for fixed structures
- Avoid unnecessary any[]
- Use meaningful variable names
- Keep array structures clean

---

# Complete Example

```ts
type Product = {
  name: string;
  price: number;
};

let products: Product[] = [
  {
    name: "Laptop",
    price: 1000
  },
  {
    name: "Phone",
    price: 500
  }
];

products.forEach(product => {
  console.log(product.name);
  console.log(product.price);
});
```

---

# Output

```bash
Laptop
1000
Phone
500
```

---

# Conclusion

Arrays and tuples are essential data structures in TypeScript.

Understanding them helps developers:

- Store structured data
- Create scalable applications
- Improve type safety
- Write professional code
- Manage complex datasets efficiently


# 7. Objects & Interfaces in TypeScript

Objects and interfaces are used to structure and organize data in TypeScript applications.

They help developers create:

- Clean architecture
- Reusable structures
- Strongly typed applications
- Scalable systems

---

# What is an Object?

An object stores related data using key-value pairs.

---

# Basic Object Example

```ts
let user = {
  name: "Ali",
  age: 22
};
```

---

# Access Object Properties

```ts
console.log(user.name);
console.log(user.age);
```

---

# Output

```bash
Ali
22
```

---

# Object Type Annotation

TypeScript allows defining object types.

---

## Example

```ts
let student: {
  name: string;
  age: number;
};
```

---

# Assign Object Values

```ts
student = {
  name: "Ahmed",
  age: 25
};
```

---

# Invalid Object Example

```ts
student = {
  name: "Ali",
  age: "Twenty"
};
```

This produces an error because `age` must be a number.

---

# Nested Objects

Objects can contain other objects.

---

## Example

```ts
let employee = {
  name: "Usman",
  address: {
    city: "Lahore",
    country: "Pakistan"
  }
};
```

---

# Access Nested Object

```ts
console.log(employee.address.city);
```

---

# Output

```bash
Lahore
```

---

# Optional Object Properties

Optional properties use `?`.

---

## Example

```ts
let user: {
  name: string;
  age?: number;
};

user = {
  name: "Ali"
};
```

---

# Readonly Properties

Readonly properties cannot be modified.

---

## Example

```ts
let product: {
  readonly id: number;
  name: string;
};

product = {
  id: 1,
  name: "Laptop"
};
```

---

# Invalid Modification

```ts
product.id = 2;
```

This produces an error.

---

# Object Methods

Objects can contain functions.

---

## Example

```ts
let person = {
  name: "Ali",

  greet() {
    console.log(`Hello ${this.name}`);
  }
};

person.greet();
```

---

# Output

```bash
Hello Ali
```

---

# What is an Interface?

An interface defines the structure of an object.

Interfaces help create reusable and scalable code.

---

# Basic Interface Syntax

```ts
interface User {
  name: string;
  age: number;
}
```

---

# Using an Interface

```ts
interface User {
  name: string;
  age: number;
}

let user: User = {
  name: "Ahmed",
  age: 22
};
```

---

# Benefits of Interfaces

Interfaces provide:

- Reusability
- Better readability
- Strong type safety
- Cleaner architecture

---

# Optional Interface Properties

```ts
interface User {
  name: string;
  age?: number;
}
```

---

# Example Usage

```ts
let user: User = {
  name: "Ali"
};
```

---

# Readonly Interface Properties

```ts
interface Product {
  readonly id: number;
  name: string;
}
```

---

# Example

```ts
let laptop: Product = {
  id: 1,
  name: "Dell"
};
```

---

# Interface with Methods

```ts
interface Person {
  name: string;

  greet(): void;
}
```

---

# Implementation Example

```ts
let user: Person = {
  name: "Ali",

  greet() {
    console.log("Welcome");
  }
};
```

---

# Output

```bash
Welcome
```

---

# Extending Interfaces

Interfaces can inherit from other interfaces.

---

## Example

```ts
interface Animal {
  name: string;
}

interface Dog extends Animal {
  breed: string;
}
```

---

# Usage

```ts
let pet: Dog = {
  name: "Tommy",
  breed: "German Shepherd"
};
```

---

# Multiple Interface Inheritance

```ts
interface Person {
  name: string;
}

interface Employee {
  salary: number;
}

interface Manager extends Person, Employee {
  department: string;
}
```

---

# Example

```ts
let manager: Manager = {
  name: "Ali",
  salary: 50000,
  department: "IT"
};
```

---

# Interfaces with Arrays

```ts
interface User {
  name: string;
  age: number;
}

let users: User[] = [
  {
    name: "Ali",
    age: 22
  },
  {
    name: "Ahmed",
    age: 25
  }
];
```

---

# Interfaces with Functions

```ts
interface MathOperation {
  (a: number, b: number): number;
}
```

---

# Example

```ts
const add: MathOperation = (a, b) => a + b;

console.log(add(10, 5));
```

---

# Output

```bash
15
```

---

# Interface vs Type Alias

| Interface | Type Alias |
|---|---|
| Best for objects | More flexible |
| Extendable | Supports unions |
| Cleaner for OOP | Better for advanced types |

---

# Interface with Class

Interfaces can be implemented in classes.

---

## Example

```ts
interface User {
  name: string;

  greet(): void;
}

class Person implements User {
  name: string;

  constructor(name: string) {
    this.name = name;
  }

  greet(): void {
    console.log(`Hello ${this.name}`);
  }
}
```

---

# Usage

```ts
const user = new Person("Ali");

user.greet();
```

---

# Output

```bash
Hello Ali
```

---

# Dynamic Object Keys

```ts
interface Scores {
  [key: string]: number;
}
```

---

# Example

```ts
let marks: Scores = {
  math: 90,
  english: 85
};
```

---

# Destructuring Objects

```ts
let user = {
  name: "Ali",
  age: 22
};

let { name, age } = user;

console.log(name);
console.log(age);
```

---

# Output

```bash
Ali
22
```

---

# Common Beginner Mistakes

| Mistake | Problem |
|---|---|
| Missing required properties | Type errors |
| Wrong property types | Invalid objects |
| Using any objects | Unsafe code |
| Ignoring interfaces | Poor scalability |

---

# Best Practices

- Use interfaces for object structures
- Use readonly when needed
- Keep interfaces reusable
- Use meaningful property names
- Avoid overly large interfaces
- Organize interfaces properly

---

# Real-world Example

```ts
interface Product {
  id: number;
  name: string;
  price: number;
  inStock: boolean;
}

const laptop: Product = {
  id: 1,
  name: "Dell XPS",
  price: 1200,
  inStock: true
};

console.log(laptop);
```

---

# Output

```bash
{
  id: 1,
  name: 'Dell XPS',
  price: 1200,
  inStock: true
}
```

---

# Conclusion

Objects and interfaces are fundamental parts of TypeScript development.

They help developers create:

- Structured applications
- Reusable architectures
- Type-safe systems
- Professional codebases
- Scalable software solutions

# 8. Type Aliases & Advanced Types in TypeScript

Type aliases and advanced types help developers create flexible, reusable, and scalable type structures.

They improve:

- Code readability
- Reusability
- Type safety
- Application scalability

---

# What is a Type Alias?

A type alias creates a custom name for a type.

---

# Basic Syntax

```ts
type TypeName = type;
```

---

# Simple Type Alias

```ts
type UserName = string;

let name: UserName = "Ali";
```

---

# Number Alias

```ts
type Age = number;

let userAge: Age = 22;
```

---

# Object Type Alias

```ts
type User = {
  name: string;
  age: number;
};
```

---

# Usage

```ts
let user: User = {
  name: "Ahmed",
  age: 25
};
```

---

# Benefits of Type Aliases

Type aliases help developers:

- Reduce repeated code
- Improve readability
- Create reusable structures
- Manage complex types

---

# Union Types

Union types allow multiple possible types.

---

# Syntax

```ts
type TypeName = type1 | type2;
```

---

# Example

```ts
type ID = string | number;

let userId: ID;

userId = 100;
userId = "TS100";
```

---

# Union Type with Functions

```ts
function printId(id: string | number) {
  console.log(id);
}
```

---

# Example Usage

```ts
printId(100);
printId("TS200");
```

---

# Output

```bash
100
TS200
```

---

# Type Narrowing

Type narrowing checks the actual type before use.

---

## Example

```ts
function process(value: string | number) {
  if (typeof value === "string") {
    console.log(value.toUpperCase());
  } else {
    console.log(value.toFixed(2));
  }
}
```

---

# Output

```bash
HELLO
10.00
```

---

# Intersection Types

Intersection types combine multiple types.

---

# Syntax

```ts
type NewType = Type1 & Type2;
```

---

# Example

```ts
type Person = {
  name: string;
};

type Employee = {
  salary: number;
};

type Manager = Person & Employee;
```

---

# Usage

```ts
let manager: Manager = {
  name: "Ali",
  salary: 50000
};
```

---

# Literal Types

Literal types restrict exact values.

---

# Example

```ts
type Direction = "left" | "right";

let move: Direction;

move = "left";
```

---

# Invalid Example

```ts
move = "up";
```

This produces an error.

---

# String Literal Types

```ts
type Role = "admin" | "user" | "guest";

let currentRole: Role = "admin";
```

---

# Number Literal Types

```ts
type Dice = 1 | 2 | 3 | 4 | 5 | 6;

let value: Dice = 4;
```

---

# Boolean Literal Types

```ts
type Status = true | false;
```

---

# Type Aliases with Arrays

```ts
type Users = string[];

let students: Users = ["Ali", "Ahmed"];
```

---

# Type Aliases with Functions

```ts
type AddFunction = (
  a: number,
  b: number
) => number;
```

---

# Example

```ts
const add: AddFunction = (a, b) => a + b;
```

---

# Nullable Types

Nullable types allow `null`.

---

# Example

```ts
type User = string | null;

let username: User = null;
```

---

# Optional Types

```ts
type User = {
  name: string;
  age?: number;
};
```

---

# Readonly Types

Readonly prevents modification.

---

# Example

```ts
type Product = {
  readonly id: number;
  name: string;
};
```

---

# Example Usage

```ts
let laptop: Product = {
  id: 1,
  name: "Dell"
};
```

---

# Invalid Modification

```ts
laptop.id = 2;
```

This produces an error.

---

# Function Return Union Types

```ts
function format(value: string | number): string {
  return String(value);
}
```

---

# Complex Type Alias

```ts
type Product = {
  id: number;
  name: string;
  price: number;
  inStock: boolean;
};
```

---

# Example

```ts
const phone: Product = {
  id: 1,
  name: "iPhone",
  price: 1200,
  inStock: true
};
```

---

# Nested Type Aliases

```ts
type Address = {
  city: string;
  country: string;
};

type User = {
  name: string;
  address: Address;
};
```

---

# Example

```ts
const user: User = {
  name: "Ali",
  address: {
    city: "Lahore",
    country: "Pakistan"
  }
};
```

---

# Type Assertions

Type assertions tell TypeScript the exact type.

---

# Example

```ts
let value: unknown = "Hello";

let length: number = (value as string).length;
```

---

# Output

```bash
5
```

---

# Discriminated Unions

Discriminated unions are useful for handling multiple object types.

---

# Example

```ts
type Circle = {
  type: "circle";
  radius: number;
};

type Square = {
  type: "square";
  side: number;
};

type Shape = Circle | Square;
```

---

# Usage

```ts
function area(shape: Shape) {
  if (shape.type === "circle") {
    return 3.14 * shape.radius ** 2;
  }

  return shape.side * shape.side;
}
```

---

# Utility Types

TypeScript provides built-in utility types.

---

# Partial

Makes all properties optional.

```ts
type User = {
  name: string;
  age: number;
};

type PartialUser = Partial<User>;
```

---

# Required

Makes all properties required.

```ts
type RequiredUser = Required<User>;
```

---

# Readonly

Makes properties readonly.

```ts
type ReadonlyUser = Readonly<User>;
```

---

# Pick

Selects specific properties.

```ts
type User = {
  name: string;
  age: number;
  email: string;
};

type UserPreview = Pick<User, "name" | "email">;
```

---

# Omit

Removes specific properties.

```ts
type UserWithoutEmail = Omit<User, "email">;
```

---

# Record

Creates object types dynamically.

```ts
type Users = Record<string, number>;
```

---

# Example

```ts
const scores: Users = {
  Ali: 90,
  Ahmed: 85
};
```

---

# Common Beginner Mistakes

| Mistake | Problem |
|---|---|
| Overusing any | Unsafe code |
| Complex unions everywhere | Hard readability |
| Ignoring type narrowing | Runtime issues |
| Wrong literal values | Type errors |

---

# Best Practices

- Use reusable type aliases
- Prefer union types over any
- Keep types readable
- Use utility types properly
- Use readonly where needed
- Organize types in separate files

---

# Real-world Example

```ts
type UserRole = "admin" | "editor" | "user";

type User = {
  id: number;
  name: string;
  role: UserRole;
};

const currentUser: User = {
  id: 1,
  name: "Ali",
  role: "admin"
};

console.log(currentUser);
```

---

# Output

```bash
{
  id: 1,
  name: 'Ali',
  role: 'admin'
}
```

---

# Conclusion

Type aliases and advanced types are powerful TypeScript features that help developers build:

- Flexible applications
- Reusable architectures
- Strongly typed systems
- Professional codebases
- Scalable enterprise applications

# 9. Enums in TypeScript

Enums are used to store a collection of related constant values.

Enums make code:

- More readable
- Easier to manage
- More maintainable
- Better structured

---

# What is an Enum?

Enum stands for "Enumeration".

It allows developers to define a set of named constants.

---

# Why Use Enums?

Enums help developers:

- Avoid hardcoded values
- Improve readability
- Create meaningful constants
- Reduce coding mistakes

---

# Basic Enum Syntax

```ts
enum EnumName {
  VALUE1,
  VALUE2,
  VALUE3
}
```

---

# Numeric Enum

By default, enums use numeric values starting from `0`.

---

# Example

```ts
enum Role {
  Admin,
  User,
  Guest
}
```

---

# Access Enum Values

```ts
console.log(Role.Admin);
console.log(Role.User);
console.log(Role.Guest);
```

---

# Output

```bash
0
1
2
```

---

# Access Enum Names

```ts
console.log(Role[0]);
console.log(Role[1]);
```

---

# Output

```bash
Admin
User
```

---

# Assign Enum Value to Variable

```ts
enum Status {
  Active,
  Inactive
}

let currentStatus: Status = Status.Active;

console.log(currentStatus);
```

---

# Output

```bash
0
```

---

# Custom Numeric Enum Values

Enum values can be customized.

---

# Example

```ts
enum Direction {
  Up = 1,
  Down = 2,
  Left = 3,
  Right = 4
}
```

---

# Output Example

```ts
console.log(Direction.Left);
```

```bash
3
```

---

# Auto Increment Behavior

After defining the first value, TypeScript auto-increments the rest.

---

# Example

```ts
enum Level {
  Low = 1,
  Medium,
  High
}
```

---

# Values

```bash
Low = 1
Medium = 2
High = 3
```

---

# String Enums

String enums store string values.

---

# Example

```ts
enum UserRole {
  Admin = "ADMIN",
  User = "USER",
  Guest = "GUEST"
}
```

---

# Usage

```ts
console.log(UserRole.Admin);
```

---

# Output

```bash
ADMIN
```

---

# Why String Enums are Useful

String enums are easier to debug because values are readable.

---

# Mixed Enums

Enums can contain both numbers and strings.

---

# Example

```ts
enum Result {
  Success = "SUCCESS",
  Failed = 0
}
```

---

# Const Enums

`const enum` improves performance because TypeScript removes extra generated code.

---

# Example

```ts
const enum Color {
  Red,
  Blue,
  Green
}

let selected = Color.Blue;
```

---

# Benefits of const enum

- Faster performance
- Smaller compiled code
- Better optimization

---

# Enum with Functions

Enums can be used inside functions.

---

# Example

```ts
enum PaymentStatus {
  Pending,
  Completed,
  Failed
}

function checkStatus(status: PaymentStatus) {
  console.log(status);
}

checkStatus(PaymentStatus.Completed);
```

---

# Output

```bash
1
```

---

# Enums with Conditions

```ts
enum Role {
  Admin,
  User
}

let currentRole: Role = Role.Admin;

if (currentRole === Role.Admin) {
  console.log("Access Granted");
}
```

---

# Output

```bash
Access Granted
```

---

# Enum in Objects

```ts
enum OrderStatus {
  Pending,
  Delivered
}

type Order = {
  id: number;
  status: OrderStatus;
};
```

---

# Example

```ts
const order: Order = {
  id: 1,
  status: OrderStatus.Pending
};
```

---

# Enum in Arrays

```ts
enum Category {
  Electronics,
  Clothing,
  Food
}

let categories: Category[] = [
  Category.Electronics,
  Category.Food
];
```

---

# Reverse Mapping

Numeric enums support reverse mapping.

---

# Example

```ts
enum Status {
  Active,
  Inactive
}

console.log(Status[0]);
```

---

# Output

```bash
Active
```

---

# Enum vs Object

| Enum | Object |
|---|---|
| Built for constants | General-purpose |
| Better readability | More flexible |
| Type-safe | Less strict |

---

# Real-world Enum Example

```ts
enum AccountType {
  Saving = "SAVING",
  Current = "CURRENT"
}

type BankAccount = {
  id: number;
  type: AccountType;
};
```

---

# Usage

```ts
const account: BankAccount = {
  id: 1,
  type: AccountType.Saving
};

console.log(account);
```

---

# Output

```bash
{
  id: 1,
  type: 'SAVING'
}
```

---

# Enum with Switch Statement

```ts
enum TrafficLight {
  Red,
  Yellow,
  Green
}

function action(light: TrafficLight) {
  switch (light) {
    case TrafficLight.Red:
      console.log("Stop");
      break;

    case TrafficLight.Yellow:
      console.log("Ready");
      break;

    case TrafficLight.Green:
      console.log("Go");
      break;
  }
}
```

---

# Usage

```ts
action(TrafficLight.Green);
```

---

# Output

```bash
Go
```

---

# Common Beginner Mistakes

| Mistake | Problem |
|---|---|
| Using enums for simple values | Unnecessary complexity |
| Mixing unrelated values | Poor readability |
| Overusing numeric enums | Hard debugging |
| Ignoring string enums | Less readable code |

---

# Best Practices

- Prefer string enums in large projects
- Use meaningful enum names
- Group related constants together
- Use const enums for optimization
- Avoid unnecessary enums

---

# Enum Naming Conventions

## Good Example

```ts
enum UserRole {}
enum PaymentStatus {}
```

---

## Bad Example

```ts
enum data {}
enum test {}
```

---

# Complete Example

```ts
enum UserRole {
  Admin = "ADMIN",
  Editor = "EDITOR",
  User = "USER"
}

type User = {
  name: string;
  role: UserRole;
};

const currentUser: User = {
  name: "Ali",
  role: UserRole.Admin
};

console.log(currentUser);
```

---

# Output

```bash
{
  name: 'Ali',
  role: 'ADMIN'
}
```

---

# Advantages of Enums

- Better readability
- Cleaner code
- Easier maintenance
- Strong type safety
- Reduced hardcoded values

---

# Limitations of Enums

- Extra generated JavaScript code
- Can increase complexity if overused
- Numeric enums can be confusing

---

# Conclusion

Enums are powerful tools for managing constant values in TypeScript applications.

They help developers create:

- Professional codebases
- Readable applications
- Maintainable systems
- Scalable architectures
- Cleaner business logic

# 10. Classes & OOP in TypeScript

TypeScript fully supports Object-Oriented Programming (OOP).

OOP helps developers build:

- Scalable applications
- Reusable code
- Maintainable systems
- Professional architectures

---

# What is Object-Oriented Programming?

Object-Oriented Programming is a programming style based on objects and classes.

OOP focuses on:

- Reusability
- Modularity
- Encapsulation
- Abstraction
- Inheritance

---

# Main OOP Concepts

| Concept | Purpose |
|---|---|
| Class | Blueprint for objects |
| Object | Instance of a class |
| Encapsulation | Protect data |
| Inheritance | Reuse code |
| Polymorphism | Multiple behaviors |
| Abstraction | Hide implementation details |

---

# What is a Class?

A class is a blueprint used to create objects.

---

# Basic Class Syntax

```ts
class ClassName {
  // properties
  // methods
}
```

---

# Create First Class

```ts
class User {
  name: string = "Ali";
}
```

---

# Create Object

```ts
const user = new User();

console.log(user.name);
```

---

# Output

```bash
Ali
```

---

# Class Properties

Properties store object data.

---

# Example

```ts
class Product {
  name: string = "Laptop";
  price: number = 1000;
}
```

---

# Access Properties

```ts
const item = new Product();

console.log(item.name);
console.log(item.price);
```

---

# Output

```bash
Laptop
1000
```

---

# Constructors

Constructors initialize object values.

---

# Constructor Syntax

```ts
constructor() {
  // initialization
}
```

---

# Example

```ts
class User {
  name: string;

  constructor(name: string) {
    this.name = name;
  }
}
```

---

# Create Object

```ts
const user = new User("Ahmed");

console.log(user.name);
```

---

# Output

```bash
Ahmed
```

---

# this Keyword

`this` refers to the current object instance.

---

# Example

```ts
class Student {
  name: string;

  constructor(name: string) {
    this.name = name;
  }

  greet() {
    console.log(`Hello ${this.name}`);
  }
}
```

---

# Usage

```ts
const student = new Student("Ali");

student.greet();
```

---

# Output

```bash
Hello Ali
```

---

# Methods in Classes

Methods define object behavior.

---

# Example

```ts
class Calculator {
  add(a: number, b: number): number {
    return a + b;
  }
}
```

---

# Usage

```ts
const calc = new Calculator();

console.log(calc.add(10, 5));
```

---

# Output

```bash
15
```

---

# Access Modifiers

Access modifiers control property visibility.

---

# Types of Access Modifiers

| Modifier | Access Level |
|---|---|
| public | Accessible everywhere |
| private | Accessible only inside class |
| protected | Accessible inside class and subclasses |

---

# Public Modifier

`public` is the default modifier.

---

# Example

```ts
class User {
  public name: string;

  constructor(name: string) {
    this.name = name;
  }
}
```

---

# Private Modifier

Private properties cannot be accessed outside the class.

---

# Example

```ts
class Account {
  private balance: number = 1000;
}
```

---

# Invalid Access

```ts
const account = new Account();

console.log(account.balance);
```

This produces an error.

---

# Protected Modifier

Protected members are accessible in subclasses.

---

# Example

```ts
class Animal {
  protected name: string;

  constructor(name: string) {
    this.name = name;
  }
}
```

---

# Parameter Properties

TypeScript provides shorthand constructor syntax.

---

# Example

```ts
class User {
  constructor(
    public name: string,
    public age: number
  ) {}
}
```

---

# Usage

```ts
const user = new User("Ali", 22);

console.log(user.name);
```

---

# Output

```bash
Ali
```

---

# Readonly Properties

Readonly properties cannot be modified after initialization.

---

# Example

```ts
class Product {
  readonly id: number;

  constructor(id: number) {
    this.id = id;
  }
}
```

---

# Invalid Modification

```ts
product.id = 2;
```

This produces an error.

---

# Inheritance

Inheritance allows one class to reuse another class.

---

# Basic Syntax

```ts
class Child extends Parent {}
```

---

# Example

```ts
class Animal {
  move() {
    console.log("Moving");
  }
}

class Dog extends Animal {
  bark() {
    console.log("Barking");
  }
}
```

---

# Usage

```ts
const dog = new Dog();

dog.move();
dog.bark();
```

---

# Output

```bash
Moving
Barking
```

---

# Method Overriding

Subclass methods can override parent methods.

---

# Example

```ts
class Animal {
  sound() {
    console.log("Animal Sound");
  }
}

class Cat extends Animal {
  sound() {
    console.log("Meow");
  }
}
```

---

# Usage

```ts
const cat = new Cat();

cat.sound();
```

---

# Output

```bash
Meow
```

---

# super Keyword

`super` calls parent class methods or constructors.

---

# Example

```ts
class Person {
  constructor(public name: string) {}
}

class Employee extends Person {
  constructor(
    name: string,
    public salary: number
  ) {
    super(name);
  }
}
```

---

# Abstract Classes

Abstract classes cannot be instantiated directly.

---

# Example

```ts
abstract class Shape {
  abstract area(): number;
}
```

---

# Implement Abstract Class

```ts
class Circle extends Shape {
  area(): number {
    return 3.14 * 5 * 5;
  }
}
```

---

# Interfaces with Classes

Classes can implement interfaces.

---

# Example

```ts
interface User {
  name: string;

  greet(): void;
}

class Person implements User {
  constructor(public name: string) {}

  greet(): void {
    console.log(`Hello ${this.name}`);
  }
}
```

---

# Static Properties & Methods

Static members belong to the class itself.

---

# Example

```ts
class MathUtils {
  static PI: number = 3.14;

  static square(num: number): number {
    return num * num;
  }
}
```

---

# Usage

```ts
console.log(MathUtils.PI);
console.log(MathUtils.square(5));
```

---

# Output

```bash
3.14
25
```

---

# Getters & Setters

Getters and setters control property access.

---

# Example

```ts
class User {
  private _name: string = "";

  get name(): string {
    return this._name;
  }

  set name(value: string) {
    this._name = value;
  }
}
```

---

# Usage

```ts
const user = new User();

user.name = "Ali";

console.log(user.name);
```

---

# Output

```bash
Ali
```

---

# Object Destructuring

```ts
class Product {
  constructor(
    public name: string,
    public price: number
  ) {}
}

const laptop = new Product("Dell", 1200);

const { name, price } = laptop;

console.log(name);
console.log(price);
```

---

# Output

```bash
Dell
1200
```

---

# Common Beginner Mistakes

| Mistake | Problem |
|---|---|
| Not using constructors properly | Initialization issues |
| Overusing public properties | Weak encapsulation |
| Ignoring interfaces | Poor scalability |
| Large classes | Hard maintenance |

---

# Best Practices

- Keep classes focused
- Use interfaces where needed
- Prefer private properties
- Use readonly when possible
- Avoid massive classes
- Follow SOLID principles

---

# Real-world Example

```ts
class BankAccount {
  constructor(
    public accountHolder: string,
    private balance: number
  ) {}

  deposit(amount: number): void {
    this.balance += amount;
  }

  getBalance(): number {
    return this.balance;
  }
}

const account = new BankAccount(
  "Ali",
  1000
);

account.deposit(500);

console.log(account.getBalance());
```

---

# Output

```bash
1500
```

---

# Advantages of OOP

- Better code organization
- Reusability
- Scalability
- Maintainability
- Professional architecture

---

# Conclusion

Classes and OOP are essential for professional TypeScript development.

Understanding OOP helps developers build:

- Enterprise applications
- Scalable systems
- Reusable architectures
- Maintainable codebases
- Professional software solutions

# 11. Generics in TypeScript

Generics allow developers to create reusable and flexible components that work with multiple data types while maintaining type safety.

Generics are one of the most powerful features in TypeScript.

---

# Why Generics are Important

Generics help developers:

- Avoid code duplication
- Create reusable logic
- Maintain type safety
- Build scalable applications
- Write flexible code

---

# Problem Without Generics

Without generics, developers often repeat the same code for different data types.

---

# Example Without Generics

```ts
function stringValue(value: string): string {
  return value;
}

function numberValue(value: number): number {
  return value;
}
```

This creates duplicate logic.

---

# What is a Generic?

A generic allows a function, class, or interface to work with multiple types dynamically.

---

# Generic Syntax

```ts
function functionName<T>(value: T): T {
  return value;
}
```

`T` represents a generic type.

---

# First Generic Function

```ts
function identity<T>(value: T): T {
  return value;
}
```

---

# Usage

```ts
console.log(identity<string>("Hello"));
console.log(identity<number>(100));
```

---

# Output

```bash
Hello
100
```

---

# How Generics Work

TypeScript replaces `T` with the actual provided type.

---

# Generic with Type Inference

TypeScript can automatically detect generic types.

---

# Example

```ts
console.log(identity("TypeScript"));
console.log(identity(500));
```

---

# Generic Arrays

Generics work with arrays.

---

# Example

```ts
function getFirst<T>(items: T[]): T {
  return items[0];
}
```

---

# Usage

```ts
console.log(getFirst<number>([1, 2, 3]));
console.log(getFirst<string>(["Ali", "Ahmed"]));
```

---

# Output

```bash
1
Ali
```

---

# Multiple Generic Types

Generics can use multiple type parameters.

---

# Example

```ts
function combine<T, U>(
  first: T,
  second: U
) {
  return {
    first,
    second
  };
}
```

---

# Usage

```ts
console.log(combine<string, number>("Age", 22));
```

---

# Output

```bash
{
  first: 'Age',
  second: 22
}
```

---

# Generic Interfaces

Interfaces can use generics.

---

# Example

```ts
interface ApiResponse<T> {
  success: boolean;
  data: T;
}
```

---

# Usage

```ts
const response: ApiResponse<string> = {
  success: true,
  data: "Data Loaded"
};
```

---

# Generic Interface with Object

```ts
interface User {
  name: string;
  age: number;
}

const userResponse: ApiResponse<User> = {
  success: true,
  data: {
    name: "Ali",
    age: 22
  }
};
```

---

# Generic Classes

Classes can also use generics.

---

# Example

```ts
class Box<T> {
  content: T;

  constructor(content: T) {
    this.content = content;
  }
}
```

---

# Usage

```ts
const stringBox = new Box<string>("Hello");

console.log(stringBox.content);
```

---

# Output

```bash
Hello
```

---

# Generic Constraints

Constraints limit what types can be used.

---

# Example

```ts
function printLength<T extends { length: number }>(
  item: T
): void {
  console.log(item.length);
}
```

---

# Usage

```ts
printLength("Hello");
printLength([1, 2, 3]);
```

---

# Output

```bash
5
3
```

---

# Invalid Generic Usage

```ts
printLength(100);
```

This produces an error because numbers do not have `length`.

---

# Generic with keyof

`keyof` works with object keys.

---

# Example

```ts
function getValue<T, K extends keyof T>(
  obj: T,
  key: K
) {
  return obj[key];
}
```

---

# Usage

```ts
const user = {
  name: "Ali",
  age: 22
};

console.log(getValue(user, "name"));
```

---

# Output

```bash
Ali
```

---

# Generic Type Aliases

Type aliases can use generics.

---

# Example

```ts
type ApiResult<T> = {
  success: boolean;
  data: T;
};
```

---

# Usage

```ts
const result: ApiResult<number> = {
  success: true,
  data: 100
};
```

---

# Generic Default Types

Generics can have default types.

---

# Example

```ts
interface User<T = string> {
  value: T;
}
```

---

# Usage

```ts
const user: User = {
  value: "Ali"
};
```

---

# Generic Utility Function

```ts
function createArray<T>(
  value: T,
  count: number
): T[] {
  return Array(count).fill(value);
}
```

---

# Usage

```ts
console.log(createArray<string>("TS", 3));
```

---

# Output

```bash
["TS", "TS", "TS"]
```

---

# Generic Promise

Promises can use generics.

---

# Example

```ts
function fetchData(): Promise<string> {
  return Promise.resolve("Data Loaded");
}
```

---

# Usage

```ts
fetchData().then(data => {
  console.log(data);
});
```

---

# Output

```bash
Data Loaded
```

---

# Generic Repository Pattern

Generics are widely used in professional applications.

---

# Example

```ts
class Repository<T> {
  private items: T[] = [];

  add(item: T): void {
    this.items.push(item);
  }

  getAll(): T[] {
    return this.items;
  }
}
```

---

# Usage

```ts
const users = new Repository<string>();

users.add("Ali");
users.add("Ahmed");

console.log(users.getAll());
```

---

# Output

```bash
["Ali", "Ahmed"]
```

---

# Generic with Interfaces & Classes

```ts
interface Product {
  name: string;
  price: number;
}

class Store<T> {
  items: T[] = [];

  addItem(item: T) {
    this.items.push(item);
  }
}
```

---

# Usage

```ts
const productStore = new Store<Product>();

productStore.addItem({
  name: "Laptop",
  price: 1200
});
```

---

# Built-in Generic Types

TypeScript provides many built-in generic types.

---

# Array

```ts
let numbers: Array<number> = [1, 2, 3];
```

---

# Promise

```ts
let promise: Promise<string>;
```

---

# Map

```ts
let users = new Map<number, string>();
```

---

# Set

```ts
let ids = new Set<number>();
```

---

# Common Beginner Mistakes

| Mistake | Problem |
|---|---|
| Overcomplicated generics | Hard readability |
| Using any instead of generics | Unsafe code |
| Missing constraints | Invalid operations |
| Too many generic parameters | Complex architecture |

---

# Best Practices

- Use meaningful generic names
- Prefer reusable generic components
- Use constraints when needed
- Avoid unnecessary complexity
- Keep generics readable

---

# Generic Naming Conventions

| Generic | Meaning |
|---|---|
| T | Type |
| K | Key |
| V | Value |
| U | Secondary Type |

---

# Real-world Example

```ts
interface ApiResponse<T> {
  status: number;
  data: T;
}

interface User {
  id: number;
  name: string;
}

const response: ApiResponse<User> = {
  status: 200,
  data: {
    id: 1,
    name: "Ali"
  }
};

console.log(response);
```

---

# Output

```bash
{
  status: 200,
  data: {
    id: 1,
    name: 'Ali'
  }
}
```

---

# Advantages of Generics

- Reusable code
- Strong type safety
- Better scalability
- Cleaner architecture
- Flexible development

---

# Conclusion

Generics are one of the most powerful features in TypeScript.

They help developers build:

- Reusable components
- Professional applications
- Scalable systems
- Flexible architectures
- Type-safe solutions

# 12. Modules & File Structure in TypeScript

Modules help developers organize code into separate reusable files.

A proper file structure improves:

- Scalability
- Maintainability
- Readability
- Team collaboration
- Professional architecture

---

# What is a Module?

A module is a file containing reusable code.

Each TypeScript file becomes a module when it uses:

- `export`
- `import`

---

# Why Use Modules?

Modules help developers:

- Split large applications
- Reuse code
- Avoid duplicate logic
- Organize files professionally
- Improve scalability

---

# Basic Module Structure

```bash
project/
│
├── src/
│   ├── app.ts
│   ├── user.ts
│   └── product.ts
│
├── dist/
├── package.json
├── tsconfig.json
└── README.md
```

---

# Exporting Code

`export` allows code to be used in other files.

---

# Named Export

## user.ts

```ts
export const username: string = "Ali";
```

---

# Importing Named Export

## app.ts

```ts
import { username } from "./user";

console.log(username);
```

---

# Output

```bash
Ali
```

---

# Export Multiple Values

## math.ts

```ts
export const add = (
  a: number,
  b: number
): number => a + b;

export const subtract = (
  a: number,
  b: number
): number => a - b;
```

---

# Import Multiple Values

## app.ts

```ts
import { add, subtract } from "./math";

console.log(add(10, 5));
console.log(subtract(20, 5));
```

---

# Output

```bash
15
15
```

---

# Default Export

A file can contain one default export.

---

# Example

## user.ts

```ts
export default class User {
  constructor(
    public name: string
  ) {}
}
```

---

# Import Default Export

## app.ts

```ts
import User from "./user";

const user = new User("Ahmed");

console.log(user.name);
```

---

# Output

```bash
Ahmed
```

---

# Difference Between Named & Default Export

| Named Export | Default Export |
|---|---|
| Multiple allowed | Only one allowed |
| Imported with braces | Imported without braces |
| Better for utilities | Better for main modules |

---

# Export All

`export *` re-exports everything.

---

# Example

## utils/index.ts

```ts
export * from "./math";
export * from "./string";
```

---

# Import All

```ts
import * as MathUtils from "./math";

console.log(MathUtils.add(5, 5));
```

---

# Output

```bash
10
```

---

# Aliasing Imports

Imports can be renamed.

---

# Example

```ts
import { add as sum } from "./math";

console.log(sum(10, 5));
```

---

# Output

```bash
15
```

---

# Organizing Project Structure

Professional applications separate code into folders.

---

# Recommended Structure

```bash
src/
│
├── components/
├── services/
├── controllers/
├── models/
├── interfaces/
├── utils/
├── config/
├── types/
└── app.ts
```

---

# Folder Explanation

| Folder | Purpose |
|---|---|
| components | Reusable UI components |
| services | Business logic |
| controllers | Request handling |
| models | Data structures |
| interfaces | TypeScript interfaces |
| utils | Helper functions |
| config | Configuration files |
| types | Shared custom types |

---

# Example Utility Module

## utils/string.ts

```ts
export function capitalize(
  value: string
): string {
  return value.toUpperCase();
}
```

---

# Usage

## app.ts

```ts
import { capitalize } from "./utils/string";

console.log(capitalize("typescript"));
```

---

# Output

```bash
TYPESCRIPT
```

---

# Path Aliases

Path aliases simplify imports.

---

# Without Path Alias

```ts
import { User } from "../../../../models/user";
```

---

# With Path Alias

```ts
import { User } from "@models/user";
```

---

# Configure Path Aliases

## tsconfig.json

```json
{
  "compilerOptions": {
    "baseUrl": "./src",
    "paths": {
      "@models/*": ["models/*"],
      "@utils/*": ["utils/*"]
    }
  }
}
```

---

# Index Files

Index files simplify exports.

---

# Example

## services/index.ts

```ts
export * from "./authService";
export * from "./userService";
```

---

# Usage

```ts
import { login } from "./services";
```

---

# Module Resolution

TypeScript automatically resolves imported modules.

---

# Common Module Types

| Module Type | Description |
|---|---|
| CommonJS | Node.js default |
| ES Modules | Modern JavaScript modules |

---

# CommonJS Example

```ts
module.exports = {};
```

---

# ES Module Example

```ts
export {};
```

---

# Configure Module System

## tsconfig.json

```json
{
  "compilerOptions": {
    "module": "commonjs"
  }
}
```

---

# Dynamic Imports

Dynamic imports load modules when needed.

---

# Example

```ts
async function loadModule() {
  const math = await import("./math");

  console.log(math.add(5, 5));
}
```

---

# Output

```bash
10
```

---

# Namespace vs Modules

| Namespace | Modules |
|---|---|
| Older approach | Modern approach |
| Global scope | File-based scope |
| Less scalable | Highly scalable |

---

# Barrel Exports

Barrel exports combine multiple exports.

---

# Example

## index.ts

```ts
export * from "./user";
export * from "./product";
export * from "./order";
```

---

# Benefits of Barrel Exports

- Cleaner imports
- Better organization
- Easier scalability

---

# Real-world Example

## interfaces/User.ts

```ts
export interface User {
  id: number;
  name: string;
}
```

---

## services/userService.ts

```ts
import { User } from "../interfaces/User";

export function getUser(): User {
  return {
    id: 1,
    name: "Ali"
  };
}
```

---

## app.ts

```ts
import { getUser } from "./services/userService";

console.log(getUser());
```

---

# Output

```bash
{
  id: 1,
  name: 'Ali'
}
```

---

# Common Beginner Mistakes

| Mistake | Problem |
|---|---|
| Large single files | Poor scalability |
| Circular imports | Runtime issues |
| Poor folder naming | Confusing structure |
| Deep nested imports | Hard maintenance |

---

# Best Practices

- Use small reusable modules
- Separate business logic
- Use index files wisely
- Organize folders properly
- Avoid circular dependencies
- Use path aliases in large projects

---

# Professional Architecture Example

```bash
src/
│
├── api/
├── controllers/
├── database/
├── middleware/
├── models/
├── routes/
├── services/
├── types/
├── utils/
└── app.ts
```

---

# Advantages of Modules

- Reusable code
- Better maintainability
- Scalable architecture
- Cleaner structure
- Team-friendly development

---

# Conclusion

Modules and proper file structure are essential for professional TypeScript development.

They help developers create:

- Organized applications
- Scalable architectures
- Maintainable systems
- Reusable components
- Enterprise-level projects

# 13. Error Handling & Debugging in TypeScript

Error handling and debugging are essential for building stable and professional TypeScript applications.

They help developers:

- Prevent application crashes
- Detect bugs quickly
- Improve code quality
- Build reliable systems
- Handle unexpected situations safely

---

# What is Error Handling?

Error handling is the process of managing runtime problems in an application.

Examples:

- Invalid input
- API failures
- Database errors
- File errors
- Authentication issues

---

# Why Error Handling is Important

Without proper error handling:

- Applications may crash
- Data may become corrupted
- User experience becomes poor
- Debugging becomes difficult

---

# Types of Errors in TypeScript

| Error Type | Description |
|---|---|
| Syntax Error | Invalid code syntax |
| Type Error | Wrong data type |
| Runtime Error | Error during execution |
| Logical Error | Wrong program logic |

---

# Syntax Error Example

```ts
let name: string = ;
```

This produces a syntax error.

---

# Type Error Example

```ts
let age: number = "Twenty";
```

TypeScript catches this during compilation.

---

# Runtime Error Example

```ts
const user = undefined;

console.log(user.name);
```

This crashes during runtime.

---

# What is Debugging?

Debugging is the process of finding and fixing errors in code.

---

# Common Debugging Methods

- Console logging
- VS Code debugger
- Breakpoints
- Error messages
- Source maps

---

# Console Logging

`console.log()` helps inspect values.

---

# Example

```ts
let username: string = "Ali";

console.log(username);
```

---

# Output

```bash
Ali
```

---

# Debug Multiple Values

```ts
let name: string = "Ahmed";
let age: number = 22;

console.log(name, age);
```

---

# Output

```bash
Ahmed 22
```

---

# try...catch Statement

`try...catch` handles runtime errors safely.

---

# Basic Syntax

```ts
try {
  // risky code
} catch (error) {
  // error handling
}
```

---

# Basic Example

```ts
try {
  throw new Error("Something went wrong");
} catch (error) {
  console.log(error);
}
```

---

# Output

```bash
Error: Something went wrong
```

---

# Real-world Example

```ts
try {
  const result = JSON.parse("invalid json");

  console.log(result);
} catch (error) {
  console.log("Invalid JSON");
}
```

---

# Output

```bash
Invalid JSON
```

---

# finally Block

`finally` always runs whether an error occurs or not.

---

# Example

```ts
try {
  console.log("Running...");
} catch (error) {
  console.log(error);
} finally {
  console.log("Finished");
}
```

---

# Output

```bash
Running...
Finished
```

---

# Throwing Custom Errors

Developers can create custom errors.

---

# Example

```ts
function divide(
  a: number,
  b: number
): number {
  if (b === 0) {
    throw new Error("Division by zero is not allowed");
  }

  return a / b;
}
```

---

# Usage

```ts
try {
  console.log(divide(10, 0));
} catch (error) {
  console.log(error);
}
```

---

# Output

```bash
Error: Division by zero is not allowed
```

---

# Error Object

The `Error` object contains useful information.

---

# Example

```ts
try {
  throw new Error("Server Error");
} catch (error) {
  console.log(error.message);
}
```

---

# Output

```bash
Server Error
```

---

# Custom Error Classes

TypeScript allows creating custom error classes.

---

# Example

```ts
class ValidationError extends Error {
  constructor(message: string) {
    super(message);

    this.name = "ValidationError";
  }
}
```

---

# Usage

```ts
throw new ValidationError("Invalid Email");
```

---

# Output

```bash
ValidationError: Invalid Email
```

---

# Async Error Handling

Async operations should use `try...catch`.

---

# Example

```ts
async function fetchData() {
  try {
    throw new Error("API Failed");
  } catch (error) {
    console.log(error);
  }
}

fetchData();
```

---

# Output

```bash
Error: API Failed
```

---

# Promise Error Handling

Promises use `.catch()`.

---

# Example

```ts
Promise.reject("Failed")
  .catch(error => {
    console.log(error);
  });
```

---

# Output

```bash
Failed
```

---

# Debugging with VS Code

VS Code provides powerful debugging tools.

---

# Features

- Breakpoints
- Step execution
- Variable inspection
- Call stack analysis

---

# Add Breakpoint

Click beside the line number in VS Code.

---

# Start Debugging

Shortcut:

```bash
F5
```

---

# Source Maps

Source maps connect compiled JavaScript to original TypeScript code.

---

# Enable Source Maps

## tsconfig.json

```json
{
  "compilerOptions": {
    "sourceMap": true
  }
}
```

---

# Benefits of Source Maps

- Easier debugging
- Better stack traces
- Direct TypeScript debugging

---

# Assertions for Validation

Assertions help validate conditions.

---

# Example

```ts
function assert(
  condition: boolean,
  message: string
): void {
  if (!condition) {
    throw new Error(message);
  }
}
```

---

# Usage

```ts
assert(5 > 10, "Invalid Condition");
```

---

# Output

```bash
Error: Invalid Condition
```

---

# Optional Chaining

Optional chaining prevents runtime crashes.

---

# Example

```ts
const user = {
  profile: {
    name: "Ali"
  }
};

console.log(user.profile?.name);
```

---

# Output

```bash
Ali
```

---

# Nullish Coalescing

Provides default values safely.

---

# Example

```ts
let username: string | null = null;

console.log(username ?? "Guest");
```

---

# Output

```bash
Guest
```

---

# Logging Errors Professionally

Bad practice:

```ts
console.log(error);
```

---

# Better Practice

```ts
console.error("Application Error:", error);
```

---

# Input Validation

Always validate user input.

---

# Example

```ts
function register(age: number) {
  if (age < 18) {
    throw new Error("Age must be 18 or above");
  }

  console.log("Registered");
}
```

---

# Common Debugging Techniques

| Technique | Purpose |
|---|---|
| console.log | Inspect values |
| Breakpoints | Pause execution |
| Stack traces | Track errors |
| Source maps | Debug TS directly |

---

# Common Beginner Mistakes

| Mistake | Problem |
|---|---|
| Ignoring errors | Unstable apps |
| Using any everywhere | Hidden bugs |
| No input validation | Runtime failures |
| Empty catch blocks | Difficult debugging |

---

# Best Practices

- Always handle errors properly
- Use meaningful error messages
- Validate user input
- Use source maps
- Avoid silent failures
- Use custom error classes when needed

---

# Real-world Example

```ts
class AuthenticationError extends Error {
  constructor(message: string) {
    super(message);

    this.name = "AuthenticationError";
  }
}

function login(
  username: string,
  password: string
): void {
  if (!username || !password) {
    throw new AuthenticationError(
      "Username and password are required"
    );
  }

  console.log("Login Successful");
}

try {
  login("", "");
} catch (error) {
  console.error(error);
}
```

---

# Output

```bash
AuthenticationError: Username and password are required
```

---

# Advantages of Proper Error Handling

- Better stability
- Improved user experience
- Easier debugging
- Safer applications
- Professional architecture

---

# Conclusion

Error handling and debugging are critical skills for professional TypeScript development.

They help developers build:

- Reliable systems
- Stable applications
- Scalable architectures
- Professional software
- Production-ready applications

# 14. Async Programming in TypeScript

Async programming allows applications to perform tasks without blocking execution.

It is used for:

- API requests
- Database operations
- File handling
- Timers
- Authentication systems
- Background tasks

---

# What is Synchronous Programming?

Synchronous code runs line by line.

Each task waits for the previous task to finish.

---

# Example

```ts
console.log("Start");

console.log("Process");

console.log("End");
```

---

# Output

```bash
Start
Process
End
```

---

# Problem with Synchronous Code

Long-running tasks block the application.

Examples:

- API requests
- Database queries
- File uploads

---

# What is Asynchronous Programming?

Asynchronous programming allows tasks to run in the background without blocking the application.

---

# Example

```ts
console.log("Start");

setTimeout(() => {
  console.log("Processing");
}, 2000);

console.log("End");
```

---

# Output

```bash
Start
End
Processing
```

---

# What is a Callback?

A callback is a function passed into another function.

---

# Callback Example

```ts
function greet(
  name: string,
  callback: () => void
) {
  console.log(`Hello ${name}`);

  callback();
}

greet("Ali", () => {
  console.log("Callback Executed");
});
```

---

# Output

```bash
Hello Ali
Callback Executed
```

---

# Callback Problems

Large callback chains create:

- Callback Hell
- Difficult debugging
- Poor readability

---

# What is a Promise?

A Promise represents a future result.

Promises improve asynchronous code readability.

---

# Promise States

| State | Description |
|---|---|
| Pending | Waiting |
| Fulfilled | Success |
| Rejected | Failed |

---

# Basic Promise Syntax

```ts
const promise = new Promise((resolve, reject) => {
  // async task
});
```

---

# Simple Promise Example

```ts
const myPromise = new Promise<string>(
  (resolve, reject) => {
    resolve("Data Loaded");
  }
);
```

---

# Using Promise

```ts
myPromise.then(data => {
  console.log(data);
});
```

---

# Output

```bash
Data Loaded
```

---

# Promise Rejection

```ts
const login = new Promise(
  (resolve, reject) => {
    reject("Invalid Credentials");
  }
);
```

---

# Handle Error

```ts
login.catch(error => {
  console.log(error);
});
```

---

# Output

```bash
Invalid Credentials
```

---

# Promise Chaining

Promises can be chained using `.then()`.

---

# Example

```ts
Promise.resolve(5)
  .then(value => value * 2)
  .then(value => value + 10)
  .then(result => {
    console.log(result);
  });
```

---

# Output

```bash
20
```

---

# Async & Await

`async/await` simplifies asynchronous programming.

---

# Async Function

```ts
async function fetchData() {
  return "Data Loaded";
}
```

---

# Using Async Function

```ts
fetchData().then(data => {
  console.log(data);
});
```

---

# Output

```bash
Data Loaded
```

---

# Await Keyword

`await` pauses execution until a Promise completes.

---

# Example

```ts
async function getData() {
  const result = await Promise.resolve(
    "TypeScript"
  );

  console.log(result);
}

getData();
```

---

# Output

```bash
TypeScript
```

---

# Async Error Handling

Always use `try...catch` with async code.

---

# Example

```ts
async function loadData() {
  try {
    throw new Error("API Failed");
  } catch (error) {
    console.log(error);
  }
}

loadData();
```

---

# Output

```bash
Error: API Failed
```

---

# Fetch API

Fetch API retrieves data from servers.

---

# Example

```ts
async function getUsers() {
  const response = await fetch(
    "https://jsonplaceholder.typicode.com/users"
  );

  const data = await response.json();

  console.log(data);
}
```

---

# HTTP Methods

| Method | Purpose |
|---|---|
| GET | Retrieve data |
| POST | Create data |
| PUT | Update data |
| DELETE | Remove data |

---

# GET Request Example

```ts
async function getPosts() {
  const response = await fetch(
    "https://jsonplaceholder.typicode.com/posts"
  );

  const posts = await response.json();

  console.log(posts);
}
```

---

# POST Request Example

```ts
async function createPost() {
  const response = await fetch(
    "https://jsonplaceholder.typicode.com/posts",
    {
      method: "POST",

      headers: {
        "Content-Type": "application/json"
      },

      body: JSON.stringify({
        title: "TypeScript"
      })
    }
  );

  const data = await response.json();

  console.log(data);
}
```

---

# Promise.all()

Runs multiple promises simultaneously.

---

# Example

```ts
async function loadAll() {
  const results = await Promise.all([
    Promise.resolve("Users"),
    Promise.resolve("Products")
  ]);

  console.log(results);
}

loadAll();
```

---

# Output

```bash
["Users", "Products"]
```

---

# Promise.race()

Returns the first completed promise.

---

# Example

```ts
Promise.race([
  new Promise(resolve =>
    setTimeout(() => resolve("Fast"), 1000)
  ),

  new Promise(resolve =>
    setTimeout(() => resolve("Slow"), 3000)
  )
]).then(result => {
  console.log(result);
});
```

---

# Output

```bash
Fast
```

---

# setTimeout()

Executes code after delay.

---

# Example

```ts
setTimeout(() => {
  console.log("Executed");
}, 2000);
```

---

# setInterval()

Executes code repeatedly.

---

# Example

```ts
setInterval(() => {
  console.log("Running");
}, 1000);
```

---

# Clearing Interval

```ts
const interval = setInterval(() => {
  console.log("Hello");
}, 1000);

clearInterval(interval);
```

---

# Async Functions with Types

```ts
async function getMessage(): Promise<string> {
  return "Hello";
}
```

---

# Generic Async Function

```ts
async function fetchData<T>(
  url: string
): Promise<T> {
  const response = await fetch(url);

  return response.json();
}
```

---

# Example Usage

```ts
interface User {
  id: number;
  name: string;
}

fetchData<User[]>(
  "https://jsonplaceholder.typicode.com/users"
);
```

---

# Real-world Login Example

```ts
async function login(
  username: string,
  password: string
): Promise<string> {
  if (
    username === "admin" &&
    password === "123"
  ) {
    return "Login Successful";
  }

  throw new Error("Invalid Credentials");
}
```

---

# Usage

```ts
async function authenticate() {
  try {
    const result = await login(
      "admin",
      "123"
    );

    console.log(result);
  } catch (error) {
    console.log(error);
  }
}

authenticate();
```

---

# Output

```bash
Login Successful
```

---

# Common Beginner Mistakes

| Mistake | Problem |
|---|---|
| Missing await | Unexpected behavior |
| Ignoring errors | Application crashes |
| Callback nesting | Poor readability |
| Blocking async flow | Slow applications |

---

# Best Practices

- Prefer async/await
- Always handle errors
- Avoid callback hell
- Use Promise.all for parallel tasks
- Use proper return types
- Keep async functions clean

---

# Async Architecture Example

```bash
src/
│
├── api/
├── services/
├── utils/
├── interfaces/
└── app.ts
```

---

# Advantages of Async Programming

- Better performance
- Faster applications
- Improved user experience
- Non-blocking execution
- Scalable architecture

---

# Conclusion

Async programming is essential for modern TypeScript development.

Understanding async concepts helps developers build:

- Real-time applications
- APIs
- Professional backend systems
- Scalable web applications
- Production-ready software

# 15. TypeScript with React

TypeScript with React helps developers build scalable, maintainable, and type-safe frontend applications.

It improves:

- Component safety
- Developer experience
- Code quality
- Scalability
- Team collaboration

---

# Why Use TypeScript with React?

React applications become complex as they grow.

TypeScript helps by providing:

- Static typing
- Better IntelliSense
- Early error detection
- Safer props handling
- Cleaner architecture

---

# Benefits of React + TypeScript

| Benefit | Description |
|---|---|
| Type Safety | Prevents invalid data |
| Better Auto-completion | Faster development |
| Easier Refactoring | Safe code updates |
| Better Maintainability | Cleaner structure |
| Improved Team Collaboration | Predictable code |

---

# Create React App with TypeScript

---

# Using Vite (Recommended)

```bash
npm create vite@latest my-app -- --template react-ts
```

---

# Move Into Project

```bash
cd my-app
```

---

# Install Dependencies

```bash
npm install
```

---

# Start Development Server

```bash
npm run dev
```

---

# Using Create React App

```bash
npx create-react-app my-app --template typescript
```

---

# Project Structure

```bash
src/
│
├── components/
├── pages/
├── hooks/
├── services/
├── interfaces/
├── types/
├── App.tsx
└── main.tsx
```

---

# File Extensions in React TypeScript

| Extension | Purpose |
|---|---|
| .ts | TypeScript file |
| .tsx | React TypeScript component |

---

# First React Component

## App.tsx

```tsx
function App() {
  return <h1>Hello TypeScript</h1>;
}

export default App;
```

---

# Functional Components

Modern React uses functional components.

---

# Example

```tsx
const Header = () => {
  return <h1>Welcome</h1>;
};

export default Header;
```

---

# Props in React TypeScript

Props should always be typed.

---

# Basic Props Example

```tsx
type Props = {
  title: string;
};

const Header = ({ title }: Props) => {
  return <h1>{title}</h1>;
};
```

---

# Usage

```tsx
<Header title="TypeScript" />
```

---

# Multiple Props

```tsx
type UserProps = {
  name: string;
  age: number;
};
```

---

# Component Example

```tsx
const User = ({
  name,
  age
}: UserProps) => {
  return (
    <div>
      <h2>{name}</h2>
      <p>{age}</p>
    </div>
  );
};
```

---

# Optional Props

Optional props use `?`.

---

# Example

```tsx
type ButtonProps = {
  text: string;
  color?: string;
};
```

---

# Default Props

```tsx
const Button = ({
  text,
  color = "blue"
}: ButtonProps) => {
  return (
    <button>{text}</button>
  );
};
```

---

# Children Props

React components can receive children.

---

# Example

```tsx
type CardProps = {
  children: React.ReactNode;
};
```

---

# Component

```tsx
const Card = ({
  children
}: CardProps) => {
  return <div>{children}</div>;
};
```

---

# Usage

```tsx
<Card>
  <h1>Hello</h1>
</Card>
```

---

# useState Hook

`useState` manages component state.

---

# Basic Example

```tsx
import { useState } from "react";

const Counter = () => {
  const [count, setCount] =
    useState<number>(0);

  return (
    <button
      onClick={() =>
        setCount(count + 1)
      }
    >
      {count}
    </button>
  );
};
```

---

# useState with String

```tsx
const [name, setName] =
  useState<string>("");
```

---

# useState with Array

```tsx
const [users, setUsers] =
  useState<string[]>([]);
```

---

# useState with Objects

```tsx
type User = {
  name: string;
  age: number;
};

const [user, setUser] =
  useState<User | null>(null);
```

---

# useEffect Hook

`useEffect` handles side effects.

---

# Example

```tsx
import { useEffect } from "react";

useEffect(() => {
  console.log("Component Mounted");
}, []);
```

---

# Fetch API Data

```tsx
import { useEffect, useState } from "react";

type User = {
  id: number;
  name: string;
};

const Users = () => {
  const [users, setUsers] =
    useState<User[]>([]);

  useEffect(() => {
    fetch(
      "https://jsonplaceholder.typicode.com/users"
    )
      .then(res => res.json())
      .then(data => setUsers(data));
  }, []);

  return (
    <div>
      {users.map(user => (
        <p key={user.id}>
          {user.name}
        </p>
      ))}
    </div>
  );
};
```

---

# Event Typing

Events should be typed properly.

---

# Input Change Event

```tsx
const handleChange = (
  event: React.ChangeEvent<HTMLInputElement>
) => {
  console.log(event.target.value);
};
```

---

# Button Click Event

```tsx
const handleClick = (
  event: React.MouseEvent<HTMLButtonElement>
) => {
  console.log("Clicked");
};
```

---

# Forms in React TypeScript

---

# Example

```tsx
import { useState } from "react";

const LoginForm = () => {
  const [email, setEmail] =
    useState<string>("");

  return (
    <input
      type="email"
      value={email}
      onChange={e =>
        setEmail(e.target.value)
      }
    />
  );
};
```

---

# useRef Hook

`useRef` references DOM elements.

---

# Example

```tsx
import { useRef } from "react";

const Input = () => {
  const inputRef =
    useRef<HTMLInputElement>(null);

  return (
    <input ref={inputRef} />
  );
};
```

---

# Context API with TypeScript

---

# Create Context Type

```tsx
type ThemeContextType = {
  theme: string;
};
```

---

# Create Context

```tsx
import { createContext } from "react";

export const ThemeContext =
  createContext<
    ThemeContextType | undefined
  >(undefined);
```

---

# React.FC

React provides `React.FC`.

---

# Example

```tsx
const Header: React.FC = () => {
  return <h1>Header</h1>;
};
```

---

# Interfaces vs Types for Props

| Interface | Type |
|---|---|
| Better for extension | Better for unions |
| Common in large apps | Flexible syntax |

---

# Component Folder Structure

```bash
components/
│
├── Button/
│   ├── Button.tsx
│   ├── Button.module.css
│   └── index.ts
```

---

# Custom Hooks

---

# Example

```tsx
import { useState } from "react";

export function useCounter() {
  const [count, setCount] =
    useState<number>(0);

  const increment = () =>
    setCount(count + 1);

  return {
    count,
    increment
  };
}
```

---

# Using Custom Hook

```tsx
const Counter = () => {
  const { count, increment } =
    useCounter();

  return (
    <button onClick={increment}>
      {count}
    </button>
  );
};
```

---

# API Service Structure

```bash
src/
│
├── services/
│   └── api.ts
```

---

# Example API Service

```ts
export async function getUsers() {
  const response = await fetch(
    "https://jsonplaceholder.typicode.com/users"
  );

  return response.json();
}
```

---

# Environment Variables

## Example

```bash
VITE_API_URL=https://api.example.com
```

---

# Access Variable

```ts
const apiUrl =
  import.meta.env.VITE_API_URL;
```

---

# React Router with TypeScript

---

# Install

```bash
npm install react-router-dom
```

---

# Example

```tsx
import {
  BrowserRouter,
  Routes,
  Route
} from "react-router-dom";
```

---

# Lazy Loading

---

# Example

```tsx
import { lazy } from "react";

const Home = lazy(() =>
  import("./pages/Home")
);
```

---

# Common Beginner Mistakes

| Mistake | Problem |
|---|---|
| Using any everywhere | Unsafe components |
| Untyped props | Runtime bugs |
| Large components | Hard maintenance |
| Poor folder structure | Scalability issues |

---

# Best Practices

- Type all props
- Use reusable components
- Separate business logic
- Create custom hooks
- Use proper folder structure
- Avoid unnecessary any

---

# Professional Architecture Example

```bash
src/
│
├── assets/
├── components/
├── hooks/
├── layouts/
├── pages/
├── routes/
├── services/
├── store/
├── types/
├── utils/
└── App.tsx
```

---

# Real-world Example

```tsx
type ProductProps = {
  name: string;
  price: number;
};

const ProductCard = ({
  name,
  price
}: ProductProps) => {
  return (
    <div>
      <h2>{name}</h2>
      <p>${price}</p>
    </div>
  );
};

export default ProductCard;
```

---

# Usage

```tsx
<ProductCard
  name="Laptop"
  price={1200}
/>
```

---

# Advantages of React + TypeScript

- Better scalability
- Safer components
- Cleaner architecture
- Better collaboration
- Improved maintainability

---

# Conclusion

React with TypeScript is one of the best combinations for modern frontend development.

It helps developers build:

- Scalable applications
- Enterprise-level systems
- Reusable components
- Professional architectures
- Production-ready frontend applications

# 17. Advanced TypeScript Concepts

Advanced TypeScript concepts help developers build enterprise-level, scalable, and highly type-safe applications.

These concepts are widely used in:

- Large applications
- Frameworks
- Enterprise software
- APIs
- Libraries
- Professional frontend/backend systems

---

# What are Advanced Concepts?

Advanced TypeScript concepts include:

- Utility Types
- Conditional Types
- Mapped Types
- Decorators
- Advanced Generics
- Type Guards
- Indexed Access Types
- Infer Keyword
- Template Literal Types

---

# Utility Types

TypeScript provides built-in utility types to transform existing types.

---

# Partial Type

`Partial<T>` makes all properties optional.

---

# Example

```ts
interface User {
  name: string;
  age: number;
}

type PartialUser =
  Partial<User>;
```

---

# Usage

```ts
const user: PartialUser = {
  name: "Ali"
};
```

---

# Required Type

`Required<T>` makes all properties required.

---

# Example

```ts
interface Product {
  name?: string;
  price?: number;
}

type RequiredProduct =
  Required<Product>;
```

---

# Readonly Type

`Readonly<T>` prevents modification.

---

# Example

```ts
interface User {
  name: string;
}

const user: Readonly<User> = {
  name: "Ali"
};
```

---

# Invalid Modification

```ts
user.name = "Ahmed";
```

This produces an error.

---

# Pick Type

`Pick<T, K>` selects specific properties.

---

# Example

```ts
interface User {
  id: number;
  name: string;
  email: string;
}

type UserPreview =
  Pick<User, "name" | "email">;
```

---

# Omit Type

`Omit<T, K>` removes properties.

---

# Example

```ts
type UserWithoutEmail =
  Omit<User, "email">;
```

---

# Record Type

`Record<K, T>` creates object types dynamically.

---

# Example

```ts
type Scores = Record<
  string,
  number
>;
```

---

# Usage

```ts
const marks: Scores = {
  Ali: 90,
  Ahmed: 85
};
```

---

# Conditional Types

Conditional types use conditions inside types.

---

# Syntax

```ts
T extends U ? X : Y
```

---

# Example

```ts
type IsString<T> =
  T extends string
    ? "YES"
    : "NO";
```

---

# Usage

```ts
type Result1 =
  IsString<string>;

type Result2 =
  IsString<number>;
```

---

# Output

```bash
YES
NO
```

---

# Mapped Types

Mapped types transform properties dynamically.

---

# Example

```ts
type ReadonlyUser<T> = {
  readonly [K in keyof T]: T[K];
};
```

---

# Usage

```ts
interface User {
  name: string;
  age: number;
}

type SafeUser =
  ReadonlyUser<User>;
```

---

# keyof Operator

`keyof` extracts object keys.

---

# Example

```ts
interface User {
  name: string;
  age: number;
}

type UserKeys = keyof User;
```

---

# Output

```bash
"name" | "age"
```

---

# Indexed Access Types

Access property types dynamically.

---

# Example

```ts
interface User {
  name: string;
  age: number;
}

type NameType =
  User["name"];
```

---

# Output

```bash
string
```

---

# Type Guards

Type guards narrow types safely.

---

# typeof Guard

```ts
function print(
  value: string | number
) {
  if (typeof value === "string") {
    console.log(
      value.toUpperCase()
    );
  }
}
```

---

# instanceof Guard

```ts
class User {}

const user = new User();

console.log(
  user instanceof User
);
```

---

# Custom Type Guards

---

# Example

```ts
type Admin = {
  role: string;
};

function isAdmin(
  user: any
): user is Admin {
  return user.role !== undefined;
}
```

---

# Decorators

Decorators add metadata to classes and methods.

---

# Enable Decorators

## tsconfig.json

```json
{
  "experimentalDecorators": true
}
```

---

# Class Decorator Example

```ts
function Logger(
  constructor: Function
) {
  console.log("Logging...");
}

@Logger
class User {}
```

---

# Method Decorator Example

```ts
function Log(
  target: any,
  propertyKey: string
) {
  console.log(propertyKey);
}
```

---

# Generic Constraints

Constraints limit generic types.

---

# Example

```ts
function printLength<
  T extends {
    length: number;
  }
>(item: T) {
  console.log(item.length);
}
```

---

# Usage

```ts
printLength("Hello");
printLength([1, 2, 3]);
```

---

# Infer Keyword

`infer` extracts types dynamically.

---

# Example

```ts
type ReturnTypeOf<T> =
  T extends (
    ...args: any[]
  ) => infer R
    ? R
    : never;
```

---

# Template Literal Types

Create dynamic string types.

---

# Example

```ts
type Direction =
  "left" | "right";

type Move =
  `move-${Direction}`;
```

---

# Output

```bash
"move-left"
"move-right"
```

---

# Advanced Generic Example

```ts
class Repository<T> {
  private items: T[] = [];

  add(item: T) {
    this.items.push(item);
  }

  getAll(): T[] {
    return this.items;
  }
}
```

---

# Usage

```ts
const users =
  new Repository<string>();

users.add("Ali");

console.log(users.getAll());
```

---

# Output

```bash
["Ali"]
```

---

# Deep Readonly Type

---

# Example

```ts
type DeepReadonly<T> = {
  readonly [K in keyof T]:
    T[K] extends object
      ? DeepReadonly<T[K]>
      : T[K];
};
```

---

# Function Overloads

Multiple function signatures.

---

# Example

```ts
function combine(
  a: string,
  b: string
): string;

function combine(
  a: number,
  b: number
): number;

function combine(
  a: any,
  b: any
) {
  return a + b;
}
```

---

# Usage

```ts
console.log(
  combine("Hello ", "TS")
);

console.log(
  combine(10, 20)
);
```

---

# Output

```bash
Hello TS
30
```

---

# Advanced Async Types

---

# Example

```ts
type ApiResponse<T> = {
  success: boolean;
  data: T;
};
```

---

# Usage

```ts
interface User {
  id: number;
  name: string;
}

const response:
  ApiResponse<User> = {
    success: true,
    data: {
      id: 1,
      name: "Ali"
    }
  };
```

---

# Namespace Example

```ts
namespace MathUtils {
  export function add(
    a: number,
    b: number
  ) {
    return a + b;
  }
}
```

---

# Usage

```ts
console.log(
  MathUtils.add(5, 5)
);
```

---

# Output

```bash
10
```

---

# Performance Optimization Tips

- Use lazy loading
- Avoid unnecessary types
- Reduce deep nesting
- Use reusable utilities
- Prefer modular architecture

---

# Enterprise Architecture Example

```bash
src/
│
├── api/
├── core/
├── decorators/
├── hooks/
├── interfaces/
├── middleware/
├── repositories/
├── services/
├── types/
├── utils/
└── app.ts
```

---

# Common Beginner Mistakes

| Mistake | Problem |
|---|---|
| Overcomplicated types | Hard readability |
| Using any everywhere | Unsafe architecture |
| Ignoring utility types | Duplicate code |
| Deep nesting | Complex maintenance |

---

# Best Practices

- Keep types readable
- Use utility types wisely
- Prefer reusable generics
- Avoid unnecessary complexity
- Separate advanced types into files
- Use strict mode

---

# Real-world Example

```ts
interface ApiResponse<T> {
  success: boolean;
  data: T;
}

interface Product {
  id: number;
  name: string;
  price: number;
}

async function getProducts():
Promise<
  ApiResponse<Product[]>
> {
  return {
    success: true,
    data: [
      {
        id: 1,
        name: "Laptop",
        price: 1200
      }
    ]
  };
}

getProducts().then(
  response => {
    console.log(response);
  }
);
```

---

# Output

```bash
{
  success: true,
  data: [
    {
      id: 1,
      name: 'Laptop',
      price: 1200
    }
  ]
}
```

---

# Advantages of Advanced TypeScript

- Stronger type safety
- Better scalability
- Cleaner architecture
- Enterprise-level development
- Highly reusable code

---

# Conclusion

Advanced TypeScript concepts help developers build:

- Enterprise applications
- Large-scale systems
- Professional architectures
- Highly reusable codebases
- Production-ready software

# 18. TypeScript Backend Development with Node.js & Express

TypeScript is widely used for backend development to build scalable, secure, and enterprise-level server applications.

This section covers:

- Node.js with TypeScript
- Express.js setup
- REST APIs
- Middleware
- Authentication
- Database integration
- Professional backend architecture

---

# Why Use TypeScript for Backend?

TypeScript improves backend development by providing:

- Strong typing
- Better scalability
- Safer APIs
- Cleaner architecture
- Better developer experience

---

# What is Node.js?

Node.js is a JavaScript runtime used for backend development.

It allows developers to build:

- APIs
- Realtime applications
- Authentication systems
- Microservices
- Full-stack applications

---

# What is Express.js?

Express.js is a lightweight backend framework for Node.js.

It simplifies:

- Routing
- Middleware
- API creation
- Request handling

---

# Create Backend Project

---

# Step 1 — Create Folder

```bash
mkdir ts-backend
```

---

# Step 2 — Move Into Folder

```bash
cd ts-backend
```

---

# Step 3 — Initialize Project

```bash
npm init -y
```

---

# Step 4 — Install Dependencies

```bash
npm install express
```

---

# Install TypeScript Dependencies

```bash
npm install --save-dev typescript ts-node nodemon @types/node @types/express
```

---

# Step 5 — Initialize TypeScript

```bash
npx tsc --init
```

---

# Recommended Project Structure

```bash
src/
│
├── controllers/
├── middleware/
├── models/
├── routes/
├── services/
├── interfaces/
├── utils/
├── config/
└── server.ts
```

---

# Configure tsconfig.json

```json
{
  "compilerOptions": {
    "target": "ES6",
    "module": "commonjs",
    "rootDir": "./src",
    "outDir": "./dist",
    "strict": true,
    "esModuleInterop": true
  }
}
```

---

# Create Express Server

## src/server.ts

```ts
import express from "express";

const app = express();

const PORT = 5000;

app.listen(PORT, () => {
  console.log(
    `Server running on port ${PORT}`
  );
});
```

---

# Run Development Server

```bash
npx ts-node src/server.ts
```

---

# Output

```bash
Server running on port 5000
```

---

# Create First Route

```ts
app.get("/", (req, res) => {
  res.send("Hello TypeScript Backend");
});
```

---

# Output

```bash
Hello TypeScript Backend
```

---

# Express Middleware

Middleware processes requests before responses are sent.

---

# Example Middleware

```ts
app.use((req, res, next) => {
  console.log("Request Received");

  next();
});
```

---

# JSON Middleware

```ts
app.use(express.json());
```

---

# Route Parameters

---

# Example

```ts
app.get(
  "/user/:id",
  (req, res) => {
    res.send(req.params.id);
  }
);
```

---

# URL Example

```bash
/user/10
```

---

# Output

```bash
10
```

---

# Query Parameters

---

# Example

```ts
app.get("/search", (req, res) => {
  res.send(req.query.name);
});
```

---

# URL Example

```bash
/search?name=Ali
```

---

# Output

```bash
Ali
```

---

# Request Body

---

# Example

```ts
app.post("/user", (req, res) => {
  console.log(req.body);

  res.send("User Created");
});
```

---

# Example JSON Body

```json
{
  "name": "Ali",
  "age": 22
}
```

---

# Type Request Body

```ts
interface User {
  name: string;
  age: number;
}
```

---

# Usage

```ts
app.post(
  "/user",
  (
    req: Request<
      {},
      {},
      User
    >,
    res: Response
  ) => {
    res.send(req.body);
  }
);
```

---

# Create Router

## routes/userRoutes.ts

```ts
import express from "express";

const router = express.Router();

router.get("/", (req, res) => {
  res.send("Users Route");
});

export default router;
```

---

# Use Router

## server.ts

```ts
import userRoutes
from "./routes/userRoutes";

app.use("/users", userRoutes);
```

---

# Controller Architecture

Controllers separate request logic.

---

# Example

## controllers/userController.ts

```ts
export const getUsers = (
  req: Request,
  res: Response
) => {
  res.send("All Users");
};
```

---

# Service Layer

Services contain business logic.

---

# Example

## services/userService.ts

```ts
export function fetchUsers() {
  return [
    {
      id: 1,
      name: "Ali"
    }
  ];
}
```

---

# Environment Variables

Install dotenv:

```bash
npm install dotenv
```

---

# Create .env File

```bash
PORT=5000
DB_URL=mongodb://localhost
```

---

# Load Environment Variables

```ts
import dotenv from "dotenv";

dotenv.config();
```

---

# Access Variables

```ts
const PORT =
  process.env.PORT;
```

---

# Error Handling Middleware

---

# Example

```ts
app.use(
  (
    err: Error,
    req: Request,
    res: Response,
    next: NextFunction
  ) => {
    res.status(500).json({
      message: err.message
    });
  }
);
```

---

# Async Route Example

```ts
app.get(
  "/products",
  async (req, res) => {
    const products = await Promise.resolve([
      {
        id: 1,
        name: "Laptop"
      }
    ]);

    res.json(products);
  }
);
```

---

# HTTP Status Codes

| Code | Meaning |
|---|---|
| 200 | Success |
| 201 | Created |
| 400 | Bad Request |
| 401 | Unauthorized |
| 404 | Not Found |
| 500 | Server Error |

---

# Send JSON Response

```ts
res.status(200).json({
  success: true
});
```

---

# Authentication Example

---

# Install JWT

```bash
npm install jsonwebtoken bcryptjs
```

---

# Example Login

```ts
import jwt from "jsonwebtoken";

const token = jwt.sign(
  {
    id: 1
  },
  "SECRET_KEY"
);
```

---

# Verify Token Middleware

```ts
function authMiddleware(
  req: Request,
  res: Response,
  next: NextFunction
) {
  next();
}
```

---

# Database Integration

---

# Install MongoDB Packages

```bash
npm install mongoose
```

---

# Create Database Connection

## config/database.ts

```ts
import mongoose from "mongoose";

export async function connectDB() {
  await mongoose.connect(
    process.env.DB_URL as string
  );

  console.log("Database Connected");
}
```

---

# Create Model

## models/User.ts

```ts
import mongoose from "mongoose";

const userSchema =
  new mongoose.Schema({
    name: String,
    age: Number
  });

export default mongoose.model(
  "User",
  userSchema
);
```

---

# Create User

```ts
const user = await User.create({
  name: "Ali",
  age: 22
});
```

---

# Validation Example

```ts
if (!email) {
  return res.status(400).json({
    message: "Email Required"
  });
}
```

---

# Async Error Wrapper

```ts
function asyncHandler(
  fn: Function
) {
  return (
    req: Request,
    res: Response,
    next: NextFunction
  ) => {
    Promise.resolve(
      fn(req, res, next)
    ).catch(next);
  };
}
```

---

# API Response Structure

```json
{
  "success": true,
  "message": "User Created",
  "data": {}
}
```

---

# Professional Architecture

```bash
src/
│
├── config/
├── controllers/
├── database/
├── interfaces/
├── middleware/
├── models/
├── routes/
├── services/
├── utils/
└── server.ts
```

---

# Logging Requests

Install Morgan:

```bash
npm install morgan
```

---

# Usage

```ts
import morgan from "morgan";

app.use(morgan("dev"));
```

---

# Security Best Practices

Install Helmet:

```bash
npm install helmet
```

---

# Usage

```ts
import helmet from "helmet";

app.use(helmet());
```

---

# CORS Setup

Install CORS:

```bash
npm install cors
```

---

# Usage

```ts
import cors from "cors";

app.use(cors());
```

---

# Production Scripts

## package.json

```json
{
  "scripts": {
    "dev": "nodemon src/server.ts",
    "build": "tsc",
    "start": "node dist/server.js"
  }
}
```

---

# Common Beginner Mistakes

| Mistake | Problem |
|---|---|
| Large server.ts file | Poor scalability |
| No error handling | Application crashes |
| Using any | Unsafe APIs |
| Hardcoded secrets | Security risks |

---

# Best Practices

- Use layered architecture
- Separate controllers/services
- Validate user input
- Use environment variables
- Handle errors properly
- Use TypeScript interfaces

---

# Real-world API Example

```ts
interface Product {
  id: number;
  name: string;
  price: number;
}

const products: Product[] = [
  {
    id: 1,
    name: "Laptop",
    price: 1200
  }
];

app.get(
  "/products",
  (req, res) => {
    res.json(products);
  }
);
```

---

# Output

```json
[
  {
    "id": 1,
    "name": "Laptop",
    "price": 1200
  }
]
```

---

# Advantages of TypeScript Backend Development

- Better scalability
- Cleaner APIs
- Strong type safety
- Professional architecture
- Easier maintenance

---

# Conclusion

TypeScript with Node.js and Express is one of the best choices for modern backend development.

It helps developers build:

- Secure APIs
- Enterprise systems
- Scalable architectures
- Production-ready applications
- Professional backend solutions

# 19. Database Integration in TypeScript

Databases are used to store, manage, and retrieve application data.

TypeScript applications commonly integrate databases for:

- Authentication systems
- E-commerce applications
- Social media platforms
- APIs
- Enterprise software

---

# Types of Databases

There are two main database categories.

| Type | Example |
|---|---|
| SQL Database | MySQL, PostgreSQL |
| NoSQL Database | MongoDB |

---

# SQL vs NoSQL

| SQL | NoSQL |
|---|---|
| Table-based | Document-based |
| Structured schema | Flexible schema |
| Relational | Non-relational |
| Example: PostgreSQL | Example: MongoDB |

---

# Why Use TypeScript with Databases?

TypeScript provides:

- Type safety
- Better data validation
- Safer queries
- Better scalability
- Cleaner architecture

---

# Popular Database Libraries

| Database | Library |
|---|---|
| MongoDB | Mongoose |
| PostgreSQL | Prisma |
| MySQL | Sequelize |
| SQLite | Prisma |

---

# MongoDB with Mongoose

MongoDB is one of the most popular NoSQL databases.

---

# Install Mongoose

```bash
npm install mongoose
```

---

# Install Type Definitions

```bash
npm install --save-dev @types/mongoose
```

---

# Create Database Connection

## config/database.ts

```ts
import mongoose from "mongoose";

export async function connectDB() {
  try {
    await mongoose.connect(
      process.env.DB_URL as string
    );

    console.log(
      "Database Connected"
    );
  } catch (error) {
    console.error(error);
  }
}
```

---

# Environment Variables

## .env

```bash
DB_URL=mongodb://127.0.0.1:27017/mydb
```

---

# Load Environment Variables

```ts
import dotenv from "dotenv";

dotenv.config();
```

---

# Create User Schema

## models/User.ts

```ts
import mongoose from "mongoose";

const userSchema =
  new mongoose.Schema({
    name: {
      type: String,
      required: true
    },

    email: {
      type: String,
      required: true
    },

    age: Number
  });
```

---

# Export Model

```ts
export default mongoose.model(
  "User",
  userSchema
);
```

---

# Create User Interface

```ts
export interface IUser {
  name: string;
  email: string;
  age?: number;
}
```

---

# Create User

```ts
const user = await User.create({
  name: "Ali",
  email: "ali@gmail.com",
  age: 22
});
```

---

# Get All Users

```ts
const users = await User.find();
```

---

# Find Single User

```ts
const user = await User.findById(id);
```

---

# Update User

```ts
await User.findByIdAndUpdate(
  id,
  {
    name: "Ahmed"
  }
);
```

---

# Delete User

```ts
await User.findByIdAndDelete(id);
```

---

# Express Controller Example

## controllers/userController.ts

```ts
import User from "../models/User";

export async function getUsers(
  req,
  res
) {
  const users = await User.find();

  res.json(users);
}
```

---

# Add Route

## routes/userRoutes.ts

```ts
router.get(
  "/users",
  getUsers
);
```

---

# Validation Example

```ts
if (!email) {
  return res.status(400).json({
    message: "Email Required"
  });
}
```

---

# Mongoose Schema Validation

```ts
email: {
  type: String,
  required: true,
  unique: true
}
```

---

# Timestamps

Automatically create:

- createdAt
- updatedAt

---

# Example

```ts
const userSchema =
  new mongoose.Schema(
    {
      name: String
    },
    {
      timestamps: true
    }
  );
```

---

# Password Hashing

Install bcrypt:

```bash
npm install bcryptjs
```

---

# Hash Password

```ts
import bcrypt from "bcryptjs";

const hashedPassword =
  await bcrypt.hash(
    password,
    10
  );
```

---

# Compare Password

```ts
const isMatch =
  await bcrypt.compare(
    password,
    user.password
  );
```

---

# JWT Authentication

Install JWT:

```bash
npm install jsonwebtoken
```

---

# Create Token

```ts
import jwt from "jsonwebtoken";

const token = jwt.sign(
  {
    id: user._id
  },
  "SECRET_KEY",
  {
    expiresIn: "7d"
  }
);
```

---

# Verify Token

```ts
jwt.verify(
  token,
  "SECRET_KEY"
);
```

---

# Authentication Middleware

```ts
function authMiddleware(
  req,
  res,
  next
) {
  next();
}
```

---

# Pagination Example

```ts
const page = 1;
const limit = 10;

const users = await User.find()
  .skip((page - 1) * limit)
  .limit(limit);
```

---

# Search Example

```ts
const users = await User.find({
  name: /ali/i
});
```

---

# Sorting Example

```ts
const users = await User.find()
  .sort({
    createdAt: -1
  });
```

---

# Populate Relationships

---

# Example

```ts
const posts = await Post.find()
  .populate("user");
```

---

# Transactions

Transactions ensure database consistency.

---

# Example

```ts
const session =
  await mongoose.startSession();

session.startTransaction();
```

---

# Error Handling Example

```ts
try {
  const users =
    await User.find();

  res.json(users);
} catch (error) {
  res.status(500).json({
    message: "Server Error"
  });
}
```

---

# Professional Backend Structure

```bash
src/
│
├── config/
├── controllers/
├── database/
├── middleware/
├── models/
├── routes/
├── services/
├── validators/
└── server.ts
```

---

# Prisma ORM

Prisma is a modern TypeScript ORM.

---

# Install Prisma

```bash
npm install prisma
```

---

# Initialize Prisma

```bash
npx prisma init
```

---

# Prisma Schema Example

## prisma/schema.prisma

```prisma
model User {
  id    Int    @id @default(autoincrement())
  name  String
  email String @unique
}
```

---

# Generate Prisma Client

```bash
npx prisma generate
```

---

# Create User with Prisma

```ts
const user =
  await prisma.user.create({
    data: {
      name: "Ali",
      email: "ali@gmail.com"
    }
  });
```

---

# PostgreSQL Connection

## .env

```bash
DATABASE_URL="postgresql://user:password@localhost:5432/mydb"
```

---

# Database Seeding

Seed initial data.

---

# Example

```ts
await User.create({
  name: "Admin",
  email: "admin@gmail.com"
});
```

---

# Repository Pattern

Repository pattern separates database logic.

---

# Example

## repositories/userRepository.ts

```ts
export class UserRepository {
  async findAll() {
    return User.find();
  }
}
```

---

# Service Layer Example

## services/userService.ts

```ts
export class UserService {
  async getUsers() {
    return User.find();
  }
}
```

---

# Performance Optimization

- Use indexes
- Avoid unnecessary queries
- Use pagination
- Cache data
- Optimize relationships

---

# Database Index Example

```ts
userSchema.index({
  email: 1
});
```

---

# Security Best Practices

- Validate user input
- Hash passwords
- Use environment variables
- Prevent SQL injection
- Limit sensitive data exposure

---

# Common Beginner Mistakes

| Mistake | Problem |
|---|---|
| No validation | Invalid data |
| Hardcoded credentials | Security risk |
| No indexing | Slow queries |
| Large controllers | Poor scalability |

---

# Best Practices

- Separate models/services/controllers
- Use interfaces
- Handle errors properly
- Validate input
- Use repository pattern
- Optimize queries

---

# Real-world Example

```ts
interface Product {
  name: string;
  price: number;
}

const productSchema =
  new mongoose.Schema<Product>({
    name: String,
    price: Number
  });

const Product =
  mongoose.model(
    "Product",
    productSchema
  );

async function createProduct() {
  const product =
    await Product.create({
      name: "Laptop",
      price: 1200
    });

  console.log(product);
}
```

---

# Output

```bash
{
  name: 'Laptop',
  price: 1200
}
```

---

# Advantages of Database Integration

- Persistent data storage
- Scalable applications
- Better data management
- Professional backend systems
- Enterprise-level architecture

---

# Conclusion

Database integration is one of the most important parts of backend development.

TypeScript helps developers build:

- Type-safe databases
- Scalable APIs
- Secure applications
- Enterprise systems
- Production-ready backend architectures

# 20. Deployment & Production in TypeScript

Deployment is the process of publishing an application to a live production environment so users can access it online.

Production-level TypeScript applications require:

- Optimization
- Security
- Scalability
- Monitoring
- Environment management
- CI/CD pipelines

---

# What is Production?

Production is the live environment where real users use the application.

---

# Development vs Production

| Development | Production |
|---|---|
| Local environment | Live server |
| Debugging enabled | Optimized |
| Frequent changes | Stable release |
| Testing stage | Real users |

---

# Why Deployment Matters

Deployment allows developers to:

- Publish applications online
- Share APIs globally
- Scale systems
- Deliver products to users

---

# Popular Deployment Platforms

| Platform | Usage |
|---|---|
| Vercel | Frontend deployment |
| Netlify | Static websites |
| Render | Full-stack apps |
| Railway | Backend deployment |
| AWS | Enterprise hosting |
| DigitalOcean | VPS hosting |

---

# Build TypeScript Project

Before deployment, TypeScript must compile into JavaScript.

---

# Build Command

```bash
npm run build
```

---

# TypeScript Compilation

```bash
tsc
```

---

# Output Folder

Compiled files are usually stored inside:

```bash
dist/
```

---

# Example Project Structure

```bash
project/
│
├── src/
├── dist/
├── node_modules/
├── package.json
├── tsconfig.json
└── .env
```

---

# Configure tsconfig.json

```json
{
  "compilerOptions": {
    "target": "ES6",
    "module": "commonjs",
    "rootDir": "./src",
    "outDir": "./dist",
    "strict": true
  }
}
```

---

# Package.json Scripts

---

# Example

```json
{
  "scripts": {
    "dev": "nodemon src/server.ts",
    "build": "tsc",
    "start": "node dist/server.js"
  }
}
```

---

# Install Production Tools

---

# Install Nodemon

```bash
npm install --save-dev nodemon
```

---

# Install ts-node

```bash
npm install --save-dev ts-node
```

---

# Environment Variables

Sensitive data should never be hardcoded.

---

# Create .env File

```bash
PORT=5000
DB_URL=mongodb://localhost
JWT_SECRET=mysecret
```

---

# Install dotenv

```bash
npm install dotenv
```

---

# Load Environment Variables

```ts
import dotenv from "dotenv";

dotenv.config();
```

---

# Access Variables

```ts
const PORT =
  process.env.PORT;
```

---

# Production Environment Example

```bash
NODE_ENV=production
```

---

# Security Best Practices

Production applications require strong security.

---

# Install Helmet

```bash
npm install helmet
```

---

# Usage

```ts
import helmet from "helmet";

app.use(helmet());
```

---

# Install CORS

```bash
npm install cors
```

---

# Usage

```ts
import cors from "cors";

app.use(cors());
```

---

# Request Logging

Install Morgan:

```bash
npm install morgan
```

---

# Usage

```ts
import morgan from "morgan";

app.use(morgan("dev"));
```

---

# Error Handling Middleware

---

# Example

```ts
app.use(
  (
    err,
    req,
    res,
    next
  ) => {
    res.status(500).json({
      message: err.message
    });
  }
);
```

---

# Build Optimization

Production builds should be optimized.

---

# Remove Console Logs

Bad practice:

```ts
console.log(data);
```

---

# Better Practice

Use proper logging systems.

---

# Minification

Minification reduces file size.

---

# Benefits

- Faster loading
- Better performance
- Smaller bundles

---

# Source Maps

Enable source maps for debugging.

---

# tsconfig.json

```json
{
  "compilerOptions": {
    "sourceMap": true
  }
}
```

---

# Docker Deployment

Docker packages applications into containers.

---

# Why Use Docker?

Docker provides:

- Consistent environments
- Easier deployment
- Better scalability

---

# Create Dockerfile

## Dockerfile

```dockerfile
FROM node:18

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

RUN npm run build

CMD ["npm", "start"]
```

---

# Build Docker Image

```bash
docker build -t ts-app .
```

---

# Run Docker Container

```bash
docker run -p 5000:5000 ts-app
```

---

# Deploy to Vercel

Best for frontend applications.

---

# Install Vercel CLI

```bash
npm install -g vercel
```

---

# Deploy

```bash
vercel
```

---

# Deploy Backend to Render

---

# Steps

1. Push code to GitHub
2. Connect repository to Render
3. Add environment variables
4. Deploy application

---

# Deploy to Railway

---

# Steps

1. Push project to GitHub
2. Connect Railway account
3. Configure environment variables
4. Deploy

---

# Deploy to AWS

AWS is used for enterprise hosting.

---

# AWS Services

| Service | Purpose |
|---|---|
| EC2 | Virtual server |
| S3 | File storage |
| RDS | Database |
| Lambda | Serverless functions |

---

# CI/CD Pipeline

CI/CD automates testing and deployment.

---

# CI/CD Benefits

- Faster deployment
- Automatic testing
- Reduced errors
- Better collaboration

---

# GitHub Actions Example

## .github/workflows/deploy.yml

```yaml
name: Deploy

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v3

      - name: Install Dependencies
        run: npm install

      - name: Build Project
        run: npm run build
```

---

# PM2 Process Manager

PM2 keeps Node.js applications running.

---

# Install PM2

```bash
npm install -g pm2
```

---

# Start Application

```bash
pm2 start dist/server.js
```

---

# Monitor Processes

```bash
pm2 monit
```

---

# Restart App

```bash
pm2 restart all
```

---

# Database Deployment

Production databases should be hosted securely.

---

# Popular Database Hosting

| Database | Hosting |
|---|---|
| MongoDB | MongoDB Atlas |
| PostgreSQL | Supabase |
| MySQL | PlanetScale |

---

# MongoDB Atlas Connection

```bash
mongodb+srv://username:password@cluster.mongodb.net/mydb
```

---

# SSL & HTTPS

Production apps should always use HTTPS.

---

# Benefits

- Secure communication
- Better SEO
- User trust

---

# Performance Optimization

---

# Use Compression

```bash
npm install compression
```

---

# Usage

```ts
import compression from "compression";

app.use(compression());
```

---

# Caching

Caching improves performance.

---

# Example

```ts
res.set(
  "Cache-Control",
  "public, max-age=3600"
);
```

---

# Monitoring Tools

| Tool | Purpose |
|---|---|
| PM2 | Process monitoring |
| Sentry | Error tracking |
| New Relic | Performance monitoring |

---

# Sentry Integration

Install Sentry:

```bash
npm install @sentry/node
```

---

# Example

```ts
import * as Sentry from "@sentry/node";

Sentry.init({
  dsn: "YOUR_DSN"
});
```

---

# Backup Strategy

Always backup production databases.

---

# Backup Benefits

- Data recovery
- Disaster protection
- Business continuity

---

# API Rate Limiting

Protect APIs from abuse.

---

# Install Express Rate Limit

```bash
npm install express-rate-limit
```

---

# Example

```ts
import rateLimit from "express-rate-limit";

const limiter = rateLimit({
  windowMs: 15 * 60 * 1000,
  max: 100
});

app.use(limiter);
```

---

# Professional Deployment Architecture

```bash
Production Stack
│
├── Frontend
├── Backend API
├── Database
├── CDN
├── Monitoring
├── Reverse Proxy
└── SSL
```

---

# Reverse Proxy with Nginx

Nginx improves:

- Performance
- Security
- Load balancing

---

# Example Nginx Config

```nginx
server {
  listen 80;

  location / {
    proxy_pass http://localhost:5000;
  }
}
```

---

# Scaling Applications

Scaling methods:

| Type | Description |
|---|---|
| Vertical Scaling | Increase server power |
| Horizontal Scaling | Add more servers |

---

# Common Beginner Mistakes

| Mistake | Problem |
|---|---|
| Hardcoded secrets | Security risk |
| No environment variables | Unsafe deployment |
| No error handling | Crashes |
| No backups | Data loss |

---

# Best Practices

- Use environment variables
- Enable HTTPS
- Use logging systems
- Monitor production apps
- Optimize builds
- Use CI/CD pipelines

---

# Real-world Deployment Example

```bash
Frontend:
Vercel

Backend:
Render

Database:
MongoDB Atlas

Monitoring:
PM2 + Sentry
```

---

# Advantages of Proper Deployment

- Better scalability
- Higher performance
- Improved security
- Reliable production systems
- Professional architecture

---

# Conclusion

Deployment and production management are critical parts of professional TypeScript development.

They help developers build:

- Scalable systems
- Secure applications
- Production-ready APIs
- Enterprise architectures
- Reliable software solutions


