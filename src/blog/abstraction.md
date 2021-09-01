# Abstraction

There are a few abstractions in Rust that follow the same pattern that seems very general:

1. A fairly simple Rust trait that requires a capability from the implementations.
2. A set of composable types and operations that implement that trait.
3. A set of functions that consume types with that trait.

At a minimum `Iterator`, `Future` and `Stream` use this pattern.

I wonder if it has a name.
