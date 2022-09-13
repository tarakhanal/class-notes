
# CSharp Types

## Common Type System
The CTS defined two broad families of types in .NET. These are the "First-class citizens" of .NET.

:::note NOTE
A "first-class citizen" in a programming language is a way of saying "this is a thing a variable can refer to". First class citizens can have a name.
:::

## All the variables in C# can be of two types:

### Value Type
* Lives in Stack
* They structs in C#
* When the variable goes out of scope, it is automically removed from the stack
### Reference Type
* Lives in Heap
* They are classes in C#
* When the variable goes out of scope, it is deallocated using the generational garbage collector algorithm
* Memory is deallocated in a non-deterministic way. That means you can't know when an value is removed from the heap.
* This is known as "non-deterministic finalization".
