# Gradle Playground

## What is Gradle?

- Build by convention.
- Written in Java but the build language is a Groovy DSL.
- Supports dependencies.
    - Ivy and Maven
- Supports multi-project builds.
- Easily customisable.
- Declarative build language
    - Expresses Intent (What rather than how)
    - Maintainable
    
## Basic Gradle Tasks

### What is a Task?
- Code that Gradle executes
    - Tasks have a lifecycle
        - Initialisation phase
        - Configuration phase
        - Execution phase
    - Tasks have properties
    - Tasks have `actions` (Code that is going to execute)
    - Tasks have dependencies
    
So in your `build.gradle` file you can create a task as below:

- `project.task("Task 1")`
- `task("Task 2")`
- `task "Task 3"`
- `task Task4`

And execute: `gradle tasks --all`.

These are the ways to create tasks in a gradle build. And since 
tasks have properties, we can even give tasks description properties
so that they are more meaningful when are using them.

`Task4.description = "Task 4 Description"`

and execute `gradle tasks --all`