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






