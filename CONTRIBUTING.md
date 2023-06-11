# Contributing

**Table of Contents**

- [Newcomers](#newcomers)
- [Useful links](#useful-links)
    - [IDE Configuration](#ide-configuration)
    - [Source code contribution](#source-code-contribution)
    - [Run locally](#run-locally)
    - [FAQ](#Frequently-asked-questions)

**Never report security issues on GitHub, public issues or other public channels (Discord etc.), follow the instruction in the [SECURITY.md](https://github.com/IntellectualSites/.github/blob/main/SECURITY.md) to report vulnerabilities in private.**

We appreciate any kind of contributions: code, documentation, design, etc. Any contribution counts, and the size does not matter!

## Newcomers

If you are a newcomer contributor, look for the label `Good first issue`. Issues labeled like that can be resolved without having an in depth knowledge about the codebase you are contributing to.


### IDE Configuration

If a project has a code style policy, you can find an `.editorconfig` file in the root directory of the project. If you're using IntelliJ, you can install the `EditorConfig` plugin. Writing or reformatting files now follows our standards.

### Source code contribution

- For larger contributions create an issue for any required discussion
- Implement the solution on a branch in your fork that is **not the main branch**
- Once you're done, create a pull request. GitHub will request a review from a maintainer automatically.
    - Remember to title your pull request properly, as it is used for release notes.
    - Please raise one PR for one issue or enhancement you're working on. The smaller the PR change is, the easier and faster it is to review. We don't mind receiving several minor PRs.

### Run locally
To get started, you will need the following software, most of which can be obtained in (most) package managers such as `apt` (Debian / Ubuntu), `homebrew` (macOS / Linux), and more:
- `git` (package `git` everywhere)
- A Java 17 or later JDK (packages vary).
    - [Adoptium](https://adoptium.net/) has builds for most operating systems.
    - If not stated otherwise, our projects make use of Gradle's [Toolchain](https://docs.gradle.org/current/userguide/toolchains.html) feature to allow building with only JRE 8 or later installed. (Gradle will automatically provision JDK 17 for compilation if it cannot find an existing install).

If you are on Windows, you can download git [here](https://git-scm.com/downloads). The instructions for Java apply nevertheless.

Compiling is done by invoking the steps `clean` and `build` with the project's build tool.

## Frequently Asked Questions

### My commit doesn't need a build, what do I do?
Well, quite simple: You add `[ci skip]` to the start of your commit subject.

This case most often applies to changes to files like `README.md`, this very file (`CONTRIBUTING.md`), the `LICENSE.md` file, and so forth.
