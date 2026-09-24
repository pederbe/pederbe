# Dr. Peder Bergan

I'm a software developer focused on Rust and open source, with a background in building web applications and business tools. I enjoy turning practical problems into useful software.

My background spans software development, business analysis, research, and IT leadership. Earlier in my career, I developed business software for a Toyota dealership and a legislative-text web application prototype for Norway's Ministry of Justice. I later worked on business analysis and software delivery at the European Parliament, coordinating an international development team.

I use AI in development, including code generation. My work includes defining and speccing the problem, directing implementation, and working through tests and review feedback.

Based in Essen, Germany. PhD in Information Systems.

[Website and contact](https://pederbe.dev/) · [Contributions](https://github.com/pulls?q=is%3Apr+author%3Apederbe+is%3Apublic)

## Technologies

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

### DeepTutor: diagnose setup problems before a session

My contribution added `deeptutor doctor` to check model configuration, credentials, writable storage, and configured retrieval backends. It provides terminal and JSON output, with a failing exit status when required checks fail. Provider requests require `--online`.

The PR added tests for diagnostics, credential redaction, and CLI behavior. It reports 78 CLI tests passing and one skipped; the remote test summary also passed. The command gives users a way to investigate setup problems before starting a session.

[View the contribution · PR #959](https://github.com/HKUDS/DeepTutor/pull/959)

### KeePassXC: save password-generation profiles per database

I added named password and passphrase profiles stored inside each encrypted database. Users can save generator settings, choose a database default, and keep an entry associated with the profile used for its password without changing KeePassXC's global generator settings.

The C++/Qt contribution builds on earlier work by KeePassXC maintainer droidmonkey. It adds stable profile IDs, validation, database and GUI integration, documentation, translations, and regression coverage for persistence, merge behavior, entry save/cancel behavior, missing profiles, and locking.

[View the contribution · PR #13652](https://github.com/keepassxreboot/keepassxc/pull/13652)
