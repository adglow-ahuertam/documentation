Angular Style Guide
===================


This present document  is for defining the syntax, conventions, and application structure we should use while working woth Angular framework.

----------

Single responsability
-------------
> **Tip:** Apply the [single responsibility principle (SRP)](https://wikipedia.org/wiki/Single_responsibility_principle) to all components, services, and other symbols. This helps make the app cleaner, easier to read and maintain, and more testable.

----------


Rule of One
-------------------

Do define one thing, such as a service or component, per file.
Consider limiting files to **400** lines of code.
The key is to make the code more reusable, easier to read, and less mistake prone.
It is a better practice to redistribute the component and its supporting classes into their own, **dedicated files**.

> - Why? One component per file makes it far easier to read, maintain, and avoid collisions with teams in source control.
> - Why? One component per file avoids hidden bugs that often arise when combining components in a file where they may share variables, create unwanted closures, or unwanted coupling with dependencies.
> - Why? A single component can be the default export for its file which facilitates lazy loading with the router.


----------

Small functions
-------------

Do define small functions
Consider limiting to no more than **75** lines.
> - Why? Small functions are easier to test, especially when they do one thing and serve one purpose.
> - Why? Small functions promote reuse.
> - Why? Small functions are easier to read.
> - Why? Small functions are easier to read.
> - Why? Small functions are easier to maintain.
> - Why? Small functions help avoid hidden bugs that come with large functions that share variables with external scope, create unwanted closures, or unwanted coupling with dependencies.

----------

Naming
--------------------

Naming conventions are hugely important to maintainability and readability. This guide recommends naming conventions for the file name and the symbol name.

### General Naming Guidelines

Do use consistent names for all symbols.
Do follow a pattern that describes the symbol's feature then its type. The recommended pattern is feature.type.ts.
>**Why?**
>-  Naming conventions help provide a consistent way to find content at a glance. Consistency within the project is vital. Consistency with a team is important. Consistency across a company provides tremendous efficiency.
>- The naming conventions should simply help find desired code faster and make it easier to understand.
>-  Names of folders and files should clearly convey their intent. For example, app/heroes/hero-list.component.ts may contain a component that manages a list of heroes.

### Separate file names with dots and dashes

Do use dashes to separate words in the descriptive name.
Do use dots to separate the descriptive name from the type.
Do use consistent type names for all components following a pattern that describes the component's feature then its type. A recommended pattern is feature.type.ts.
Do use conventional type names including .service, .component, .pipe, .module, and .directive. Invent additional type names if you must but take care not to create too many.


>**Why?**
>-  Type names provide a consistent way to quickly identify what is in the file.
>- Type names make it easy to find a specific file type using an editor or IDE's fuzzy search techniques.
>-  Unabbreviated type names such as .service are descriptive and unambiguous. Abbreviations such as .srv, .svc, and .serv can be confusing.
>-  Type names provide pattern matching for any automated tasks.
