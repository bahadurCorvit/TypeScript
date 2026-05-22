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




