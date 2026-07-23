# Exercises

Do these without building the full validator.

## 1. Source navigation

From the official [`validator/src/main.rs`](https://github.com/anza-xyz/agave/blob/3b1b239ce2ae3868dce17ff0e06fd0ac32313592/validator/src/main.rs), locate:

1. where the `run` subcommand is declared;
2. where `commands::run::execute` is re-exported;
3. where the shared command error type is declared.

Write the file and line in `notes.md`, then explain why `main.rs` can use the shorter paths it uses.

## 2. Ownership tracing

For each value, write **owned**, **shared borrow**, or **moved at this call** at the relevant point:

- `default_args` passed to `app`;
- `cli_app` used by `get_matches`;
- the string passed to `PathBuf::from`;
- `ledger_path` passed to an administrative handler;
- `primordial_caps` placed into `Config`.

## 3. Dispatch prediction

Predict the selected match arm for:

```text
agave-validator --ledger /data/ledger
agave-validator --ledger /data/ledger run
agave-validator --ledger /data/ledger monitor
agave-validator --ledger /data/ledger init
```

Do not predict what deeper handlers do.

## 4. Small code exercise

On paper, write a five-arm TypeScript `switch` corresponding to the Rust `match`. Then list two things the Rust patterns express more directly (hint: tuple destructuring and `Some(...)`).

## 5. Contributor lens

Check whether adding a new operator command would require changing both the CLI grammar and dispatch. Explain what would happen if only one side changed. This is a promising documentation/test-improvement area because grammar/dispatcher drift ends at `unreachable!()`.
