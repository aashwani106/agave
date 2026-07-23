# Glossary

- **binary / executable:** machine code the operating system can start.
- **crate:** a Rust compilation unit. This package has a binary crate (`main.rs`) and a library crate (`lib.rs`).
- **module:** a namespace and visibility boundary inside a crate, such as `commands::run`.
- **macro:** code that expands from tokens at compile time; invoked with `!`, such as `version!()`.
- **attribute:** metadata/instruction written as `#[...]`; `#![...]` applies to the enclosing item/crate.
- **borrow (`&T`):** temporary shared access without transferring ownership.
- **move:** transfer of ownership from one binding/container to another.
- **`Option<T>`:** either `Some(T)` or `None`.
- **`Result<T, E>`:** either `Ok(T)` or `Err(E)`.
- **match:** exhaustive pattern-based branching.
- **closure:** an inline callable value, such as `|err| { ... }`.
- **shadowing:** declaring a new binding with the same name as an earlier binding.
- **OS capability:** a granular Linux privilege, narrower than an all-powerful root/non-root split.
- **allocator:** process machinery that provides and reclaims heap memory.

