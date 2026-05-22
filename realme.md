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



