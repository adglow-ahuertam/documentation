Adglow Angular Style Guide
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
>**Why?**
> -  One component per file makes it far easier to read, maintain, and avoid collisions with teams in source control.
> -  One component per file avoids hidden bugs that often arise when combining components in a file where they may share variables, create unwanted closures, or unwanted coupling with dependencies.
> -  A single component can be the default export for its file which facilitates lazy loading with the router.


----------

Small functions
-------------

Do define small functions
Consider limiting to no more than **75** lines.
>**Why?**
> - Small functions are easier to test, especially when they do one thing and serve one purpose.
> - Small functions promote reuse.
> -  Small functions are easier to read.
> -  Small functions are easier to read.
> -  Small functions are easier to maintain.
> -  Small functions help avoid hidden bugs that come with large functions that share variables with external scope, create unwanted closures, or unwanted coupling with dependencies.

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


### Symbols and file names

Do use consistent names for all assets named after what they represent.
Do use upper camel case for class names.
Do match the name of the symbol to the name of the file.
Do append the symbol name with the conventional suffix (such as Component, Directive, Module, Pipe, or Service) for a thing of that type.
Do give the filename the conventional suffix (such as .component.ts, .directive.ts, .module.ts, .pipe.ts, or .service.ts) for a file of that type.


>**Why?**
>-  Consistent conventions make it easy to quickly identify and reference assets of different types.

### Service names

Do use consistent names for all services named after their feature.

Do suffix a service class name with Service. For example, something that gets data or heroes should be called a DataService or a HeroService.

A few terms are unambiguously services. They typically indicate agency by ending in "-er". You may prefer to name a service that logs messages Logger rather than LoggerService. Decide if this exception is agreeable in your project. As always, strive for consistency.


>**Why?**
>-  Provides a consistent way to quickly identify and reference services.
>-   Clear service names such as Logger do not require a suffix.
>-  Service names such as Credit are nouns and require a suffix and should be named with a suffix when it is not obvious if it is a service or something else.

###  Bootstrapping

Do put bootstrapping and platform logic for the app in a file named main.ts.
Do include error handling in the bootstrapping logic.
Avoid putting app logic in main.ts. Instead, consider placing it in a component or service.


>**Why?**
>-  Follows a consistent convention for the startup logic of an app.
>-   Follows a familiar convention from other technology platforms.

###  Directive selectors

Do Use lower camel case for naming the selectors of directives.

>**Why?**
>-  Keeps the names of the properties defined in the directives that are bound to the view consistent with the attribute names.
>-   The Angular HTML parser is case sensitive and recognizes lower camel case.

###  Custom prefix for components

Do use a hyphenated, lowercase element selector value (e.g. admin-users).
Do use a custom prefix for a component selector. For example, the prefix toh represents from Tour of Heroes and the prefix admin represents an admin feature area.
Do use a prefix that identifies the feature area or the app itself.

>**Why?**
>-  Prevents element name collisions with components in other apps and with native HTML elements.
>-   Makes it easier to promote and share the component in other apps.
>-    Components are easy to identify in the DOM.

###  Custom prefix for directives

Do use a custom prefix for the selector of directives (e.g, the prefix toh from Tour of Heroes).
Do spell non-element selectors in lower camel case unless the selector is meant to match a native HTML attribute.

>**Why?**
>-  Prevents name collisions.
>-    Directives are easily identified.

###  Pipe names

Do use consistent names for all pipes, named after their feature.

>**Why?**
>-  Provides a consistent way to quickly identify and reference pipes.

###  Unit test file names

Do name test specification files the same as the component they test.
Do name test specification files with a suffix of .spec.

>**Why?**
>-  Provides a consistent way to quickly identify tests.
>-   Provides pattern matching for karma or other test runners.

###  Angular NgModule names

Do append the symbol name with the suffix Module.
Do give the file name the .module.ts extension.
Do name the module after the feature and folder it resides in.

>**Why?**
>-   Provides a consistent way to quickly identify and reference modules.
>-   Upper camel case is conventional for identifying objects that can be instantiated using a constructor.
>-   Easily identifies the module as the root of the same named feature.

Do suffix a RoutingModule class name with RoutingModule.
Do end the filename of a RoutingModule with -routing.module.ts.
>**Why?**
>-    A RoutingModule is a module dedicated exclusively to configuring the Angular router. A consistent class and file name convention make these modules easy to spot and verify.

###  Coding conventions

Have a consistent set of coding, naming, and whitespace conventions.

####  Classes
Do use upper camel case when naming classes.
>**Why?**
>-  Follows conventional thinking for class names.
>-  Classes can be instantiated and construct an instance. By convention, upper camel case i​
29
----------
30
​
31
Small functions
32
-------------
33
​
34
Do define small functions
35
Consider limiting to no more than **75** lines.
36
> - Why? Small functions are easier to test, especially when they do one thing and serve one purpose.
37
> - Why? Small functions promote reuse.
38
> - Why? Small functions are easier to read.
39
> - Why? Small functions are easier to read.
40
> - Why? Small functions are easier to maintain.
41
> - Why? Small functions help avoid hidden bugs that come with large functions that share variables with external scope, create unwanted closures, or unwanted coupling with dependencies.
42
​
43
----------
44
​
45
Naming
46
--------------------
47
​
48
Naming conventions are hugely important to maintainability and readability. This guide recommends naming conventions for the file name and the symbol name.
49
​​
29
----------
30
​
31
Small functions
32
-------------
33
​
34
Do define small functions
35
Consider limiting to no more than **75** lines.
36
> - Why? Small functions are easier to test, especially when they do one thing and serve one purpose.
37
> - Why? Small functions promote reuse.
38
> - Why? Small functions are easier to read.
39
> - Why? Small functions are easier to read.
40
> - Why? Small functions are easier to maintain.
41
> - Why? Small functions help avoid hidden bugs that come with large functions that share variables with external scope, create unwanted closures, or unwanted coupling with dependencies.
42
​
43
----------
44
​
45
Naming
46
--------------------
47
​
48
Naming conventions are hugely important to maintainability and readability. This guide recommends naming conventions for the file name and the symbol name.
49
​
50
### General Naming Guidelines
51
​
52
Do use consistent names for all symbols.
53
Do follow a pattern that describes the symbol's feature then its type. The recommended pattern is feature.type.ts.
54
>**Why?**
55
>-  Naming conventions help provide a consistent way to find content at a glance. Consistency within the project is vital. Consistency with a team is important. Consistency across a company provides tremendous efficiency.
56
>- The naming conventions should simply help find desired code faster and make it easier to understand.
57
>-  Names of folders and files should clearly convey their intent. For example, app/heroes/hero-list.component.ts may contain a component that manages a list of heroes.
58
​
59
### Separate file names with dots and dashes
60
​
61
Do use dashes to separate words in the descriptive name.
62
Do use dots to separate the descriptive name from the type.
63
Do use consistent type names for all components following a pattern that describes the component's feature then its type. A recommended pattern is feature.type.ts.
64
Do use conventional type names including .service, .component, .pipe, .module, and .directive. Invent additional type names if you must but take care not to create too many.
65
​
66
​
67
>**Why?**
68
>-  Type names provide a consistent way to quickly identify what is in the file.
69
>- Type names make it easy to find a specific file type using an editor or IDE's fuzzy search techniques.
70
>-  Unabbreviated type names such as .service are descriptive and unambiguous. Abbreviations such as .srv, .svc, and .serv can be confusing.
71
>-  Type names provide pattern matching for any automated tasks.
50
### General Naming Guidelines
51
​
52
Do use consistent names for all symbols.
53
Do follow a pattern that describes the symbol's feature then its type. The recommended pattern is feature.type.ts.
54
>**Why?**
55
>-  Naming conventions help provide a consistent way to find content at a glance. Consistency within the project is vital. Consistency with a team is important. Consistency across a company provides tremendous efficiency.
56
>- The naming conventions should simply help find desired code faster and make it easier to understand.
57
>-  Names of folders and files should clearly convey their intent. For example, app/heroes/hero-list.component.ts may contain a component that manages a list of heroes.
58
​
59
### Separate file names with dots and dashes
60
​
61
Do use dashes to separate words in the descriptive name.
62
Do use dots to separate the descriptive name from the type.
63
Do use consistent type names for all components following a pattern that describes the component's feature then its type. A recommended pattern is feature.type.ts.
64
Do use conventional type names including .service, .component, .pipe, .module, and .directive. Invent additional type names if you must but take care not to create too many.
65
​
66
​
67
>**Why?**
68
>-  Type names provide a consistent way to quickly identify what is in the file.
69
>- Type names make it easy to find a specific file type using an editor or IDE's fuzzy search techniques.
70
>-  Unabbreviated type names such as .service are descriptive and unambiguous. Abbreviations such as .srv, .svc, and .serv can be confusing.
71
>-  Type names provide pattern matching for any automated tasks.ndicates a constructable asset.

####  Constants
Do declare variables with const if their values should not change during the application lifetime.
>**Why?**
>-  Conveys to readers that the value is invariant.
>-   TypeScript helps enforce that intent by requiring immediate initialization and by preventing subsequent re-assignment.

Consider spelling const variables in lower camel case.
>**Why?**
>-  Lower camel case variable names (heroRoutes) are easier to read and understand than the traditional UPPER_SNAKE_CASE names (HERO_ROUTES).
>-   The tradition of naming constants in UPPER_SNAKE_CASE reflects an era before the modern IDEs that quickly reveal the const declaration. TypeScript prevents accidental reassignment.

Do tolerate existing const variables that are spelled in UPPER_SNAKE_CASE.
>**Why?**
>-  The tradition of UPPER_SNAKE_CASE remains popular and pervasive, especially in third party modules. It is rarely worth the effort to change them at the risk of breaking existing code and documentation.

####  Interfaces
Do name an interface using upper camel case.
Consider naming an interface without an I prefix.
Consider using a class instead of an interface.

>**Why?**
>-  TypeScript guidelines discourage the I prefix.
>-  A class alone is less code than a class-plus-interface.
>-  A class can act as an interface (use implements instead of extends).
>-  An interface-class can be a provider lookup token in Angular dependency injection.

###  Properties and methods
Do use lower camel case to name properties and methods.
Avoid prefixing private properties and methods with an underscore.

>**Why?**
>-  Follows conventional thinking for properties and methods.
>-   JavaScript lacks a true private property or method.
>-  TypeScript tooling makes it easy to identify private vs. public properties and methods.

###  Import line spacing
Consider leaving one empty line between third party imports and application imports.
Consider listing import lines alphabetized by the module.
Consider listing destructured imported symbols alphabetically.

>**Why?**
>-  The empty line separates your stuff from their stuff.
>-   Alphabetizing makes it easier to read and locate symbols.

###  Application structure and NgModules
Have a near-term view of implementation and a long-term vision. Start small but keep in mind where the app is heading down the road.
All of the app's code goes in a folder named src. All feature areas are in their own folder, with their own NgModule.
All content is one asset per file. Each component, service, and pipe is in its own file. All third party vendor scripts are stored in another folder and not in the src folder. You didn't write them and you don't want them cluttering src. Use the naming conventions for files in this guide.

###  Locate( to do)
###  Identify ( to do)
###  FLAT (to do)

###  T-DRY (Try to be DRY)
Do be DRY (Don't Repeat Yourself).

Avoid being so DRY that you sacrifice readability.

>**Why?**
>-  Being DRY is important, but not crucial if it sacrifices the other elements of LIFT. That's why it's called T-DRY. For example, it's redundant to name a template hero-view.component.html because with the .html extension, it is obviously a view. But if something is not obvious or departs from a convention, then spell it out.

###  Overall structural guidelines (to do)
###  Folders-by-feature structure (to do)
###  App root module (to do)
###  Feature modules (to do)
###  Shared feature module (to do)
###  Core feature module (to do)
###  Prevent re-import of the core module (to do)
###  Lazy Loaded folders (to do)
###  Never directly import lazy loaded folders (to do)
###  Components (to do)
###  Extract templates and styles to their own files (to do)
###  Decorate input and output properties (to do)
###  Avoid aliasing inputs and outputs (to do)
###  Member sequence (to do)
###  Delegate complex component logic to services (to do)
###  Don't prefix output properties (to do)
###  Put presentation logic in the component class (to do)
###  Directives (to do)
###  Services (to do)
###  Data Services (to do)
###  Lifecycle hooks (to do)
###  File templates and snippets (to do)
