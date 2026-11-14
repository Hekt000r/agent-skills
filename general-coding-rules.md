description: Rules for coding that should be always be applied to every coding task

### Variable naming patterns
Variables and should use camelCase, classes and types use PascalCase, constants use UPPER_SNAKE_CASE

For C language, variables and types should use snake_case

### Function length and surface
A single function should be no longer than 70 lines of code.

A function should do only one thing. Both these rules must be respected, and if your function doesnt fit, it should be broken down into smaller pieces.

The purpose and functionality of a function should be clear and concrete

### File length and surface
Similar to functions, files should not be over 350 lines of code.

Files should respect seperation of concerns,
for example business logic and HTTP routing should not be in the same file. Split by individual task (ex. calculateChange.c, performs a single task, calculates the change from a total and cash), (ex. getRecieptRoute.ts handles HTTP parsing and response)

Files should group together code that perform a single task that involves multiple steps


It should be clear by the name what the code inside is about. 

### Folders
Root folders (ex. src/, dist/, public/) should be use to organize the project and its assets as a whole

Code folders (ex. src/engine/) should be used whenever there is more than one file for a specific domain or feature (ex. src/plugins, src/engine, src/route)

### OOP best practices

Use OOP patterns (classes, methods) when:
- Multiple instances of the same code but different data is needed (ex. plugins, game objects, UI components
- Code needs to be highly reusable across many different sections (ex. a group of helper methods for assisting logic in a certain feature or domain
- The problem is naturally expressable withh classes and methods

Avoid:
- Deep, complicated inheritance chains
- Massive monolith classes
- Unneccessary use of encapsulation / abstraction
