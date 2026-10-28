# Dr. Peder Bergan

I'm a full-stack software engineer building web applications, backend services and developer tools. My recent work includes Esdieff for connected-device models, Ripscope for C code navigation and Fastmash for command-line statistics.

My background spans software development, business analysis, research, and IT leadership. Earlier in my career, I developed business software for a Toyota dealership and a legislative-text web application prototype for Norway's Ministry of Justice. I later worked on business analysis and software delivery at the European Parliament, coordinating an international development team.

Based in Essen, Germany. PhD in Information Systems.

[Website and contact](https://pederbe.dev/) · [Contributions](https://github.com/pulls?q=is%3Apr+author%3Apederbe+is%3Apublic)

## Esdieff: Put device models to work.

I built Esdieff, a command-line tool and Rust library that helps developers explore, check and test connected-device models written in Semantic Definition Format (SDF), defined by IETF RFC 9880.

Esdieff helps teams understand a supplier's interface, catch model mistakes, compare revisions for breaking changes and generate valid, boundary and invalid test values. It also checks recorded values against the model and supports repeatable checks and machine-readable reports.

I've discussed implementation questions with the RFC authors and the IETF ASDF working group, using concrete examples to clarify how the specification should behave.

Free and open source for Linux, macOS and Windows.
[Explore Esdieff](https://github.com/pederbe/esdieff)

## Ripscope: Fast C navigation. An index that keeps up.

I built [Ripscope](https://ripscope.com), a C code navigator written in safe Rust. Find definitions, follow callers and trace assignments through cscope's familiar queries, from Vim, Neovim or Emacs.

Saved edits appear in subsequent editor searches automatically. The index updates changed files in one SQLite transaction, so queries read a complete revision. No compiler, preprocessor or compile database is needed.

[![Ripscope in Vim: search for callers of greet, add and save a call, then search again to see the new caller.](https://ripscope.com/demo.gif)](https://ripscope.com)

Ripscope 0.1.0 is free and open source for x86-64 Linux and Windows. Its public documentation explains the source-reading rules, measured comparisons and recognition limits.

[Try Ripscope](https://ripscope.com) · [Source code](https://github.com/pederbe/ripscope) · [Benchmarks](https://ripscope.com/docs/reference/benchmarks/) · [How it is built](https://ripscope.com/docs/project/how-it-is-built/)

## Fastmash: Fast statistics. Smarter tables.

I built [Fastmash](https://fastmash.io), a Rust command-line tool for statistics on text and quoted CSV. It uses GNU datamash's familiar command language and adds named reports, weighted means, highest and lowest complete-record selection, text-table health checks, and ranked dataset comparisons.

Software 80-bit arithmetic and built-in locale data keep results reproducible for the same version, input, and explicit settings on supported machines. Fastmash runs on Linux x86-64, Windows through WSL2, and Apple Silicon macOS 15 or later.

[![Fastmash terminal demo: installation, colored help, and the same RefGene quartile command in both tools. Both return 4, 8, 14, and 10. The measured timing replay is slowed 20 times.](https://pederbe.dev/media/b70c62c3567c.gif)](https://fastmash.io)

On RefGene quartiles, Fastmash took **26.6 ms versus GNU datamash 1.9's 112.8 ms**, or **4.2 times the speed**, on an Intel laptop running native Linux, with matching output.

[Try Fastmash](https://fastmash.io) · [Source code](https://github.com/pederbe/fastmash) · [Benchmarks](https://fastmash.io/benchmarks/)

<details>
<summary>See the benchmark highlights</summary>

[![Fastmash v0.1.0 benchmark highlights on two native Linux hosts: RefGene quartiles 4.2x and 3.8x, exon statistics per gene 1.9x and 1.7x, sum and mean of one million decimals 2.7x and 2.3x, grouped decimals 1.8x and 1.7x, and many small groups 1.5x and 1.4x.](https://pederbe.dev/media/89144da5e558.webp)](https://fastmash.io/benchmarks/)

</details>

## Technologies

My backend work includes PostgreSQL, authentication, database migrations, webhook delivery and retries. I also work with integration tests, audit logs, metrics and cloud deployments.

My current work focuses on Rust. My earlier web and business applications used JavaScript, PHP, SQL, HTML/CSS, and VBA. I'm also interested in WebAssembly and Linux.

## Selected contributions

### SWC: skip unnecessary work in a compiler transform

The `export_default_from` transform traversed scripts even though it only needed module-level exports. My contribution replaced the visitor with a direct pass that returns immediately for scripts and processes the module body for modules.

The PR added script fixtures, export-rewriting coverage, and benchmarks at two input sizes. The reported benchmarks show improvements for scripts, with the four module cases classified as unchanged.

[View the contribution · PR #12348](https://github.com/swc-project/swc/pull/12348)

### Atuin: filter command history by multiple exit codes

Added support for filtering command history by multiple exit codes, with tests covering exclusions, overlapping filters, and deletion selection.

The change connects repeated CLI flags to database filtering. Included codes match any listed value; exclusions remove every listed code, including overlaps.

[View the contribution · PR #4132](https://github.com/atuinsh/atuin/pull/4132)

### DeepTutor: diagnose AI tutor setup problems

DeepTutor is an open-source AI tutor that helps people learn from their own study materials. I added `deeptutor doctor` to check AI connection settings, access keys, storage permissions and the tools used to search study materials before a session starts. It provides terminal and JSON output for automated checks. Live AI connection tests run only when requested with `--online`.

Tests cover setup checks, keeping access keys out of diagnostic reports and command-line behavior.

[View the contribution · PR #959](https://github.com/HKUDS/DeepTutor/pull/959)

### KeePassXC: save password-generation profiles per database

I added named password and passphrase profiles stored inside each encrypted database. Users can save generator settings, choose a database default, and keep an entry associated with the profile used for its password without changing KeePassXC's global generator settings.

The C++/Qt contribution builds on earlier work by KeePassXC maintainer droidmonkey. It adds stable profile IDs, validation, database and GUI integration, documentation, translations, and regression coverage for persistence, merge behavior, entry save/cancel behavior, missing profiles, and locking.

[View the contribution · PR #13652](https://github.com/keepassxreboot/keepassxc/pull/13652)
