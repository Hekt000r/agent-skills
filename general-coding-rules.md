description: Rules for coding that should be always be applied to every coding task

### Variable naming patterns
If starting a new project: Use the established naming conventions for the respective language.
In an existing project: Always prioritize existing naming conventions

Most variables should start with `is`,`can`,`should`, (ex. `isAdmin`)
Functions should use verbs that describe their action (ex. `calculateTax()`)

### Function length and surface
A single function should be no longer than 70 lines of code.

A function should do only primarily one thing. (This doesn't mean a function can't have multiple simple steps like calling other functions) 

Both these rules must be respected, and if your function doesnt fit, it should be broken down into smaller pieces.

The purpose and functionality of a function should be clear and concrete

### File length and surface
Similar to functions, files should not be over 350 lines of code.

Files should respect seperation of concerns,
for example business logic and HTTP routing should not be in the same file. Split by individual task (ex. calculateChange.c, performs a single task, calculates the change from a total and cash), (ex. getRecieptRoute.ts handles HTTP parsing and response)

Files should group together code that perform a single task that involves multiple steps


It should be clear by the name what the code inside is about. 

### Folders
Root folders (ex. src/, dist/, public/) should be use to organize the project and its assets as a whole

Code folders (ex. src/engine/) should be used whenever there is more than one file for a specific domain or feature (ex. src/plugins, src/engine, src/login/LoginRoute.ts src/login/LoginService.ts)

### OOP best practices

Use OOP patterns (classes, methods) when:
- Multiple instances of the same code but different data is needed (ex. plugins, game objects, UI components
- Code needs to be highly reusable across many different sections (ex. a group of helper methods for assisting logic in a certain feature or domain
- The problem is naturally expressable withh classes and methods

Avoid:
- Deep, complicated inheritance chains
- Massive monolith classes
- Unneccessary use of encapsulation / abstraction
- Prefer composition over inheritance.

### Do not overengineer
Keep implementations as simple as possible.
Do not add new features, abstractions, dependencies, design patterns, or additional complexity outside of the initial scope, unless explicitly instructed to.

Do not attempt to solve a complex problem on your own if an existing, well-established library can already solve it

Maximize code reusability, never solve the same problem in two places

### Comments
Do not unnecessarily add comments.
Comments should be added when:
- There is extra-ordinarily complex logic being used, that is difficult for the reader to understand
- There is an operation performed that seemingly doesn't belong there. Use comments to explain WHY it's there.

DO NOT add comments when dealing with typical normal logic and established coding patterns

### YAGNI ( You Ain't Gonna Need It ) and DRY (Don't Repeat Yourself)
If you're thinking about adding extra code for a feature you THINK you will need in the future, don't add it. Only add code as is neccessary.
This doesn't mean you shouldn't take in consideration the maintainability of the code respective to future code

Don't Repeat Yourself
Do not solve the same problem in multiple places
This doesn't mean you should create overly vague and general functions/abstractions just so it can be used in multiple places


