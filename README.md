# Codex Rust Codebase Exploration

This repository contains my work for the CSE 598 Agentic AI Code Reading Warmup assignment. The purpose of the assignment was to verify my Rust development environment and practice navigating, understanding, and tracing code in a large Rust project.

## Work Completed

* Verified the installed Rust compiler and Cargo toolchain.
* Checked out the required Codex repository commit: `4347f94d55`.
* Successfully checked the `codex-core` crate with Cargo.
* Explored the crates and executable entry points in the `codex-rs` workspace.
* Examined internal modules in the `codex-core` crate.
* Used VS Code and rust-analyzer to perform a successful Go-to-Definition jump.
* Created a hand-drawn diagram showing selected crate dependencies.
* Followed a call chain three levels through the source code.

## Call Trace

```text
cli/src/main.rs:1064 (main)
    ->
cli/src/main.rs:1072 (cli_main)
    ->
exec/src/lib.rs:246 (run_main)
```

## Code Explanation

This code path starts the Codex CLI, parses and routes the selected subcommand, and sends a `codex exec` request to the non-interactive execution runner.

Its inputs are parsed CLI options, helper-executable paths in `Arg0DispatchPaths`, and startup state; its outputs are an `anyhow::Result<()>` and terminal-visible execution results or errors.

## Assignment Files

* `01_rustc_version.png` — Rust compiler version verification
* `02_git_commit.png` — Required Git commit verification
* `03_goto_definition_before.png` — Source location before Go-to-Definition
* `04_goto_definition_after.png` — Definition reached after the jump
* `05_crate_dependency_diagram.jpg` — Hand-drawn crate dependency diagram
* `06_trace_record.docx` — Three-level source-code trace and explanation

## Tools Used

* macOS Terminal
* Rust and Cargo
* Git
* Visual Studio Code
* rust-analyzer
* ripgrep
