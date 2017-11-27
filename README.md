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
