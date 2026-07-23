# Quiz — Lesson 01

## Conceptual

1. Why is `main.rs` a process boundary rather than the transaction pipeline?
2. Why can the same executable safely serve both long-running and administrative modes?
3. What distinction exists between a Rust package, crate, and module here?

## Architecture

4. Draw the call path from the OS to `commands::run::execute`.
5. Where is the last common failure boundary for all dispatched commands?
6. Why is allocator selection located outside `main()`?

## Code

7. What ownership change occurs when `get_matches()` is called on `cli_app`?
8. Why can `subcommand` borrow from `matches` safely through dispatch?
9. Explain the two consecutive `primordial_caps` shadowing statements.
10. What is the compile-time difference between Linux and non-Linux `run_config`?
11. How do `inspect_err`, `map_err`, and `unwrap_or_else` play different roles?
12. Why does `exit(1)` satisfy the closure's type even though it does not produce a normal success value?

## Practical checkpoint

Open official [`validator/src/main.rs`](https://github.com/anza-xyz/agave/blob/3b1b239ce2ae3868dce17ff0e06fd0ac32313592/validator/src/main.rs#L75-L133) at a random dispatch arm and narrate:

- source of every argument;
- whether each is owned or borrowed;
- expected return shape;
- final behavior on error.

You are ready for Lesson 02 when you can do this without the walkthrough.

## Interview-style questions

1. How would you explain the difference between process initialization and validator service initialization?
2. Why might a security-sensitive daemon reduce Linux capabilities before dispatch instead of inside each command?
3. If an accepted CLI command reaches `unreachable!()`, what two source areas would you compare first?

## Things to explore next

- How Rust divides this package into a binary crate and library crate.
- How ownership and borrowing let startup code share configuration safely.
- How `Result` creates a consistent error boundary across different command handlers.

Do not trace `commands::run::execute` yet; that is intentionally split into later lessons.
