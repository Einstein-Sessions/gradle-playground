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

### Writing Simple Tasks

#### What is a Task?
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

### Running Tasks

* If you want to run a task you can execute: `gradle task4`.
* Of course the task will not have/do anything as there are no actions
assigned to it
* All tasks have a method called `doLast()` which we pass a groovy closure.
* So if we add:

```groovy
Task4.doLast { println "This is Task 4"}
```
and execute:

```bash
gradle task4
```

this will present an output on the console when you execute the gradle task `Task4`.
* There are other ways to do this