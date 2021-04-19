# Best practise for writing clean code

## Naming of variables, methods, classes [1, p.48]
A name of a variable, function, or class, should answer why it exists, what it does, and how it is used. If a name requires a comment, then the name does not reveal its intent.

### Classes
- Classes and objects should have noun or noun phrase names like Customer, WikiPage, Account, and AddressParser. A class name should not be a verb.
- The class name should be concrete. Avoid words like Manager, Processor, Data, Controller or Info in the name of a class, because they are too general to be used.

### Methods name
- Methods should have verb or verb phrase names like postPayment, deletePage, or save. Accessors, mutators, and predicates should be named for their value and prefixed with get, set, and is according to the javabean standard.
- Peak a concept and stick with it. For instance, it’s confusing to have fetch, retrieve, and get as equivalent methods of different classes.

## Functions[1, p.62]
- Functions should be small
- Functions should do one thing. In order to make sure our functions are doing “one thing,” we need to make sure that the statements within our function are all at the same level of abstraction.
- Keep function arguments small(max 3), so that anyone can understand and test it.
- Name of a function should clearly express what it does and nothing else. If function is named as "read" it should do only read operation.

## Comments[1, p.84]
“Don’t comment bad code—rewrite it.” — Brian W. Kernighan and P. J. Plaugher 1

- When you find yourself in a position where you need to write a comment, think it through and see whether there isn’t some way to turn the tables and express yourself in code
- TODO comments should not be an excuse to leave bad code in the system

## Tests[1, p.152]
"If you let the tests rot, then your code will rot too. Keep your tests clean." — Robert C.Martin

- Test code is not second-class citizen, it is as important as production code. It must be kept as clean as production code.

## Nullable

- If method returns null(or there is a possibility to return null), it should either be marked as javax.annotation.Nullable or method should return Optional.
- If an argument from the argument list is null(or there is a possibility to point to null) it should either be marked as javax.annotation.Nullable or argument should be Optional
- If a class member points to null(or there is a possibility to point to null) it should either be marked with javax.annotation.Nullable or class member should be Optional.

## Follow SOLID principles

1. There should never be more than one reason for a class to change(SRP)[2, p. 95]
2. Software entities(classes, modules, functions) should be open for extension, but closed for modification(OCP)[2, p.99]
3. Subtypes must be substitutable for their base types(LSP)[2, p.111]
4. Abstraction should not depend on details. Details should depend on abstractions(DIP)[2, p.127]
5. Many client-specific interfaces are better than one general-purpose interface(ISP)[2, 135]

# References:
1. [Clean Code : A Handbook of Agile Software Craftsmanship, Robert Martin](Clean.Code.2008.pdf)
2. [Agile Software Development, Principles, Patterns, and Practices, Robert Martin](Agile.Software.Development.pdf)
